<template>
    <h2>Tipo de cuenta: {{tipo}}</h2>
    <h2>Saldo: {{saldo}}</h2>
    <h2>Cuenta {{estado ? 'Activa' : 'Desactivada'}}</h2>
    <div v-for="(servicio, index) in servicios" :key="index">
        {{index + 1}} .- {{servicio}}
    </div> 
    <AccionSaldo texto = 'Aumentar saldo'/>
    <AccionSaldo texto = 'Disminuir saldo'/>
</template>

<script>

import AccionSaldo from './AccionSaldo.vue'

export default {
    data() {
        return {
            saldo: 1000,
            tipo: 'Visa',
            estado: true,
            servicios: ['giro', 'abono', 'transferencia']
        }
    },
    components: {
        AccionSaldo
    },
    methods: {
        //estas opciones se deberán de activar a través del componente hijo
        aumentar() {
            this.saldo = this.saldo + 100;
        },
        disminuir() {
            this.saldo = this.saldo - 100
        }
    }
}
</script>

<style>

</style>