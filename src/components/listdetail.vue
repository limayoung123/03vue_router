<template>
  <div class="container">
      {{$route.params.id}}
      <!-- $route.params.id 도메인/id값을 변화되게하기위해 -->
      <router-link to="/product">뒤로가기</router-link>
      <h2>list detail</h2>
          <!-- router로 전송됐기에 그냥 연결만시켜주면됌 -->
        <div>
            <h3>{{listData[$route.params.id].title}}</h3>
            <h5>{{listData[$route.params.id].content}}</h5>
        </div>
  </div>
  
</template>

<script>
export default {
    name:'detail',
    props:['listData']

}
</script>

<style>
.container{padding: 20px;}
</style>