<template>
    <button><slot></slot></button>
</template>

<script>
    export default {
        name: "InfoButton",
    data() {
    return {};
    },
    props: {
    name: String,
    description: String,
    },
    methods: {},
    }
</script>

<style scoped>
button {
  width: 200px;
  font-size: 15px;
  border: 10px white;
  border-radius: 50px;
  background-color: rgb(255, 255, 255);
  color: rgb(47, 85, 90);
  height: 50px;
  margin-top: 10px;
  transition: 0.5s;
  margin-bottom: 10px;
  cursor: pointer;
}
button:hover {
  transform: scale(1.1);
}
button:active {
  transform: scale(0.9);
}
</style>