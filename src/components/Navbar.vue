<template lang="">
     <nav class="navbar navbar-expand-sm" style="border-bottom: 1px solid gray">
      <div class="container-fluid">
        <h2 class="logo" @click="gohome()" >Anlat</h2>
      </div>
      <div style="display: flex; background: ; align-items: center">
  <!--    <i class="fa-regular fa-bell"></i>
        <i class="fa-regular fa-comment-dots"></i>
-->  
        <button
          type="button"
          style="
            align-items: center;
            display: flex;
            background: white;
            border: grey 0.5px solid;
          "
          class="btn btn-warning me-5"
        >
          <i class="fa-regular fa-user"></i> {{name}}
          <i class="fa-solid fa-angle-down" style="color: gray;"></i>        </button>
      </div>
    </nav>
</template>
<script setup>
import { defineProps } from 'vue';
import { useRouter } from 'vue-router';


const props = defineProps({
  name: String,
});


const router = useRouter() 

const gohome = () => {
    router.push({path: "/"})
}





</script>
<style scoped>
i {
  font-size: large;
  margin: 0px 15px;
}</style>
