<template>
  <div class="event" :class="{ show: isOpen }">
    <p>{{ text }}</p>
    <button @click="isOpen = false">x</button>
  </div>
</template>

<script>
export default {
  name: "EventComponent",
  props: {
    text: String,
  },
  data() {
    return {
      isOpen: true,
    };
  },
};
</script>

<style>
.event {
  background-color: #444;
  color: #fff;
  padding: 10px 20px;
  text-align: center;
  font-size: small;
  display: flex;
  justify-content: space-between;
  align-items: center;
  display: none;
}

.show {
  display: flex;
}

.event p {
  margin: 0;
}

.event button {
  margin: 0;
}
</style>
