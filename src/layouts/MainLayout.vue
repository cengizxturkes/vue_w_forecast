<template>
  <main>
    <slot />
  </main>
  <div class="main">
    <div class="main-title">
      <h2 class="text-preset-2">How’s the sky looking today?</h2>
    </div>
    <div class="search-row">
      <div class="search-input-wrapper">
        <div class="search-input-icon">
          <img src="../assets/images/icon-search.svg" alt="" />
        </div>
        <div class="search-input">
          <input
            type="text"
            placeholder="Search for a place..."
            class="text-preset-5"
          />
        </div>
      </div>

      <div class="search-button">
        <button class="btn">
          <h1 class="text-preset-5">Search</h1>
        </button>
      </div>
    </div>
    <div class="weather-info">
      <div class="weather-info-card">
        <img src="../assets/images/bg-today-large.svg" alt="" />
        <div class="weather-info-row">
          <div class="weather-text">
            <h2 class="text-preset-4">Berlin, Germany</h2>
            <h3 class="text-preset-6">Berlin, Germany</h3>
          </div>
          <div class="yan">
            <div class="weather-icon">
              <img
                src="../assets/weather-app-main/assets/images/icon-sunny.webp"
                alt=""
              />
            </div>
            <div class="weather-city-info">
              <h2 class="text-preset-1">20°</h2>
            </div>
          </div>
        </div>
      </div>
      <div class="hourly-weather-card">
      <div class="hourly-forecast-card">
        <div class="text">Hourly forecast</div>
        <div class="dropdown-forecast">
          <div class="text">Tuesday</div>
          <img src="../assets/images/icon-dropdown.svg" alt="" width="12px" height="18px">
        </div>
      </div>
      <div class="hourly-forecast-container"
      v-for="(item,index) in 8" :key="index"
      >
        <div class="hourly-forecast-container-left">
        <img src="../assets/images/icon-sunny.webp" alt="" width="40px" height="40px" >
        <h1 class="text-preset-5">{{index+1}} PM</h1>
      </div>
        <h1 class="text-preset-7">20 *</h1>

      </div>
      </div>
    </div>
    
  </div>
</template>

<script>
export default {};
</script>

<style>
.hourly-forecast-container-left{
  display: flex;
  justify-content:start;
  gap: 8px;
  align-items: center;
}
.hourly-forecast-container{
  max-width: 336px;
  max-height: 60px;

  height: 100%;
  width: 100%;
  background-color: var(--clr-neutral-700);
  border-radius: 8px;
  display: flex;
  justify-content: space-between;
  align-content: center;
  align-items: center;
  margin-top: 16px;
  margin-bottom: 16px;

}
.hourly-weather-card{
  margin-left: 32px;
  padding-left: 32px;
  flex-grow: 1; 
  background-color: var(--clr-neutral-800);
  border-radius: 20px;
  max-width: 384px;
  max-height: 693px;
  height: 100%;
  width: 100%;
}
.dropdown-forecast{
  display: flex;
  flex-direction: row;
  gap: 12px;
  max-width: 120px;
  background-color: var(--clr-neutral-600);
  max-height: 37px;
  border-radius: 8px;
  align-content: center;
  align-items: center;
  padding: 8px 16px;
}
.hourly-forecast-card {
  display: flex;
  padding-right: 24px;
  flex-direction: row;
  margin-top: 24px;
  margin-bottom: 16px;
  justify-content: space-between;

  align-items: center;
}
.yan {
  display: flex;
  gap: 24px;
}
.weather-icon {
  max-width: 120px;
  
}
.weather-info-row-test {
  justify-content: space-between;
}
.weather-info-row {
  position: absolute;
  top: 50%;
  left: 24px;
  right: 24px;
  transform: translateY(-50%);
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.weather-info {
  display: flex;
  align-items:start;
  width: 100%;
  margin-top: 48px;

}
.weather-info-card {
  position: relative;
  height: 266px;
  max-width: 800px;
}
.weather-info-card img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 20px;
}

.search-button .btn {
  display: flex;
  height: 56px;
  border-radius: 12px;
  align-items: center;
  justify-content: center;
  color: white;
  background-color: var(--clr-blue-500);
  border: none;
  width: 114px;
  cursor: pointer;
}
.search-row {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: var(--spacing-16);
}
.main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.main-title {
  margin-top: var(--spacing-64);
  margin-bottom: var(--spacing-64);
}
.search-input {
  max-width: 526px;
}
.search-input-wrapper {
  align-items: center;
  display: flex;
  gap: var(--spacing-16);
  width: 526px;
  height: 56px;
  background-color: var(--clr-neutral-800);
  padding-left: var(--spacing-24);
  padding-right: var(--spacing-24);
  border-radius: 12px;
}
.search-input-icon {
  display: flex;
  width: 20px;
  height: 30px;
}

.search-input-wrapper input {
  border: none;
  outline: none;
  background: transparent;
  max-width: 526px;
  font-size: 20px;
  padding: 4px 0;
}
</style>
