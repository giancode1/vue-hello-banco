<template>
  <h1>Tipo de Cuenta: {{cuenta}}</h1>
  <h2>Saldo: {{saldo}} </h2>
  <h3>Cuenta {{ estado ? 'Activa':'Desactivada'}}</h3>
  <div v-for="(item,index) in servicios" :key="index">
      {{index+1}}-{{ item }}
  </div>
  <!-- si puedo usar camelCase -->
  <AccionSaldo 
        texto='Aumentar Saldo'
        @accion='aumentar'
  />   
  <AccionSaldo 
        texto='Disminuir Saldo'
        @accion='disminuir'
        :desactivar='desactivar'
  />
</template>

<script>
import AccionSaldo from './AccionSaldo'

export default {
    name: 'Cuenta',
    components:{
        AccionSaldo
    },
    data() {
        return {
            saldo: 1000,
            cuenta: 'ahorros',
            estado: true,
            servicios: ['giro','abono','transferencias'],
            desactivar: false
        }
    },
    methods:{
        aumentar(){
            this.saldo = this.saldo + 100
            this.desactivar=false

        },
        disminuir(){
            if(this.saldo==0){
                this.desactivar=true
                alert('Saldo Agotado')
            }else{
            this.saldo = this.saldo - 100}
        }
    }
}
</script>

<style>

</style>