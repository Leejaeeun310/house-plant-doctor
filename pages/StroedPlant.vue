<template>

<div class="about">
      <div><img alt="Vue logo" width="200px" height="150px" src="./logo.png"></div>
    <!-- <div><img alt="Vue logo" width="200px" height="150px" src="./logo.png"></div> -->
    <br/> 
  
    <router-link to="/StroedPlant" tag="button"><p id="p1"><span style=" font:  bold 1.5em/1em Georgia, serif ;">
    STORED PLANT</span></p></router-link>
    <li><router-link to="/About" tag="button"><span style=" font:  bold 1.5em/1em Georgia, serif ;">
    ABOUT US</span></router-link></li>
   
    <br/> 


<div><img alt="Vue logo" width="200px" height="150px" src="./normal/1.png"></div>

<div><img alt="Vue logo" width="200px" height="150px" src="./normal/2.png"></div>
<div><img alt="Vue logo" width="200px" height="150px" src="./normal/3.png"></div>
<div><img alt="Vue logo" width="200px" height="150px" src="./normal/4.png"></div>


<ul v-for='item in items' v-bind:key='item'>
    <!-- <img v-bind:src="'./normal/' + item + '.png'" v-bind:alt="item">
    <div><img alt="Vue logo" width="200px" height="150px" src=item></div> -->
    {{ item.message }}
   

</ul>

    
</div>

</template>
<script>

var i = 0;
export default {
    

 data: function() {
    for(i=0;i<5;i++){
        i +=i;
    }
    
    return {
        items: [

      { message: i },
      { message: 'text' },
     
    ]
  };
}
    
};

</script>
<style>
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
}</style>
