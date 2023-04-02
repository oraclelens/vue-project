<template>
    <div>
      <div class="stancelebs">
        <h2 class="name">{{ name }}</h2>
        <img :src="image" alt="middle-aged celeb" />
        <button @click="noescape">Unstan Celeb</button>
      </div>
    </div>
  </template>
  
  <script>

  export default {
    name: "StanCard",
    props: {
      name: String,
      image: String,
    },
    data() {
      return {
        stancelebs: true,
      };
    },
    components: {
    },
    methods: {
        noescape(){
            alert("THERE'S NO GOING BACK NOW")
        }
    },
  };
  </script>
  
  <style scoped>
  .stancelebs {
    background-color: rgb(74, 134, 142);
    text-align: center;
    padding: 15px;
    margin: auto;
    margin-bottom: 30px;
    border-radius: 50px;
    width: 250px;
    margin-top: 20px;
  }
  img {
    width: 150px;
    border-radius: 50%;
  }
  h2 {
    font-size: 2vh;
  }
  .name {
    font-weight: bold;
    font-size: 2.5vh;
  }
  button {
  width: 200px;
  font-size: 15px;
  border: 10px white;
  border-radius: 50px;
  background-color: rgb(255, 255, 255);
  color: rgb(47, 85, 90);
  height: 50px;
  margin: auto;
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
  