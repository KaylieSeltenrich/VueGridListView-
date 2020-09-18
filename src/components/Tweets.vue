<template>
  <div id="container" :class="{ grid: isGrid, list: isList }">
    <button id="toggle" type="button"> Click here to change view </button>
    <div id="tweet-container" v-for="allTweet in allTweets" v-bind:key="allTweet"> 
    <h3 id="user-tweet"> {{ "'"+ allTweet.userTweet + "'" }} </h3>
    <h3 id="user-name"> {{ allTweet.userName }}  </h3>
    <h3 id="date-created"> {{ allTweet.dateCreated }} </h3>
     </div>
  </div>
</template>

<script>

export default {
  

 data: function() {

    return {
       
     
       allTweets: [
         

         { userTweet: "Hello World!",
          userName: "CoolUser",
          dateCreated: "9/17/2020 ",
          },

        { userTweet: "I can't wait for the weekend.",
          userName: "IHateMondays",
          dateCreated: "9/17/2020",
          },

        { userTweet: "I really like dogs.",
          userName: "DogLover",
          dateCreated: "9/17/2020",
          },

       { userTweet: "Zzzz...",
          userName: "SleepyCoder",
          dateCreated: "9/17/2020",
          },

        { userTweet: "WEEEE!",
          userName: "CaffinatedCoder",
          dateCreated: "9/17/2020",
          },
          
       
        ],
       
}
}
}


</script>

<style>
#user-tweet {
    font-size: 1.5em;
    margin: 5%;
    color: grey;
}

#tweet-container {
    border: 2px solid black; 
    margin: 5%;
}

.grid {

display: grid;
justify-items: center;
align-items: center;
grid-template-columns: repeat(2,1fr);

}

.list {
    display: block;
    text-align: center;
}

</style>
