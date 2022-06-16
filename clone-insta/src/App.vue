
<template>
  <div class="container">
    <h1>InstaClone - esd</h1>
    <div class="card-element" >
      <div v-for="post in postList" :key="post.id">
        <CardComponent :post="post" v-on:like="like"/>
      </div>
    </div>
  </div>
</template>

<script>
import CardComponent from './components/CardElement.vue';

export default {
  name: 'App',
  components: {
    CardComponent
  },
  data() {
    return {
      postList: [
        {
          "id": "1",
          "like": 0,
          "name": "Jason",
          "title": "J'adore vue.js",
          "content": "J'adore vue.js un super Framework",
          "imgUrl": "https://positivethinking.tech/wp-content/uploads/2021/01/Logo-Vuejs.png",
         "comment": "Pas fan perso",
         "commentCount": "1",
          "commentName": "John",
        },
        {
          "id": "2",
          "like": 0,
          "name": "Mickael",
          "title": "LA PLAGE !",
          "content": "Une super belle plage",
          "imgUrl": "https://www.terre.tv/wp-content/uploads/2020/05/plus-belles-plages-cuba.jpg",
          "comment": "<3",
          "commentCount": "1",
          "commentName": "John",
        },
        {
          "id": "3",
          "like": 0,
          "name": "Stefen",
          "title": "Une photo de mes vaccances ?",
          "content": "Un superbe paysage",
          "imgUrl": "https://cdn.radiofrance.fr/s3/cruiser-production/2020/06/4573d0fa-8d7c-4617-bc3b-21a159cb0f1f/870x489_vacances.jpg",
          "comment": "J'adore",
          "commentCount": "1",
          "commentName": "John",

        },
        {
          "id": "4",
          "like": 0,
          "name": "Thomas",
          "title": "Hello World !",
          "content": "Bonjour tout le monde",
          "imgUrl": "https://i.ytimg.com/vi/cRt1LKOr2P8/maxresdefault.jpg",
          "comment": "Super photo !",
          "commentCount": "1",
          "commentName": "John",
        


          
        }
      ]
    }
  },
  methods: {
    like(post) {
      post.like++;
    }
  }
}
</script>


<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  display: flex;
  align-items: center;
  justify-content: center;
}
.card-element{
  align-items: center;
  justify-content: space-around;
  width: 100%;
}
h1{
  text-align: center;
}
</style>