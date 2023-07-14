<template>
  <div class="entry-title d-flex justify-content-between p-2">
    <span class="text-success fs3 fw-bold">12</span>
    <span class="mx-1 fs3">Julio</span>
    <span class="mx-2 fs4 fw-light">2023, miercoles</span>
  </div>

  <div>
    <button class="btn btn-danger mx-2"> Borrar
        <i class="fa fa-trash-alt"></i>
    </button>
    
    <button class="btn btn-success"> Subir imagen
        <i class="fa fa-upload"></i>
    </button>
  </div>

  <hr>
  <div class="d-flex flex-column px-3 h-75">
    <textarea placeholder="¿Qué sucedió hoy?">
        
    </textarea>
  </div>

  <Fab icon="fa-save"/>

  <img 
  src="http://blogthinkbig.com/wp-content/uploads/sites/4/2014/12/diferencia-entre-gif-png-y-jpg1.jpg?resize=610%2C421" 
  alt="entry-picture"
  class="img-thumbnail"/>
</template>

<script>
import { defineAsyncComponent } from 'vue'
export default {

    components:{
        Fab: defineAsyncComponent(()=> import('../components/Fab.vue'))
    }

}
</script>

<style lang="scss" scoped>
textarea{
    font-size: 20px;
    border: none;
    height: 100%;
    
    &:focus{
        outline: none;
    }
}

img{
    width: 200px;
    position: fixed;
    bottom: 150px;
    right: 20px;
    box-shadow: 0px 5px 10px rgba($color: #000000, $alpha: 0.2);
}


</style>