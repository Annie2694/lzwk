<template>
  <div id="app">
    <DetailPage></DetailPage>
    <List></List>
    <Button></Button>
  </div>
</template>

<script>
import DetailPage from '@/components/DetailPage'
import List from '@/components/List'
import Button from '@/components/Button'

export default {
  name: 'App',

  components: {
    DetailPage,
    List,
    Button
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
