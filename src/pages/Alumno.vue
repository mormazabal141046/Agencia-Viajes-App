<template>
<div class="q-pa-lg">
    <h5 class="q-mt-none q-mb-lg"><strong>Reporte del Alumno</strong></h5>
    <q-card class="my-card" flat bordered>
        <q-card-section horizontal>
            <q-card-section class="col">
                <h6 class="q-mt-sm q-mb-lg full-width">Ficha Alumno</h6>
                <q-img class="rounded-borders" src="https://cdn.quasar.dev/img/avatar2.jpg" style="max-width:15%;" />
                <div class="text-h5 q-mt-sm q-mb-lg">Korita Gonzalez</div>
                <div class="flex column">
                    <span><strong>Edad: </strong> 17 años</span>
                    <span><strong>Curso: </strong> 4° Medio D</span>
                    <span><strong>Escuela: </strong> Esperanza Joven</span>
                    <span><strong>Email: </strong> kgonzalez@gmail.com</span>
                </div><br>
                <div class="">
                    <span><strong>Descripcion: </strong></span>
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                </div>
            </q-card-section>
            <q-separator vertical class="q-mx-lg" />

            <q-card-section class="col flex column items-start justify-start">
                <q-card-section  horizontal class="full-width flex justify-center">
                    <q-card-section class="col flex column justify-center items-center"">
                        <h6 class="q-my-md"><strong>Meta del Curso</strong></h6>
                        <h4 class="q-ml-md q-my-md" style="background: rgb(39, 15, 95); color:white; padding:8px 20px; border-radius: 25px;">$1.549.000</h4>
                    
                    </q-card-section>
                    
                    <q-separator vertical class="q-mx-lg" />
                    <q-card-section class="col flex column justify-center items-center">
                        <h6 class="q-my-md"><strong>Aporte del Alumno</strong></h6>
                        <h4 class="q-ml-md q-my-md" style="background: rgb(235, 103, 16); color:white; padding:8px 20px; border-radius: 25px;">$35.000</h4>
                    </q-card-section>
                </q-card-section>

                <h6 class="q-mt-sm q-mb-none full-width">Servicios Contratados</h6>
                <q-list bordered separator class="q-mt-lg full-width">
                    <q-item clickable v-ripple>
                        <q-item-section avatar>
                            <q-icon color="dark" name="assignment_ind" />
                        </q-item-section>
                        <q-item-section>
                            <q-item-label><strong>Contrato</strong></q-item-label>
                            <q-item-label caption>Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
                        </q-item-section>
                        <q-item-section side top>
                            <q-item-label caption class="text-positive">Activo</q-item-label>
                        </q-item-section>
                    </q-item>
                    <q-item clickable v-ripple >
                        <q-item-section avatar>
                            <q-icon color="dark" name="flight_takeoff" />
                        </q-item-section>
                        <q-item-section>
                            <q-item-label><strong>Seguro de Viaje</strong></q-item-label>
                            <q-item-label caption>Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
                        </q-item-section>
                        <q-item-section side top>
                            <q-item-label caption class="text-positive">Activo</q-item-label>
                        </q-item-section>
                    </q-item>
                    <q-item clickable v-ripple >
                        <q-item-section avatar>
                            <q-icon color="dark" name="business_center" />
                        </q-item-section>
                        <q-item-section>
                            <q-item-label><strong>Servicio Equipaje</strong></q-item-label>
                            <q-item-label caption>Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
                        </q-item-section>
                        <q-item-section side top>
                            <q-item-label caption class="text-positive">Activo</q-item-label>
                        </q-item-section>
                    </q-item>
                </q-list>                
            </q-card-section>
        </q-card-section>
        <q-separator />
        <q-card-actions>
            <q-table class="full-width" :data="data" :columns="columns" title="Pagos Abonados" row-key="name" style="box-shadow: none;" />
        </q-card-actions>
    </q-card>

</div>
</template>

<script>
export default {
    name: 'AgenciaViajesAppAlumno',

    data() {
        return {
            active: true,
            progress2: 1000,
            columns: [{
                    name: 'id',
                    required: true,
                    label: '#',
                    align: 'left',
                    field: row => row.id,
                    sortable: true,
                    style: 'max-width: 25px',
                },
                {
                    name: 'detail',
                    align: 'center',
                    label: 'Detalle',
                    field: 'detail',
                    sortable: true
                },
                {
                    name: 'amount',
                    label: 'Monto Abono',
                    field: 'amount',
                    sortable: true
                },
                {
                    name: 'date',
                    label: 'Fecha',
                    field: 'date'
                },
            ],
            data: [
                {   
                    id:1,
                    detail: 'Abono a la Meta',
                    amount: 4500,
                    date: '25-06-2023'  
                },
                {   
                    id:2,
                    detail: 'Abono a la Meta',
                    amount: 4500,
                    date: '25-06-2023'  
                },
                {   
                    id:3,
                    detail: 'Abono a la Meta',
                    amount: 4500,
                    date: '25-06-2023'  
                },
                {   
                    id:4,
                    detail: 'Abono a la Meta',
                    amount: 4500,
                    date: '25-06-2023'  
                },
                {   
                    id:5,
                    detail: 'Abono a la Meta',
                    amount: 4500,
                    date: '25-06-2023'  
                },
                {   
                    id:6,
                    detail: 'Abono a la Meta',
                    amount: 4500,
                    date: '25-06-2023'  
                },
                {   
                    id:7,
                    detail: 'Abono a la Meta',
                    amount: 4500,
                    date: '25-06-2023'  
                },
               
            ]
        };
    },

    mounted() {

    },

    methods: {

    },
};
</script>

<style lang="scss" scoped>

</style>
