<script setup lang="ts">
import Button from 'primevue/button'
import { ref } from 'vue';

const answer = ref('wait')
</script>

<template>
  <div>
    <div class="center">
      <img v-if="answer==='wait'" src="./assets/qq.jpg" width="500px" alt="">
      <img v-if="answer==='yes'" src="./assets/hh.jpg" width="500px" alt="">
      <img v-if="answer==='no'" src="./assets/aaa.jpg" width="500px" alt="">
    </div>
    <div class="question">Are you love me?</div>
    <div class="center">
      <div class="buttons">
        <Button @click="answer='yes'" class="button"  :class="{'checked':answer==='yes'}" label="Yes"></Button>
        <Button @click="answer='no'" class="button" :class="{'checked':answer==='no'}" label="No"></Button>
      </div>
    </div>

  </div>
</template>

<style scoped>
.center {
  margin-top: 50px;
  display: flex;
  justify-content: center;
}

.question {
  font-size: 50px;
  font-family: cursive;
  text-align: center;
}

.buttons {
  width: 300px;
  display: flex;
  justify-content: space-between;
}

.button {
  background-color: #eb87be;
  padding: 20px 40px;
  border-radius: 10px;
  cursor: pointer;
}
.button:hover {
  opacity: 0.7;
}
.checked {
  background-color: #44ac3ac7;
}
</style>
