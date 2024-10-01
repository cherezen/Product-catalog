<template>
  <div class="header">
    <div class="container">
      <nav class="header__nav">
        <button class="header__button">
          <span class="header__button-icon"></span>
          Новосибирск
        </button>
      </nav>
    </div>
  </div>
</template>

<style scoped>
.header {
  padding: 14px;
  width: 100%;
  box-shadow: 0px 2px 4px 0px #2727271A;
  background-color: #FFFFFF;
}
.header__nav {
  display: flex;
}
.header__button {
  font-size: 15px;
  color: #272727;
  display: flex;
  align-items: center;
  column-gap: 6px;
  border: none;
  background-color: transparent;
  cursor: pointer;
  padding: 10px 20px;
  margin-left: -20px;
}
.header__button-icon {
  display: block;
  width: 11px;
  height: 16px;
  background-image: url('@/assets/place-icon.svg');
  background-position: center center;
  background-size: auto;
  background-repeat: no-repeat;
}
.container {
  width: 1150px;
  margin: 0 auto;
}
</style>