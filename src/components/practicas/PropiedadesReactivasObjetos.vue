<template>
    <div class="container">
        <h1 class="text-center text-muted">{{titulo}}</h1>

        <form class="row g-3">
            <div class="col-12">
                <span class="text-secundary">Objeto persona completo</span>
                <label class="text-center text-primary">{{ objetoPersona }}</label>
            </div>
            <div class="col-6">
                <label for="staticEmail2" class="visually-hidden">Nombre a modificar</label>
                <input 
                    type="text" 
                    class="form-control"
                    v-model="objetoPersona.name"
                >
            </div>
            <div class="col-6">
                <label for="staticEmail2" class="visually-hidden">Edad a modificar</label>
                <input 
                    type="number" 
                    class="form-control"
                    v-model="objetoPersona.age"
                >
            </div>
            <div class="col-12">
                <label for="staticEmail2" class="visually-hidden">Salario a modificar</label>
                <input 
                    type="number" 
                    class="form-control"
                    v-model="objetoPersona.salary"
                >
            </div>
            
            
            <div class="col-md-4" v-if="true">
                <button 
                    @click="modificarNombrePersona"
                    type="submit" 
                    class="btn btn-primary mb-3">
                    Modificar objeto (atributo nombre)
                </button>
            </div>
            <div class="col-md-4" v-if="true">
                <button 
                    @click="modificarSalarioPersona"
                    type="submit" 
                    class="btn btn-primary mb-3">
                    Modificar objeto (atributo Salario)
                </button>
            </div>                
            <div class="col-md-4" v-if="true">
                <button 
                    @click="modificarEdadPersona"
                    type="submit" 
                    class="btn btn-primary mb-3">
                    Modificar objeto  (atributo edad)
                </button>
            </div>                   
        </form>            

    </div>
</template>

<script setup>
    import { reactive } from 'vue';

    defineProps({
    titulo: {
      type: String,
      required: false
    }
  })

    const limiteInferior = 1;

    // Tipo complejo que está envuelto por: reactive (reactividad aplicada en objetos).
    let objetoPersona = reactive({
        name: '',
        age: 0,
        salary: 0
    });

    const modificarNombrePersona = (e) => {
        e.preventDefault();        
        objetoPersona.name = 'jaime'
    }

    const modificarEdadPersona = (e) => {
        e.preventDefault();        
        objetoPersona.age = 37;
    }
    
    const modificarSalarioPersona = (e) => {
        e.preventDefault();        
        objetoPersona.salary = 500000;
    }
    
</script>

<style>

</style>