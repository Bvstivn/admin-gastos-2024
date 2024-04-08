<template>
  <div class="dor-columnas">
    <div class="contenedor-grafico">
      <img :src="Imagen" alt="imagen" />
    </div>

    <div class="contenedor-presupuesto">
      <button class="reset-app">Resetear App</button>
      <p>
        <span>Presupuesto:</span>
        {{ formatearCantidad(presupuesto) }}
      </p>
      <p>
        <span>Disponible:</span>
        {{ formatearCantidad(disponible) }}
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
//Helpers
import { formatearCantidad } from '../helpers';

//Definiciones
const props = defineProps({
    presupuesto:{
        type: Number,
        required: true,
    },
    disponible:{
        type: Number,
        required: true,
    }
});

</script>

<style scoped>
.dos-columnas {
  display: flex;
  flex-direction: column;
}
.dos-columnas > :first-child {
  margin-bottom: 3rem;
}
@media (min-width: 768px) {
  .dos-columnas {
    flex-direction: row;
    gap: 4rem;
    align-items: center;
  }
  .dos-columnas > :first-child {
    margin-bottom: 0;
  }
}
.reset-app{
    background-color: #DB2777;
    border: none;
    padding: 1rem;
    width: 100%;
    color: var(--blanco);
    font-weight: 900;
    text-transform: uppercase;
    border-radius: 1rem;
    transition-property: background-color;
    transition-duration: 300ms;
}
.reset-app:hover{
    cursor: pointer;
    background-color: #c91a69;
}
.contenedor-presupuesto {
  width: 100%;
}
.contenedor-presupuesto p {
  font-size: 2.4rem;
  text-align: center;
  color: var(--gris-oscuro);
}
@media (min-width: 768px) {
  .contenedor-presupuesto p {
    font-size: 2.4rem;
    text-align: left;
  }
}
.contenedor-presupuesto span {
    font-weight: 900;
    color: var(--azul);
}
</style>
