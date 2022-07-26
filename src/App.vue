<template>

    <div>
    
      <h2 v-text="msg" ref="studentmsg"></h2>
      <button @click="showDom">点我输出上面的DOM元素</button>
        <Student ref="studentRef"></Student>
    </div>
  
 
</template>

<script>
import Student from "./components/Student.vue";

export default {
  name: "App",
  components: {
    Student
  },
  data () {
    return {
      msg:'hello!Vue'
    }
  },
  methods: {
    showDom(){
      console.log(this.$refs.studentmsg) //真实的标签的DOM元素
      console.log(this.$refs.studentRef) //组件的实例对象
    }
  }
};
</script>

