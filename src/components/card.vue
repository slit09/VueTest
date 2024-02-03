<template>
  <div class="rows">
    <slot>   </slot>

    <div class="row g-3">
      <div class="col-auto">
        <label for="inputName" class="visually-hidden">Название</label>
        <input  type="text"  v-model="part.PName" class="form-control" id="inputName" placeholder="Название">
      </div>
      <div class="col-auto">
        <label for="inputPrace" class="visually-hidden">Цена за шт</label>
        <input  type="text" v-model="part.Price" class="form-control" id="inputPrace" placeholder="Цена за шт">
      </div>
      <div class="col-auto">
        <label for="inputVolume" class="visually-hidden">Кол - во</label>
        <input  type="text" v-model="part.PVolume" class="form-control" id="inputVolume" placeholder="Кол - во">
      </div>
      <div class="col-auto">
        <button v-on:click="added" class="btn btn-primary mb-3">Добавить</button>
      </div>
    </div>

<button v-on:click="show" class="btn btn-primary mb-3">Посмотреть результат</button>

  <div v-if="check" class="row">
    <ul id="array-rendering">
      <li v-for="item in product" :key="item" >
        {{  item.PName }} <br/>
        {{  item.Price }} <br/>
        {{  item.PVolume }} <br/>


      </li>
    </ul>
  </div>

  </div>
</template>

<script>
/* eslint-disable */
import Product from './Product.js'
export default {
  name: 'card',
  props: {
    msg: String
  },
  data(){
    return{
      product:[],
      part: Product,
      check : false,
      
    }
  },
  methods:{
    added(){
      this.product.push({...this.part})
    },
    show(){
      this.check = !this.check
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
