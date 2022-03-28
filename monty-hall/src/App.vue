<template>
  <div id="app">
    <h1>Problema de Monty Hall</h1>
    <Door number="1" :hasGift="false"/>
  </div>
</template>

<script>
import Door from './components/Door'

export default {
  name: 'App',
  components:{ Door }
}
</script>

<style>
*{
  box-sizing: border-box;
  font-family: "Montserrat", sans-serif;
}

body{
  background: linear-gradient(to right, rgb(21,153,87), rgb(21,87,153));
  color: #fff;
}

#app{
  align-items: center;
  display: flex;
  flex-direction: column;
}

#app h1 {
  background-color: #0004;
  border: 1px solid #000;
  padding: 20px;
  margin-bottom: 60px;
}

</style>
