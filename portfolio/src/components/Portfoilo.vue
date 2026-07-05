<template>
  <section id="portfolio" class="container">
    <h1>Portfolio</h1>
    <ul class="list row">
      <li v-for="prac in data" :key="prac.id" class="col-md-4">
        <img :src="prac.imgUrl" alt="1" />
        <h3>{{ prac.title }}</h3>
        <p>{{ prac.desc }}</p>
        <router-link :to="'/detail/' + prac.id">상세보기</router-link>
      </li>
    </ul>
  </section>
</template>

<script setup>
const props = defineProps({
  data: Array,
});
console.log(props);
</script>

<style lang="scss">
#portfolio {
  h1 {
    margin-bottom: 1rem;
  }
  .list {
    list-style-type: none;
    padding: 0;

    li {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      margin-bottom: 10vh;
      img {
        width: 100%;
        aspect-ratio: 16/9;
        object-fit: cover;
        object-position: top;
      }
      h4 {
        margin-top: 1rem;
      }
    }
  }
}
</style>
