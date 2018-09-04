<template>
<div class="card">
  <img class="card__avatar" src="@/assets/user.svg" alt="avatar"/>
  <div class="card__info">
    <span class="card__info--name"> Name : {{ item.name }} </span>
    <span class="card__info--age"> Age : {{ item.age }} </span>
    <span class="card__info--country"> Country : {{ item.country }} </span>
  </div>
</div>
</template>

<script>
export default {
  props: ['item'],
}
</script>
