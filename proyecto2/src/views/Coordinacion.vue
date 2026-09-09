<template>
    <q-page class="pagina">
        <div style="max-width: 90%; margin: 0 auto;">
            <q-img src="@/assets/hero/coordinacion.png" height="450px" fit="cover" class="imagen">
                <div class="absolute-full flex flex-center text-white">
                    <div class="text-center q-px-md">
                        <h1 class="text-h2 text-weight-bolder q-mb-xs">Coordinacion</h1>
                        <p class="text-subtitle1 text-weight-light q-mb-md bg-primary text-sub">
                            Desde la Coordinación, trabajamos cada día para que tu proceso de formación sea de calidad.
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
                    La Coordinación Académica del SENA actúa como el motor operativo y pedagógico de la formación
                    titulada, encargándose de administrar el ciclo de vida administrativo de los estudiantes mediante la
                    gestión de novedades como traslados, aplazamientos, retiros y deserciones. Asimismo, asegura la
                    calidad del proceso educativo mediante la programación eficiente de la planta de instructores y la
                    gestión logística de los ambientes de aprendizaje, garantizando que los espacios de formación e
                    infraestructura se mantengan en óptimas condiciones para la ejecución de los programas.
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
                                <q-img src="@/assets/encargados/coordinador.png" fit="cover" />
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
        horario: '07:30 AM - 12:00 PM',
        jornada: 'Mañana',
        estado: 'Abierto'
    },
    {
        name: 'martes',
        dia: 'Martes',
        horario: '07:30 AM - 12:00 PM',
        jornada: 'Mañana',
        estado: 'Abierto'
    },
    {
        name: 'miercoles',
        dia: 'Miércoles',
        horario: '07:30 AM - 12:00 PM',
        jornada: 'Mañana',
        estado: 'Abierto'
    },
    {
        name: 'jueves',
        dia: 'Jueves',
        horario: '07:30 AM - 12:00 PM',
        jornada: 'Mañana',
        estado: 'Abierto'
    },
    {
        name: 'viernes',
        dia: 'Viernes',
        horario: '07:30 AM - 12:00 PM',
        jornada: 'Mañana',
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
    nombre: 'Luis Carlos Reina ',
    cargo: 'Coordinador académico',
    telefono: '3223561730',
    correo: 'lreinas@sena.edu.com'
})
</script>