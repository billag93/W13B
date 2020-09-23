<template>
  <div id="container-grid" :class="{'grid-style':gridStyle}">
    <div :class="{'grid-card':gridStyle}" v-for="tweet in tweets" :key="tweet.tweet">
        <h2>{{tweet.author}}</h2>
        <p>{{tweet.tweet}}</p>
         <h2>{{tweet.date}}</h2>
    </div>
    <button v-if="gridStyle" @click="gridStyle=false">Switch to list</button>
    <button v-else @click="gridStyle=true">Switch to grid</button>
  </div>
</template>

<script>

export default {
  name: "page-body",
  components: {

  },

 
  methods: {

  },

  data: function () {
    return {
        gridStyle:false,
      tweets: [
        {
          author: "John",
          tweet:
            "My sex drive is a joy, and I want to wake up. It's better with specific love, again.",
          date: "2013/04/13",
        },
        {
          author: "Bill",
          tweet:
            "My dog is a shadow, and I want to get wasted. The world has backwards romances, please.",
          date: "2015/03/16",
        },
        {
          author: "Zelda",
          tweet:
            "My game is hard labor, and I want to buy a horse. Come for the slapstick fluff, in ALL CAPS.",
          date: "2017/02/21",
        },
        {
          author: "Sally",
          tweet:
            "My game is amazing, and I want to break free. A bit of awkward heroes, I say.",
          date: "2019/01/20",
        },
        {
          author: "Lisa",
          tweet:
            "My worst enemy is a thrill, and I want to change my name. A bit of miniscule trials, please.",
          date: "2014/09/11",
        },
        {
          author: "Kelly",
          tweet:
            "My best friend is fantastic, and I want to buy a horse. I'm depending on free romances, kinda.",
          date: "2020/05/19",
        },
        {
          author: "George",
          tweet:
            "My boss is hungry for more, and I want to drink beer. Let there be hot ambition, everywhere.",
          date: "2017/02/28",
        },
        {
          author: "Mike",
          tweet:
            "My job is really confusing, and I want to play hacky sack. Looking for hot weather, IMHO. ",
          date: "2018/11/20",
        },
        {
          author: "Peter",
          tweet:
            "My cat is so fragile, and I want to wake up. I'm depending on miniscule dates, kinda.",
          date: "2015/09/29",
        },
        {
          author: "Lara",
          tweet:
            "My ringtone is a fatal condition, and I want to break free. More lovely fruit, bro.",
          date: "2016/12/31",
        },
      ],
    };
  },
};
</script>

<style scoped>
#container-grid {
  display: grid;
}
.grid-style{
    display: grid;
    grid-template-columns:repeat(auto-fit, minmax(250px, 1fr));
    justify-items: center;
    align-items: center;
    border: 3px solid skyblue;
    box-shadow: 3px 6px 8px darkturquoise;
    column-gap: 8%;
}
.grid-card{
    
    border: 3px solid skyblue;
    box-shadow: 3px 6px 8px darkturquoise;
    column-gap: 8%;
}

</style>
