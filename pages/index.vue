<template>
  <section class="container">
    <div>
      <div><img alt="Vue logo" width="200px" height="150px" src="./logo.png"></div>


      
      <h1 class="title">
        Welcome to House Plant Doctor
      </h1>
      <form v-on:submit.prevent="submitForm">
    <div>
      <label for="username">id: </label>
      <input id="username" type="text" v-model="username">
      </div>
    <div>
      <label for="password">pw: </label>
      <input id="password" type="password" v-model="password">
    </div>
    

    <router-link to="/StroedPlant" tag="button" type="submit">login</router-link>

    <!-- <button type="submit">login</button> -->
    <!-- <router-link to="/about" tag="button" type="submit">login</router-link> -->
  </form>
     <br/>
      <li> &copy;Copyright 2020. House Plant Doctor Inc. All Rights Reserved</li>
    </div>
  </section>
</template>

<script>
//import AppLogo from '~/components/AppLogo.vue'
import AppLogo from '~/components/AppLogo.vue'

import axios from 'axios';

export default {
  components: {
    AppLogo
  },
  data: function(){
    return {
      username: '',
      password: '',
    }
  },
  methods: {
    submitForm: function(){
      //console.log(this.username, this.password);
      //event.preventDefault();//form의 이동,새로고침을 막는 코드
      //
      if(this.username == "LEE" && this.password == "1234"){
        console.log(this.username, this.password,loading);
       //methods에서 data로 접근 하기 위해서는 this
      } 
      var url = 'https://jsonplaceholder.typicode.com/users';
      var data = {
        username: this.username,
        password : this.password
      } 
      axios.post(url, data)//브라우저에서 서버로 데이터를 주고 받기 위한 라이브러리_post는 데이터를 생성하거나 조작하기 위한 
       .then(function(response){
         console.log(response);
       })
       .catch(function(error) {
         console.log(error);
       });
       //window.open("https://google.com", "_blank"); 
    }
  }
}


</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
#p1 {background-color:hsl(120,100%,75%);}
h4 {
    margin: 25px 50px 75px 10px;
    }


ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
h2 {
 
  margin: 0 10px;
}
p {
 
  margin: 0 10px;
}
a {
  color: #42b983;
}


</style>

