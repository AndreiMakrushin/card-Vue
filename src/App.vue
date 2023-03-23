<script setup>
import Card from "./component/Card.vue"
import { ref } from "vue"
import datas from "./data.json"

const data = ref(datas)
</script>
<template>
  <div>
    <div class="container">
          <div class="parent">
            <Card :date="date" v-for="date in data" :key="date.id"/>
          </div>
      </div>
  </div>
</template>
<style lang="scss" setup>
@import url("https://fonts.googleapis.com/css2?family=Nunito:wght@200;500;700;800;900;1000&display=swap");

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: "Nunito", sans-serif;
}

body {
  background-color: #181a1f;
  padding: 0px 50px;
}

.container {
  padding: 50px 0px;
  height: 100vh;
  display: flex;
  gap: 50px;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
}
.parent {
  height: 400px;
  width: 300px;
  padding: 20px;
  perspective: 1000px;
}



.card2 {
  filter: hue-rotate(150deg);
}
.card3 {
  filter: hue-rotate(300deg);
}
.card4 {
  filter: hue-rotate(90deg);
}
</style>