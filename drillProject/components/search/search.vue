<template name="search">
    <view class="search-block">
        <image class="search-ico" src="../../static/search-ico.png"></image>
        <input type="text" placeholder="搜索" class="search-text" maxlength="-1" focus />
    </view>
</template>

<script>
export default {
    
}
</script>

<style>
.search-block {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  background-color: #ededed;
  width: 100%;
  margin-top: 10px;
  border-radius: 8px;
}
.search-ico{
    width: 35upx;
    height: 35upx;
    margin-left: 10px;
}
.search-text {
  font-size: 18px;
  background-color: #ededed;
  height: 80upx;
  width: 80%;
}
</style>