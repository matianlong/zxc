
VUE实现Tab切换

https://blog.csdn.net/weixin_34354173/article/details/91388528

vue实现tab切换样式

<template>
    <div class="container">
        <ul class="tab-list">
          <li class="tab-li"
              :class="actiove == index ?'Active' : '' "
              v-for="(item,index) in list" @click="cutTabClick(index)"
          >{{item}}</li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: "tab",
       data(){
          return{
            list: ["全部", "招商供应", "招聘求职", "出租求租", "二手设备", "采购求购"],
            actiove:0,
          }
       },
      methods:{
        cutTabClick(index){
          // console.log(index);
          this.actiove = index
        }
      }
    }
</script>

https://blog.csdn.net/YY110621/article/details/84787963
