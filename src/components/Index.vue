<template>
  <div>
    <v-header></v-header>
    <v-navigate></v-navigate>
  </div>
</template>
<script>
import header from '../views/Header'
import navigate from '../views/Navigate'
export default {
  components: {
    'v-header': header,
    'v-navigate': navigate,
  }
}

</script>
