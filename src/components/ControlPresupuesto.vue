<template>
    <div class="dor-columnas">
        <div class="contenedor-grafico">
            <img :src="Imagen" alt="imagen">
        </div>

        <div class="contenedor-presupuesto">
            <button class="reset-app">Resetear App</button>
            <p>
                <span>Presupuesto:</span>
                $0
            </p>
            <p>
                <span>Disponible:</span>
                $0
            </p>
            <p>
                <span>Gastado:</span>
                $0
            </p>
        </div>
    </div>
</template>

<script setup>
//Imagen
import Imagen from "../assets/img/grafico.jpg";
</script>