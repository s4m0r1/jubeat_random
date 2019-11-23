
<template>
  <h1>{{ env_1 }}</h1>
</template>

<script>
export default {
  data() {
    console.log(process.env.SONGJSONURL)
    return {
      env_1: process.env.SONGJSONURL,
      // env_2: process.env.SONGJSONURL
    }
  }
}
</script>
