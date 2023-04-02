<script>
import Card from "../components/Card.vue";
import { celebinfo } from "../components/CelebInfo";
import InfoButton from "../components/InfoButton.vue";
import StanButton from "../components/StanButton.vue";
import StanCard from "../components/StanCard.vue";

export default {
  name: "Menu",
  components: {
    Card,
    InfoButton,
    StanButton,
    StanCard
  },
  methods: {},
  data() {
    return {
      celebinfo,
      celebs: [
        {
          name: "Pedro Pascal",
          image:
            "http://t2.gstatic.com/licensed-image?q=tbn:ANd9GcQ0J-v8aL74WAGRA_V-FzIjqb48BvypcCItwwdR_4Lam3LuJeskH-5wcB5DhfZkCQY7MXp8tgKwSY5uQLc",
          description:
            "Last of Us, Narcos, Mandalorian",
          alt: "celebrity Pedro Pascal"
        },
        {
          name: "Charlize Theron",
          image:
            "https://assets.vogue.com/photos/63fe3e7c9892a562495febab/master/w_1600%2Cc_limit/GettyImages-1470252414.jpg",
          description:
            "The Old Guard, Atomic Blonde, Monster",
          alt: "celebrity Charlize Theron"
        },
        {
          name: "Sarah Paulson",
          image:
            "https://media.vanityfair.com/photos/57fe47016d65c9f44d47fdcb/master/w_2560%2Cc_limit/sarah-paulson-richard-lawson-interview.jpg",
          description:
            "American Horror Story, Ocean's 8, Ratched",
          alt: "celebrity Sarah Paulson"
        },
        {
          name: "Tom Hiddleston",
          image:
            "https://flxt.tmsimg.com/assets/286678_v9_bc.jpg",
          description:
            "Thor Trilogy, Crimson Peak, High-Rise",
          alt: "celebrity Tom Hiddleston"
        },
        {
          name: "Oscar Isaac",
          image:
            "https://flxt.tmsimg.com/assets/493617_v9_bc.jpg",
          description:
            "Moon Knight, Spiderverse, Star Wars",
          alt: "celebrity Oscar Isaac"
        },
        {
          name: "Jessica Chastain",
          image:
            "https://pro2-bar-s3-cdn-cf.myportfolio.com/f9be8da2d0dd9acf5f93d4976c0d2045/1178758460c70fc1119b8e05_rw_600.jpg?h=252b5b1aebb3d1fbaf4ad9263fec8f17",
          description:
            "The Martian, Miss Sloane, Crimson Peak",
          alt: "celebrity Jessica Chastain"
        },
        {
          name: "Cate Blanchett",
          image:
            "https://m.media-amazon.com/images/M/MV5BMTc1MDI0MDg1NV5BMl5BanBnXkFtZTgwMDM3OTAzMTE@._V1_.jpg",
          description:
            "Thor: Ragnarok, Carol, Ocean's 8",
          alt: "celebrity Cate Blanchett"
        },
        {
          name: "Angela Bassett",
          image:
            "https://api.time.com/wp-content/uploads/2023/02/2023-women-of-the-year-angela-bassett.jpg",
          description:
            "Black Panther, American Horror Story, What's Love Got to Do with It",
          alt: "celebrity Angela Bassett"
        },
      ],
    };
  },
};
</script>

<template>
  <div class="fortnite">
    Stan List:
    <StanCard
          v-for="celeb in celebinfo.celebs"
          :key="celeb.name"
          :name="celeb.name"
          :image="celeb.image"
        />
  </div>
  <main>
    <div class="celebcards">
      <Card
        v-for="celeb in celebs"
        :key="celeb.name"
        :name="celeb.name"
        :image="celeb.image"
        :description="celeb.description"
      />
    </div>
  </main>
</template>

<style scoped>
.celebcards{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}
* {
  color: white;
}
h3 {
  font-size: 2.5vh;
  font-weight: bold;
}
.fortnite{
  background-color: white;
  width: 400px;
  margin: auto;
  padding: 20px;
  margin-top: 15px;
  border-radius: 30px;
  color: rgb(74, 134, 142);
  text-align: center;
  font-size: 3vh;
  font-weight: bold;
}
</style>
