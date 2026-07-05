<template>
  <section id="about" class="container">
    <h1>About</h1>
    <div class="row gx-5">
      <figure class="col-md-6">
        <img src="../assets/images/profile.jpg" alt="" />
        <figcaption>About Yeon jung</figcaption>
      </figure>
      <p class="col-md-6">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae temporibus
        quam placeat dolores quas nemo doloremque error laborum. Laboriosam,
        asperiores? Voluptatibus similique qui minima eius esse doloremque
        consequatur, tenetur totam.
      </p>
    </div>

    <article class="row mt-5">
      <h2>Skills</h2>
      <dl>
        <div v-for="item in skills" :key="item.id">
          <dt class="lead">{{ item.name }}</dt>
          <dd>
            <div class="progress" role="progressbar">
              <div class="progress-bar" :style="{ width: item.point }"></div>
            </div>
          </dd>
        </div>
      </dl>
    </article>
  </section>
</template>

<script setup>
const skills = [
  { name: "HTML", point: "90%", id: 1 },
  { name: "CSS", point: "80%", id: 2 },
  { name: "JAVASCRIPT", point: "50%", id: 3 },
  { name: "VUE", point: "75%", id: 4 },
];
</script>

<style lang="scss">
figure {
  img {
    width: 100%;
  }
}
</style>
