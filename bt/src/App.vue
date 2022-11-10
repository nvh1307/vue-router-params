<template>
  <div>
    <h1>Bài Vue 3101</h1>
    <label for="">Họ Tên: </label> <input v-model="user.name" type="text" name="" id=""> <br>
    <label for="">Giới Tính: </label>
    <label for="">Nam</label> <input v-model="user.sex" :value="true" type="radio" name="sex" id=""> 
    <label for="">Nữ</label> <input v-model="user.sex" type="radio" name="sex" id="">
    <br>
    <label for="">Giới Thiệu Bản Thân: </label> <textarea v-model="user.mys" name="" id="" cols="20" rows="5" ></textarea>
    <br>
    <label for="">Email: </label> <input v-model="user.email" type="text" name="" id=""> <br>
    <label for="">Tuổi: </label> <input v-model="user.age" type="number" name="" id=""> <br>
    <button @click="clickButton">Submit</button>
    <div v-if="isSubmitted">
      <h1>Tên: {{user.name}}</h1>
      <h1> Giới Tính: {{user.sex?"Nam":"Nữ"}}</h1>
      <h1>Giới Thiệu Bản Thân: {{user.mys}}</h1>
      <h1>Email: {{user.email}}</h1>
      <h1>Tuổi: {{user.age}}</h1>
    </div>
  </div>
</template>

<script>


export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      user:{
        name:'',
        sex: null,
        mys:'',
        email :'',
        age : null,
      },
      isSubmitted : false
    }

  },
  methods: {
    clickButton(){
      this.isSubmitted = true;
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
  padding: 5px;
}
</style>
