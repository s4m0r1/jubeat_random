<template>
  <v-container>
  <p>{{ headers }}</p>
    <v-card>
        <v-card-title>
          <v-checkbox v-model="selected" color="red" label="TEST" value="{ text: 'EXTREME', value: 'EXT'}"></v-checkbox>
          <v-checkbox v-model="headers" color="red" label="TEST2" value="{ text: 'ADVANCE', value: 'ADV'}"></v-checkbox>
          <v-spacer></v-spacer>
          <v-text-field
            v-model="search"
            append-icon=""
            label="Search"
            single-line
            hide-details
          ></v-text-field>
        </v-card-title>
        <v-data-table
          :headers="headers"
          :items="song_list"
          :search="search"
          :loading="loading"
          loading-text="読込中"
          no-data-text="データがありません。"
          no-results-text="楽曲が見つかりません"
        ></v-data-table>
      </v-card>
  </v-container>
</template>

<script>
export default {
  asyncData() {
    return {
      song_list: require(`~/assets/song_list.json`)
    }
  },
  data () {
    return {
      search: '',
      headers: [
        {
          text: '曲名',
          align: 'left',
          sortable: true,
          value: '曲名',
        },
        { text: 'ジャンル', value: 'ジャンル'},
        { text: 'アーティスト', value: 'アーティスト'},
        { text: 'BPM', value: 'BPM'},
        { text: 'Version', value: 'Version'},
        { text: 'BASIC', value: 'BSC'},
        { text: 'EXTREME', value: 'EXT'}
      ]
    }
  }
}

</script>
