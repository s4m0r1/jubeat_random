<template>

</template>


<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import { DataTable }
@Component({
  head: {
    title: '曲データ'
  },
  components: {
    ScoreTable: () => import('~/components/DataTable.vue')
  }
})
</script>
