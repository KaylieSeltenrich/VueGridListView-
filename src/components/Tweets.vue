<template>
  <div>
   <button id="toggle" type="button" @click="isList = !isList, isGrid = !isGrid"> Click Here To Change View! </button>
    <div id="container" :class="{ grid: isGrid, list: isList }">
    <div id="tweet-container" v-for="allTweet in allTweets" v-bind:key="allTweet"> 
    <h3 id="user-tweet"> {{ "'"+ allTweet.userTweet + "'" }} </h3>
    <h3 id="user-name"> {{ allTweet.userName }}  </h3>
    <h3 id="date-created"> {{ allTweet.dateCreated }} </h3>
    </div>
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
          dateCreated: "9/18/2020 ",
          },

        { userTweet: "I can't wait for the weekend.",
          userName: "IHateMondays",
          dateCreated: "9/18/2020",
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
          dateCreated: "9/16/2020",
          },

           { userTweet: "Tweet Tweet",
          userName: "Birb",
          dateCreated: "9/15/2020 ",
          },

          
       
        ],
       
    isGrid: false,
    isList: true,
}
}
}


</script>

<style>
#user-tweet {
    font-size: 2em;
    margin: 5%;
    color: grey;
}

#tweet-container {
    border: 2px solid black; 
    margin: 5%;
    padding: 5%;
    width: 80%;
}

.grid {

display: grid;
justify-items: center;
align-items: center;
grid-template-columns: 1fr 1fr;



}

.list {
    display: block;
    text-align: center;
    padding: 2%;
    
   
  
}

.list #user-tweet {
  font-size: 3em;
  
}

.list #user-name, #date-created {
  font-size: 2em;
  
}

#toggle {
  
  width: 80%;
  height: 10%;
  font-size: 1.5em;
}

</style>
