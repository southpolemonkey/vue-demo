<template>
   <div class="container">
      <!-- Eventually change to vue shorthand -->
     <h1 v-bind:class="{big: isBig }" v-on:click="isBig = !isBig">{{ msg }}</h1>
   </div>
</template>

<script>
export default {
  name: 'Feed',
  data() {
     return {
       posts: [
         {
            id: 1, title:"Google takes over world", body: "Big whoop."},
         {
            id: 2, title:"Bagels, Still great!", body: "Scientists say they are 'yummy'"
         }
       ],
       msg: "Welcome to the Vue-Demo!",
       isBig: false
     }
  },
  methods: {  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

/* sick transition too fam */
h1 {
   text-align: center;
   padding: 10px;
   margin: 0 auto;
   border: 10px solid transparent;
   user-select: none;
   cursor: pointer;
   transition: font-size 0.3s;
}

.line {
   border: 10px dotted red;
}

.big {
  font-size: 5em;
}
</style>
