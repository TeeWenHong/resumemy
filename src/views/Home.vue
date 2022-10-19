<template>
  <div class="home">
    <el-form ref="formRef" :rules="rules" :model="form" label-width="40px" class="input">
    <h1>你好老板！Hello Boss</h1>

      <el-form-item  prop="name" class="username">
        贵公司名称：<el-input v-model="form.name" class="laber" prefix-icon="el-icon-name" ></el-input>
      </el-form-item>

      <el-form-item  prop="email" class="username">
        邮箱：<el-input v-model="form.email" class="laber" prefix-icon="el-icon-user" ></el-input>
      </el-form-item>
      
      <el-form-item  prop="phone" class="username">
        电话：<el-input v-model="form.nember" class="laber" prefix-icon="el-icon-user" ></el-input>
      </el-form-item>

      <div class="username2">岗位:
        <el-select style=" width:410px" v-model="value" placeholder="请选择" prop="j" >
        <el-option
        v-for="item in form.options"
        :key="item.value"
        :label="item.label"
        :value="item.value">
        </el-option> 
      </el-select>
      </div>
      

      <!-- 提交按钮 -->
      <el-form-item class="button">
        <el-button type="primary" @click="loginCheck()">提交看简历</el-button>
      </el-form-item>

      <!-- 跳转按钮 -->
      <el-form-item class="button2">
        <el-button type="primary" @click="resumeCheck()">先看看简历</el-button>
      </el-form-item>
      

    </el-form>
 
    
    
  </div> 
</template>

<script>
export default {
  // el:"app",
  data() {
    return {
     form:{
       name:"hgg",
       email:"@gmail.com",
       nember:"01",
       job:"",
       options: [{
          value: '1',
          label: '前端web'
        }, {
          value: '2',
          label: '前端android',
        }, {
          value: '3',
          label: '后端'
        }, {
          value: '4',
          label: '数据库'
        }]
     },
     rules:{
      name:[
        {required:true,message:'请输入公司名称',trigger:'blur'},
        {min:3,max:20,message:'长度在3到20个字',trigger:'blur'}
      ],
      email:[
        {required:true,message:'请输入联系邮箱',trigger:'blur'},
        {min:3,max:20,message:'长度在3到20个字',trigger:'blur'}
      ],
      phone:[
        {required:true,message:'请输入联系号码',trigger:'blur'},
        {min:6,max:12,message:'长度在6到12个字',trigger:'blur'}
      ]
     }
      // options: [{
      //     value: '选项1',
      //     label: '前端web'
      //   }, {
      //     value: '选项2',
      //     label: '前端android',
      //   }, {
      //     value: '选项3',
      //     label: '后端'
      //   }, { 
      //     value: '选项4',
      //     label: '数据库'
      //   }]
    }
  },
  methods:{
    resumeCheck(){
    this.$router.push("./resume")
    },
    loginCheck(){
      this.$refs.formRef.resetFileds();
    }
  },
  // el:'',
  // data() {
  //   return{

  //   }
  // }
  
}  
</script>

<style>
  html, body{
        margin: 0;
        padding: 0;
    }

.button{
  position:absolute;
  top: 85%;
  left: 15%;
}

.button2{
  position:absolute;
  top: 85%;
  left: 50%;
}

.home{
  background-color: aqua;
  max-width: 1500px;
  min-width: 600px;
  min-height: 770px;
  max-height: 1000px;
  background-image: url(./img/002.jpg);
  background-repeat: no-repeat;
  background-size: 100% 100%;
}

.input{
  background-color: antiquewhite;
  max-height: 510px;
  max-width: 500px;
  min-width: 510px;
  min-height: 500px;
  transform: translate(-40%,-50%);
  position:absolute;
  left:50%;
  top:50%;
  border-radius: 15px;
}

.username{
  /* background-color: aqua; */
  height: 60px;
  width: 450px;
}
.username2{
  /* background-color: aqua; */
  height: 60px;
  width: 400px;
  position:absolute;
  left: 40px;
  top:340px;
}

</style>

