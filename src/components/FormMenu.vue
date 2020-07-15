<template>
    <form @submit="enviar" action="">
        <div class="row">
            <div class="col-md-4 offset-md-4">
                
                <h3>Menú</h3>
                <div class="input-group">
                    <div class="input-group-prepend">
                        <span class="input-group-text">Nombre del Plato</span>
                    </div>
                    <input v-model="nombre" type="text" aria-label="First name" class="form-control">
                </div>
                <p></p>
                <div class="input-group">
                    <div class="input-group-prepend">
                        <span class="input-group-text">Precio $</span>
                    </div>
                    <input v-model="precio" type="number" aria-label="First name" class="form-control">
                </div><p></p>
                <select class="custom-select" v-model="categoria">Categoria
                    <option selected>Categoria</option>
                    <option value="entrada">Entrada</option>
                    <option value="pincipal">Plato Principal</option>
                    <option value="acomp">Acompañamiento</option>
                    <option value="postre">Postre</option>
                </select>
                <p></p>
                <textarea v-model="descripcion" placeholder="Descripción"></textarea>
                <div class="custom-control custom-radio custom-control-inline">
                    <input type="radio" id="customRadioInline1" name="customRadioInline1" class="custom-control-input">
                    <label class="custom-control-label" for="customRadioInline1">Valparaíso</label>
                </div>
                <div class="custom-control custom-radio custom-control-inline">
                    <input type="radio" id="customRadioInline2" name="customRadioInline1" class="custom-control-input">
                    <label class="custom-control-label" for="customRadioInline2">Viña del Mar</label>
                </div><p></p>
                <!-- Button trigger modal -->
                <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#staticBackdrop">
                Añadir plato
                </button><p></p>

                <!-- Modal -->
                <div class="modal fade" id="staticBackdrop" data-backdrop="static" data-keyboard="false" tabindex="-1" role="dialog" aria-labelledby="staticBackdropLabel" aria-hidden="true">
                    <div class="modal-dialog">
                        <div class="modal-content">
                        <div class="modal-header">
                            <h5 class="modal-title" id="staticBackdropLabel">Plato ingresado correctamente</h5>
                            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                            <span aria-hidden="true">&times;</span>
                            </button>
                        </div>
                        <div class="modal-body">
                            <img src="@/assets/chayane.jpg" alt="">
                        </div>
                        <div class="modal-footer">
                            <button type="button" class="btn btn-secondary" data-dismiss="modal">Cerrar</button>
                            <button type="button" class="btn btn-primary">Aceptar</button>
                        </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>        
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
      descripcion: ''
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

<style scoped>
textarea{
    width: 100%;
    border-radius: 5px;
}
img{
    display: block;
    position: relative;
    width: 100%;
}
</style>