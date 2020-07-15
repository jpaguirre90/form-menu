<template>
    <form @submit="enviar" action="">
        <h3>Menú</h3>
            <p>Nombre del plato: <input type="text" v-model="nombre"></p>
            <p>Precio: $<input type="number" v-model="precio" required min="1000" max="10000"></p>
            <p>Categoría:
                <select v-model="categoria">
                    <option value="entrada">Entrada</option>
                    <option value="pincipal">Plato Principal</option>
                    <option value="acomp">Acompañamiento</option>
                    <option value="postre">Postre</option>
                </select>
            </p>
            <p>Descripción: <textarea v-model="descripcion"></textarea></p>
            <input type="checkbox" id="checkbox" v-model="checked">
            <label for="checkbox">¿Esta seguro?</label>
            <p>Esta seguro nuevamente</p><input type="radio" v-model="pick" v-bind:value="a">
            <p><input type="submit" value="Añadir Item"></p>
    </form>
    
</template>

<script>
export default {
name: 'FormMenu',
  data() {
    return {
      nombre: '',
      precio: 0,
      categoria: '',
      descripcion: '',
      opciones: []
    }
  },
  methods: {
    enviar: function(ev) {
      ev.preventDefault();
      console.log(this.nombre)
    }
  }
}
</script>

<style lang="stylus" scoped>

</style>