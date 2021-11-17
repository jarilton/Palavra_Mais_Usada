<template>
  <div>
      <v-container fluid>
          <div class="pills">
              <Pill v-for="word in groupedWords" :key="word.name"
                :name="word.name" :amount="word.amount" />
          </div>
      </v-container>
  </div>
</template>

<script>
import Pill from './Pill.vue'

export default {
    components: { Pill },

    data: function() {
        return {
            groupedWords: [
                { name: 'i', amount: 1234},
                { name: 'you', amount: 900},
                { name: 'he', amount: 853},
                { name: 'i', amount: 1234},
                { name: 'you', amount: 900},
                { name: 'he', amount: 853},
                { name: 'i', amount: 1234},
                { name: 'you', amount: 900},
                { name: 'he', amount: 853},
                { name: 'i', amount: 1234},
                { name: 'you', amount: 900},
                { name: 'he', amount: 853},
            ]
        }
    }
}
</script>

<style>
    .pills {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }
</style>