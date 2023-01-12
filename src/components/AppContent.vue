<script>
export default {
  
}
</script>

<template lang="">
  <main>
    <div class="title"> -- Content gose here -- </div>
  </main>
</template>

<style lang="scss" scoped>
@use '../styles/generals.scss' as *;
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

  main {
    height: 100px;
    background-color: black;
    display: flex;
    align-items: center;
    justify-content: center;
    
    .title{
      color: white;
    }

}
</style>