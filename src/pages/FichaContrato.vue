<template>
<div class="q-pa-lg">
    <h5 class="q-mt-none q-mb-lg"><strong>Módulo del Ejecutivo</strong></h5>
    <div class="q-gutter-y-md q-mt-lg">
        <q-card>
            <q-tabs v-model="tab" dense class="text-grey" active-color="primary" indicator-color="primary" align="justify" narrow-indicator>
                <q-tab name="ficha" label="Ficha Contrato" />
                <q-tab name="contracts" label="Contratos" />
                <!-- <q-tab name="movies" label="Movies" /> -->
            </q-tabs>

            <q-separator />

            <q-tab-panels v-model="tab" animated>
                <q-tab-panel name="ficha" class="q-pa-lg ">
                    <div class="flex column justify-center items-center q-pb-xl">
                        <div class="text-h6 q-mb-md">Nuevo Contrato</div>
                        
                        <div class="" style="max-width: 600px;">
                            <q-input class="q-mb-md" rounded outlined v-model="text" stack-label label="Cliente">
                                <template v-slot:prepend>
                                    <q-icon name="person_outline" />
                                </template>
                            </q-input>
                            <q-input class="q-mb-md" rounded outlined v-model="text" stack-label label="Destino">
                                <template v-slot:prepend>
                                    <q-icon name="public" />
                                </template>
                            </q-input>
                            <q-input class="q-mb-md" type="date" rounded outlined v-model="text" stack-label label="Fecha de Viaje">
                                <template v-slot:prepend>
                                    <q-icon name="calendar_month" />
                                </template>
                            </q-input>
                            <q-input class="q-mb-md" type="number" rounded outlined v-model="text" stack-label label="Cantidad Alumnos">
                                <template v-slot:prepend>
                                    <q-icon name="groups" />
                                </template>
                            </q-input>
                            <div class="q-mb-md">
                                <div class="q-pl-md q-pt-md"><q-icon name="fastfood" /> Servicios</div>
                                <q-checkbox v-model="right" label="Primera Clase" />
                                <q-checkbox v-model="right" label="Comida Abordo" />
                                <q-checkbox v-model="right" label="Transporte" />
                                <q-checkbox v-model="right" label="Tour" />
                                <q-checkbox v-model="right" label="Seguro de Viaje" />
                                <q-checkbox v-model="right" label="Membresia Dolares" />
                            </div>
                            <div class="q-mb-md">
                                <div class="q-pl-md q-pt-md"><q-icon name="sailing" /> Actividades</div>
                                <q-checkbox v-model="right" label="Paseo a Caballo" />
                                <q-checkbox v-model="right" label="Piscina Temperada" />
                                <q-checkbox v-model="right" label="Cine" />
                                <q-checkbox v-model="right" label="Paseo en Barco" />
                            </div>
                            <div class="q-mt-xl flex justify-end">
                                <q-btn color="primary" label="Cancelar" class="q-mr-lg" />
                                <q-btn color="secondary" label="Guardar" />
                            </div>
                        </div>
                    </div>
                </q-tab-panel>

                <q-tab-panel name="contracts">
                    <div class="text-h6">Listado Contratos</div>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                </q-tab-panel>

                <!-- <q-tab-panel name="movies">
                    <div class="text-h6">Movies</div>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                </q-tab-panel> -->
            </q-tab-panels>
        </q-card>
    </div>
</div>
</template>

<script>
export default {
    name: 'AgenciaViajesAppFichaContrato',

    data() {
        return {
            tab: 'ficha',
            right: false
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
