<template>
  <div class="main-nav">
    <div class="nav-name">{{main.navName}}</div>
    <div class="user-msg">
      <ul>
       <li v-for="(item,index) in main.mainOperation">
       <div :title="item.title">
          <img :src="item.icon" :alt="item.title" />
          <div class="meg-detail">
            <ul></ul>
          </div>
       </div>
       </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'mainNav',
  props:['main'],
  data () {
    return {}
  }
}
</script>

<style lang="scss">
$width:100%;
$backColor:#eaeaea;
.main-nav{
  width:$width;
  background:$backColor;
  height:50px;
}
.nav-name,{
  float:left;
  height:100%;
  line-height:50px;
  padding-left:20px;
}
.user-msg{
  float:right;
  height:100%;
  line-height:50px;
  padding-right:20px;
  li{
    width:50px;
    div{
      line-height:50px;
    }

  }
}

</style>
