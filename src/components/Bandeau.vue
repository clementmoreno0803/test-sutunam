<template>
  <div class="bandeau" v-show='toggle'>
    <h5>Livraison Offerte dès 35€ d'achat *</h5>
    <img
      src="../assets/bandeau/croix.svg"
      alt="croix de fermeture de bannière"
      @click="toggle = !toggle"
    />
  </div>
</template>

<script>
export default {
  name: "Bandeau",
  data(){
    return{
      toggle : true
    }
  }
};
</script>

<style>
.bandeau {
  width: 100%;
  background-color: var(--bandeau);
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  z-index: 5;
}
.bandeau img {
  width: 16px;
  height: 16px;
  position: absolute;
  right: 12px;
  top: 12px;
}
</style>
