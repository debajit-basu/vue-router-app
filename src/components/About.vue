<template>
    <div>
        <h1>{{msg}}</h1>
    </div>
</template>
<script>
export default {
  name: 'About',
  data() {
      return {
          msg: 'Welcome to About Page'
      }
  }
}
</script>
<style scoped>
    h1 {
        color: blue;
       }
</style>
