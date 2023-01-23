<template>
    <div class="container">
        <h1 class="text-center text-muted">Vue 3 + Bootstrap 5</h1>

        <form class="row g-3">
            <div class="col-12">
                esto es una interpolación :
                <label class="text-center text-primary">{{ contador }}</label>
            </div>
            <div class="col-auto">
                <label for="staticEmail2" class="visually-hidden">Número</label>
                <input 
                    type="number" 
                    class="form-control"
                    v-model="contador"
                >
            </div>
            <div class="col-auto">
                <button 
                    @click="incrementarContador"
                    type="submit" 
                    class="btn btn-primary mb-3">
                    Procesar
                </button>
            </div>
        </form>            

    </div>
</template>

<script setup>
    import { ref } from 'vue';

    const limiteInferior = 1;
    let contador = ref(0);

    const incrementarContador = (e) => {
        e.preventDefault();
        contador.value = contador.value + limiteInferior;
        // console.log("Salida de la variable contador: >>>", contador.value);
    }
    
</script>

<style>

</style>