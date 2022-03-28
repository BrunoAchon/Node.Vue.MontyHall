<template>
  <div class="gift">
      <div class="gift-top"></div>
      <div class="gift-body"></div>
      <div class="gift-tie-1"></div>
      <div class="gift-tie-2"></div>
  </div>
</template>

<script>
export default {
    name:"gift-winner"
}
</script>

<style>

.gift {
    align-items: center;
    display: flex;
    flex-direction: column;
    position: relative;
    z-index: 10;
}

.gift-top {
    background-color: #7aa944;
    border: 1px solid #000;
    height: 25px;
    width: 100px;
}

.gift-body {
    background-color: #5c7e32;
    border-left: 1px solid #000;
    border-right: 1px solid #000;
    border-bottom: 1px solid #000;
    height: 60px;
    width: 90px;
}

.gift-tie-1{
    background-color: red;
    position: absolute;
    top:1px;
    height: 82px;
    width: 15px;
}

.gift-tie-2{
    background-color: red;
    position: absolute;
    height: 15px;
    top:40px;
    width: 88px;
}

</style>