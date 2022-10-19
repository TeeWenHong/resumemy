<template>
  <div class="resume">
    <div class="body_info">
      <div class="main_info" >
        <h1>我的简历</h1>
          <div class="img_class"><img class="my_img" src="./img/img.jpg" ></div>
          <div class="main">
             <p>姓名：郑文鸿（TeeWenHong）</p>
             <p>年龄：25</p>
             <p>性别：男</p>
             <p>学历：武汉大学（软件工程）</p>
             <p>
              ---------------------------------------------               
             </p>
          </div>
          <div class="main2">
              <h2>联系方式</h2>
              <p>电话号码：016-920-3983</p>
              <p>邮箱：gqinjia55@gmail.com</p>
              <h5>注：如有任何问题请使用whatapp联系，电话接通不到谢谢您</h5>
              <p>
                  ---------------------------------------------
              </p>
           </div>
          <div class="main3">
              <h2>个人能力</h2>
              <h3>前端:</h3>
              <div class="todo1"><p class="todo1_1">Vue2.0<img src="./img/003.png" width="50px" /></p>
              <p class="todo1_1">elementUI<img src="./img/004.png" width="50px"/></p>
              </div>
              <h3>后端:(JAVA)</h3>
              <div>
                <div class="todo1">
                <p class="todo1_1">SpringBoot <img src="./img/005.jpeg" width="50px"/></p>
                <p class="todo1_2">MyBatis <img src="./img/006.png" width="50px"/></p>
                </div>
                
              </div>
              <h3>数据库:</h3>

              <div class="todo1">
                <p class="todo1_1">MySQL <img src="./img/007.png" width="50px"/></p>
              </div>
              
          </div>
         </div>
        <div class="resume_info">
          <h2>{{text}}</h2>
          <h2>{{text2}}</h2>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text:"hjadgcjhagdcad",
      text2:"asdfadsfadfadsfadyuqiwerkzbvcxlvkgwericbvqogufdsbvaergquierwtbszf"
      }
    }
  }
</script>

<style scoped>

.todo1{
  /* background-color: rgb(175, 122, 51); */
  width: 240px;
  height: 85px;
  display: flex;
  
}
.todo1_1{
    /* background-color: aqua; */
    width: 100px;
    height: 70px;
    display: flex;
    align-items: center;
    
}

.todo1_2{
    /* background-color: aqua; */
    width: 100px;
    height: 70px;
    display: flex;
    align-items: center;
    position:absolute;
    left: 145px;
}


.resume{
  background-color: aqua;
  width: 1500px;
  height: 1500px;
  background-repeat: no-repeat;
  background-size: 100% 100%;
}
.main3{
    background-color: rgb(0, 0, 0);
    margin-left: 5px;
    margin-top: 100px;
    height: 350px;
    width: 240px;
}

.resume_info{
    background-color: rgb(255, 255, 255);
    width: 510px;
    height: 1250px;
    margin-left: 2%;
    border-radius: 15px;
    word-wrap: break-word;
    word-break: normal;
    text-indent: 30px;
}

.body_main{
    background-color: rgb(65, 208, 255);
    
}

.body_info{
    background-color: rgb(209, 255, 255);
    width: 800px;
    height: 1300px;
    border-radius: 15px;
    display: flex;
    position:absolute;
    align-items: center;
    margin-left: 20%;
    top: 10%;
    
}

.main_info{
    background-color: rgb(0, 0, 0);
    width: 250px;
    height: 1250px;
    border-radius: 10px;
    color: white;
    margin-left: 10px;
}

.my_img{
    background-color: bisque;
    border-radius:100%; 
    width:100px; 
    height:100px;
    overflow: hidden;
    margin-left: 25%;
    

}

.img_class{
    display: flex;
    width: 250px;
    height: 100px;
    background-color: rgb(0, 0, 0);
}

.main{
    height: 150px;
    width: 240px;
    margin-left: 5px;
    background-color: rgb(0, 0, 0);
}

.main2{
    margin-left: 5px;
    height: 150px;
    width: 240px;

}


</style>