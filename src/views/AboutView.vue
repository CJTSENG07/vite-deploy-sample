<script setup>
import { inject } from 'vue'

const axios = inject('axios')
const url = import.meta.env.VITE_URL

const getData = () => {
  axios.get(url)
  .then((res) => {
    console.log(res.data)
  })
}
</script>

<template>


  <button type="button" @click="getData">click me</button>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
</template>


