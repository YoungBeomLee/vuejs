<template>
  <div>
    <h1 :class="red">{{ name }}</h1>
  </div>
  <input type="text" :value="name" />
  <button class="btn btn-primary" @:click="updateName">버튼</button>
</template>

<script>
//원시타입 임포트
import { ref } from "vue";
export default {
  setup() {
    let red = ref("red");
    const name = ref("김망고");
    const updateName = () => {
      name.value = "회원님";
      red.value = "green";
    };
    return { name, updateName, red };
  },
};
</script>

<style>
.red {
  background-color: red;
}
.green {
  background-color: green;
}
</style>