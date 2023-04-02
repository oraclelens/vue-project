<template>
  <div class="cards">
    <h2 class="name">{{ name }}</h2>
    <img class="image" :src="image" alt="celeb.alt"/>
    <InfoButton @click='info = !info'>Description</InfoButton>
    <div v-show='info'> Top 3: {{description}}</div>
    <StanButton @click="test">Add to Your Stan List</StanButton>
  </div>
    
</template>

<script>
import { celebinfo } from './CelebInfo';
import InfoButton from './InfoButton.vue';
import StanButton from './StanButton.vue';

export default {
  name: "Card",
  props: {
    name: String,
    image: String,
    description: String,
    alt: String,
  },
  data() {
    return {
      info: false,
      celebinfo,
    };
  },
  components: {
    InfoButton,
    StanButton,
  },
  methods: {
    test() {
      this.celebinfo.celebs.push({
        name: this.name,
        image: this.image,
      });
      console.log(this.celebinfo.celebs);
    },
}
};
</script>

<style scoped>
.cards {
  width: 250px;
  background-color: rgb(74, 134, 142);
  text-align: center;
  padding: 15px;
  margin: auto;
  margin-bottom: 30px;
  border-radius: 20px;
  height: 500px;
  margin-left: 50px;
  margin-right: 50px;
  margin-top: 20px;
}
img {
  width: 170px;
  border-radius: 20px;
  height: 250px;
}
h2 {
  font-size: 3vh;
}
.desc {
  margin-top: 10px;
}
.name {
  font-weight: bold;
  margin-bottom: 5px;
}
</style>
