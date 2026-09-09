<template>
    <q-page class="pagina">
        <div style="max-width: 90%; margin: 0 auto;">
            <q-img src="@/assets/hero/enfermeria.png" height="450px" fit="cover" class="imagen">
                <div class="absolute-full flex flex-center text-white">
                    <div class="text-center q-px-md">
                        <h1 class="text-h2 text-weight-bolder q-mb-xs">Enfermería</h1>
                        <p class="text-subtitle1 text-weight-light q-mb-md bg-primary text-sub">
                            Tu salud es primero. El servicio de enfermería del SENA está para acompañarte y cuidarte.
                        </p>
                    </div>
                </div>
            </q-img>
        </div>

        <div class="q-mt-xl q-mb-xl flex flex-center">
            <q-card dark bordered class="bg-accent card text-black tarjeta">
                <q-card-section class="bg-grey-6">
                    <div class="text-h6 text-white">Descripción</div>
                </q-card-section>

                <q-separator dark inset />

                <q-card-section>
                    El servicio de enfermería del SENA opera como un espacio fundamental de atención primaria y
                    bienestar estudiantil, equipado con zona de valoración, camillas de observación e insumos de
                    emergencia para responder rápidamente ante accidentes menores, malestares súbitos y la
                    estabilización de signos vitales. Más allá de la respuesta inmediata a primeros auxilios y la
                    gestión de remisiones médicas a centros de mayor complejidad cuando se requiere, este servicio
                    lidera activamente programas de promoción y prevención (PyP) en hábitos saludables, vacunación y
                    salud sexual, garantizando así un acompañamiento integral que protege la salud física y apoya el
                    rendimiento formativo de todos los aprendices dentro de la institución.
                </q-card-section>
            </q-card>
        </div>
        <div class="row horarios flex flex-center q-col-gutter-md justify-evenly">

            <div class="col-7">
                <q-table flat bordered title="Horarios de atención" :rows="rows" :columns="columns" row-key="name"
                    hide-header hide-bottom />
            </div>
            <div class="col-3 ">
                <q-card bordered flat class=" border bg-grey-3 my-card">
                    <div class="row justify-end q-mb-sm">
                        <q-badge color="primary" class="q-pa-sm text-subtitle2 rounded-borders shadow-1">
                            Encargado
                        </q-badge>
                    </div>
                    <q-card-section>
                        <div class="flex flex-center" style="width: 100%;">
                            <q-avatar size="180px" class="shadow-2">
                                <q-img src="@/assets/encargados/enfermera.png" fit="cover" />
                            </q-avatar>
                        </div>
                        <q-separator class="q-mt-md"></q-separator>
                        <div class="text-h5 q-pt-md">{{ encargado.nombre }}</div>
                        <div>
                            <p class="q-pt-none">Correo: {{ encargado.correo }}o</p>
                            <p class=" q-pb-none">Teléfono: {{ encargado.telefono }} </p>
                            <p class="q-pb-none">Cargo: {{ encargado.cargo }}</p>
                        </div>

                    </q-card-section>

                </q-card>
            </div>
        </div>
        <div>

        </div>
    </q-page>


</template>

<style>
.imagen {
    border-radius: 20px;
    overflow: hidden;
}

.text-sub {
    opacity: 0.8;
    border-radius: 10px;
    padding: 0 10px;
}

.pagina {
    padding-top: 50px;
    justify-content: center;
    flex-direction: column;
}

.tarjeta {
    width: 100%;
    max-width: 90%;
    margin: 0 auto;
}
</style>

<script setup>

import { ref } from 'vue'

const columns = [
    { name: 'dia', align: 'left', field: 'dia' },
    { name: 'horario', align: 'center', field: 'horario' },
    { name: 'jornada', align: 'center', field: 'jornada' },
    { name: 'estado', align: 'center', field: 'estado' }
]

const rows = ref([
    {
        name: 'lunes',
        dia: 'Lunes',
        horario: '06:30 AM - 10:30 AM / 04:00 PM - 08:00 PM',
        jornada: 'Jornada Partida',
        estado: 'Abierto'
    },
    {
        name: 'martes',
        dia: 'Martes',
        horario: '06:30 AM - 10:30 AM / 04:00 PM - 08:00 PM',
        jornada: 'Jornada Partida',
        estado: 'Abierto'
    },
    {
        name: 'miercoles',
        dia: 'Miércoles',
        horario: '06:30 AM - 10:30 AM / 04:00 PM - 08:00 PM',
        jornada: 'Jornada Partida',
        estado: 'Abierto'
    },
    {
        name: 'jueves',
        dia: 'Jueves',
        horario: '06:30 AM - 10:30 AM / 04:00 PM - 08:00 PM',
        jornada: 'Jornada Partida',
        estado: 'Abierto'
    },
    {
        name: 'viernes',
        dia: 'Viernes',
        horario: '06:30 AM - 10:30 AM / 04:00 PM - 08:00 PM',
        jornada: 'Jornada Partida',
        estado: 'Abierto'
    },
    {
        name: 'sabado',
        dia: 'Sábado',
        horario: 'Cerrado',
        jornada: 'Sin Atención',
        estado: 'Cerrado'
    },
    {
        name: 'domingo',
        dia: 'Domingo',
        horario: 'Cerrado',
        jornada: 'Sin Atención',
        estado: 'Cerrado'
    },
    {
        name: 'festivos',
        dia: 'Festivos',
        horario: 'Cerrado',
        jornada: 'Sin Atención',
        estado: 'Cerrado'
    }
])

const encargado = ref({
    nombre: 'María Fernanda Gómez Reyes ',
    cargo: 'Enfermera',
    telefono: '3214153995',
    correo: 'mfgomez@sena.edu.co'
})
</script>