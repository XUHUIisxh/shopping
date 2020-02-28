<template>
  <div class="list">
    <ul class="c-course">
      <router-link to='/detail'>
        <li v-for="(item,index) in arrList" :key="index">
          <img :src="item.imgUrl" alt />
          <h1>{{ item.title }}</h1>
          <p>{{ item.msg }}</p>
        </li>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    arrList: Array
  }
};
</script>

<style scoped>
.c-course a{
  list-style: none;
}
.c-course li {
  position: relative;
  padding: 20px 10px;
}
.c-course li img {
  position: absolute;
  width: 108px;
  border-radius: 5px;
}
.c-course li h1 {
  font-size: 18px;
  padding-left: 120px;
  color: #2b333b;
}
.c-course li p {
  font-size: 14px;
  padding-left: 120px;
  color: #71777d;
}
</style>