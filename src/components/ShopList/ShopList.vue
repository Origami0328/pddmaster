<template>
  <a class="recommend-item" >
    <img :src="item.thumb_url" alt="" width="100%" v-if="item.thumb_url">
    <h4 class="item-title">{{item.short_name}}</h4>
    <div class="item-bottom">
      <span class="item-price">¥{{item.price / 100}}</span>
      <span class="item-sales">{{item.sales_tip}}</span>
      <button class="item-btn" v-if="false">找相关</button>
      <span class="item-user" v-else>
        <img src="" alt="">
        <img src="" alt="">
      </span>
    </div>
  </a>
</template>

<script>
export default {
  name: "ShopList",
  props:{
    item:Object
  }
}
</script>

<style  lang="stylus" scoped>
.recommend-item:nth-child(2n-1)
  margin-right 1%
.recommend-item
  width 49.5%
  background #FFF
  padding-bottom 15px
  margin-bottom 15px
  .item-title
    line-height 20px
    font-size 13px
    font-weight lighter
    height 20px
    overflow hidden
    margin 5px 0
    padding 0 5px
  .item-bottom
    display flex
    flex-direction row
    align-items center
    padding 0 6px
    .item-price
      flex 2
      color red
      font-weight bolder
      font-size 12px
    .item-sales
      flex 4
      font-size 10px
      color #666666
    .item-btn
      flex 2
      border 1px solid orangered
      height 26px
      border-radius 5px
      font-size 10px
      background-color transparent
      color red
    .item-user
      img
        width 30px
        border-radius 50%
      img:nth-child(2)
        margin-left -6px

</style>