<template>
  <div>
    <div>Selamat Datang {{ myText }}</div>
    <ul>
      <li v-for="item in todos">{{ item.desc}}</li>
      
    </ul>
    <input v-model="myText"/>
    <button @click="tambah">Add</button>
  </div>
</template>



<script>
export default{
  data : function(){
    return{
      todos : [
      {desc: 'Makan Durian' },
      {desc: 'Makan Pisang'},
      {desc: 'Coding JS'}
      ],
      myText: ''
    }
  },
  methods:{
    tambah : function(){
      this.todos.push({desc: this.myText})
    }

  }
}
</script>

