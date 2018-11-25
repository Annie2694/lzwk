<template>
  <div id="app">
    <DetailPage></DetailPage>
  </div>
</template>

<script>
import DetailPage from '@/components/DetailPage'

export default {
  name: 'App',

  components: {
    DetailPage
  }
}
</script>

<style>
body {
  margin: 0;
  background-color: #f8f8f8;
}
div {
  box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
#app {

}
</style>
