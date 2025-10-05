<template>
  <section>
    <div class="hero-layout">
      <header class='hero-header'>
        <div class="hero-left flex-center">
      <img src="../assets/images/logo.svg" alt="">
    </div>
    <div class="hero-right flex-center">
      <img src="../assets/images/icon-units.svg" alt="Unit Icons">
      <h2 class="text-preset-7">Units</h2>
      <img src="../assets/images/icon-dropdown.svg" alt="Unit Icons">
    </div>
    </header>  
   
    </div>
    
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.hero-layout{
   
  .hero-header{
    display: flex;
    justify-content: space-between;
    align-items: center;     
  }
  .hero-right{
    gap: 10px;
  }
  .flex-center {
  display: flex;
  align-items: center;
}

}
</style>