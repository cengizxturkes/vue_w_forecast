<template>
    <main>
        <slot/>
    </main>
    <div class="main">
    <div class='main-title'>
      <h2 class="text-preset-2"> How’s the sky looking today?</h2>
    </div>
    <div class="search-input-wrapper ">
        <div class="search-input-icon">
        <img src="../assets/images/icon-search.svg" alt="">
    </div >
    <div class="search-input">
        <input type='text' placeholder="Search for a place..." class="text-preset-5">
    </div>

    
    </div>
</div>
</template>

<script>
export default {

}
</script>

<style>
.main{
    display: flex;
  flex-direction: column;
  align-items: center; 
}
.main-title{
  margin-top: var(--spacing-64);
  margin-bottom: var(--spacing-64);
}

.search-input-wrapper{
    align-items: center;   
    display: flex;
    gap:var(--spacing-16) ;
    width: 526px;
    height: 56px;
    background-color: var(--clr-neutral-800);
    padding-left: var(--spacing-24);
    padding-right: var(--spacing-24);
    border-radius: 12px;

}
.search-input-icon
{
    display: flex;
    width: 20px;
    height: 30px;
}

.search-input-wrapper input {
    
  border: none;            
  outline: none;           
  background: transparent; 
  flex: 1;                 
  font-size: 20ğx;
  color: var(--clr-neutral-800);
  padding: 4px 0;
}
</style>