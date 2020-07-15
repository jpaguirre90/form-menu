<template>
    <div>            
        <button type="button" class="btn btn-primary" @click="contador" @mouseover="mous_over">Contador</button>
        <p>Se ha hecho clic en el botón de arriba {{ conter }} veces. </p>
    </div>
    
</template>

<script>
export default {
    name:'Contador',
    data(){
        return{
            conter:0
        }
    },
    methods:{
        contador(){
            this.conter++;
        },
        mous_over(){
            console.log("Estoy haciendo mouseover")
        }
    }
   
 
}
</script>

<style lang="stylus" scoped>

</style>