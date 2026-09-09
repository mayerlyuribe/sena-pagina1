<template>
    <q-page class="pagina">
        <div style="max-width: 90%; margin: 0 auto;">
            <q-img src="@/assets/hero/bienestar.png" height="450px" fit="cover" class="imagen">
                <div class="absolute-full flex flex-center text-white">
                    <div class="text-center q-px-md">
                        <h1 class="text-h2 text-weight-bolder q-mb-xs">Bienestar</h1>
                        <p class="text-subtitle1 text-weight-light q-mb-md bg-primary text-sub">
                            Formarte va más allá del aula. En Bienestar te acompañamos en cada paso de tu proceso. </p>
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
                    Bienestar al Aprendiz del SENA es una estrategia institucional clave orientada a garantizar la
                    permanencia y el éxito integral de los estudiantes, combinando estímulos socioeconómicos como apoyos
                    de sostenimiento, alimentación, transporte y monitorías con un acompañamiento enfocado en la salud
                    física y mental, el deporte y el desarrollo de habilidades blandas y de liderazgo. A través de este
                    enfoque holístico, la dependencia impulsa la inclusión, la diversidad y la identidad cultural
                    mediante expresiones artísticas, promoviendo hábitos de vida saludable y brindando las herramientas
                    necesarias para potenciar tanto la formación profesional como el crecimiento personal dentro de la
                    comunidad educativa.
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
                                <q-img src="@/assets/encargados/bienestarina.png" fit="cover" />
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
        horario: '07:30 AM - 12:00 PM / 02:00 PM - 06:00 PM',
        jornada: 'Jornada Partida',
        estado: 'Abierto'
    },
    {
        name: 'martes',
        dia: 'Martes',
        horario: '07:30 AM - 12:00 PM / 02:00 PM - 06:00 PM',
        jornada: 'Jornada Partida',
        estado: 'Abierto'
    },
    {
        name: 'miercoles',
        dia: 'Miércoles',
        horario: '07:30 AM - 12:00 PM / 02:00 PM - 06:00 PM',
        jornada: 'Jornada Partida',
        estado: 'Abierto'
    },
    {
        name: 'jueves',
        dia: 'Jueves',
        horario: '07:30 AM - 12:00 PM / 02:00 PM - 06:00 PM',
        jornada: 'Jornada Partida',
        estado: 'Abierto'
    },
    {
        name: 'viernes',
        dia: 'Viernes',
        horario: '07:30 AM - 12:00 PM / 02:00 PM - 06:00 PM',
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
    nombre: ' Maria Delea Arenas Mejía ',
    cargo: ' Coordinadora de cafetería  ',
    telefono: ' 3176377670',
    correo: '  mdarenas@sena.edu.co '
})
</script>