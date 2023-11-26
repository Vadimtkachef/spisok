<script>
  export default{
    data(){
      return{
        name: "",
        age: 18,
        list: [],
      }
    },
   /* methods:{
      sayHello(){
        this.list.push(this.name);
        alert(this.list[this.list.length-1]);
        console.log(this.list);
      }
    }*/

  }

</script>
 
<template>
  <p class="spis">СПИСОК ДЕЛ</p>
  <h1 class="delo"><p class="delo1">ДЕЛО:</p> {{ name==''?'....................':name }} </h1>
  <input class="inp" type="text" v-model="name"> <br>
  <button class="btn" v-if="name==''" disabled>Введи дело</button>
  <button class="btn1" v-else @click="$event => sayHello()">ДОБАВИТЬ В СПИСОК</button>
  <h3 class="text5">ВВЕДЕННЫЕ В СПИСОК ДЕЛА</h3>
  <ol class="text6">
    <li v-for="item in list">
    {{ 
      item
    }}</li>
  </ol>

</template>

<style scoped>
.spis{
  text-align: center;
  padding-bottom: 70px;
  color: #0f0f63e9;
  font-size: 60px;
  text-shadow: 0.1em 0.1em 0.1em #212121;
  font-weight: bold;
}
.delo1{
  text-align: center;
  padding-bottom: 30px;
  font-size: 30px;
  color: #970d57e9;  
}
.delo{
  text-transform: uppercase;
  text-align: center;
  padding-bottom: 30px;
  font-size: 30px;
}
.inp{
  display: block;
  margin:0 auto;
}
.btn{
  display: block;
  margin:0 auto;
}
.btn1{
  display: block;
  margin:0 auto;
  border-radius: 20px;
  color: #180a0a; 
  background: rgb(212,75,56); 
  padding: 13px 14px; 
  font-weight: 900;
} 
.btn1:hover { background: green; }  
.btn1:active { background: yellow; }  
.text5{
  text-align: center;
  padding-bottom: 30px;
  font-size: 30px;
  color: #970d57e9;  
}
.text6{
  text-align: center;
  padding-bottom: 30px;
  font-size: 30px;
  color: black;  
  font-style: italic;
}
</style>





