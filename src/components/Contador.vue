<template>
    <div>            
        <button type="button" class="btn btn-primary" @click="contador">Contador</button>
        <p>Se ha hecho clic en el botón de arriba {{ clicks }} veces. </p>
    </div>
    
</template>

<script>
export default {
    name:'Contador',
    computed: {
      clicks() {
        return this.$store.state.clicks
      }
    },
    methods:{        
        contador(){
            this.$store.commit('increment')
        }
    }
   
 
}
</script>

<style lang="stylus" scoped>

</style>