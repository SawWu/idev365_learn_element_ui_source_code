<template>
  <div id="app">
    <div class="demo-input">
      <h1>{{input}}</h1>
      <c-row>
        <c-input v-model="input" placeholder="请输入内容" @input="handleChangeInput"/>
      </c-row>
      <c-row>
        <c-input disabled v-model="input" placeholder="请输入内容"/>
      </c-row>
    </div>
  </div>
</template>

<script>
import CInput from './../components/CInput.vue'
import CRow from './../components/CRow.vue'

export default {
  name: 'InputExample',
  data:function(){
    return {
      input:"Hello Input",
    }
  },
  components: {
    CInput,
    CRow,
  },
  methods:{
    handleChangeInput:function(val){
      console.log("handleChangeInput-->",val)
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.demo-input{
  .c-row{
    margin-bottom: 20px;
  }
  .c-input{
    width:180px;
  }
}
</style>
