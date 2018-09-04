<template>
<div class="App">
  <div class="header" >
    <span class="header__title"> User List </span>
    <span class="header__add-user" @click="handlePlusClick"> + </span>
  </div>

  <transition-group class="cards" name="fade" tag="div">
    <card v-for="(item, idx) in Data" :item="item" :key="idx" />
  </transition-group>
</div>
</template>

<script>
import Card from '@/components/card'
import Data from '@/assets/data'

export default {
  components: {
    Card
  },
  data() {
    return {
      Data
    }
  },
  methods: {
    handlePlusClick() {
      let cards = this.Data.slice()
      cards.push({
        'name': 'New User',
        'age': 100,
        'country': 'New Country'
      })
      this.Data = cards
    }
  }
}
</script>
