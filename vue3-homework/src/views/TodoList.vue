<template>
  <div>
    <h3>할일 리스트</h3>
    <input type="text" v-model="newTodo">
    <button type="button" @click="addlist()">추가</button>
    <hr>
    <ul>
      <li v-for="(n,index) in listzip" :key="index">
        {{index+1}}. {{n}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data(){
    return {
      listzip : ["vue 공부하기","Spring 공부하기","게임하기"],
      newTodo : ""
    
    }
  },
  methods: {
    addlist(){
      this.listzip.push(this.newTodo);
      this.newTodo="";
    }
  },
}
</script>