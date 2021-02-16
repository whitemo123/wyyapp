<template>
  <div class="home">
    <van-tabs sticky>
      <van-tab title="官方"></van-tab>
      <van-tab title="精选"></van-tab>
      <van-tab title="曲风"></van-tab>
      <van-tab title="全球"></van-tab>
      <van-tab title="MV"></van-tab>
      <van-tab title="特色"></van-tab>
    </van-tabs>
    <div class="mobai-recommand__box">
      <h1 class="mobai-recommand__title">榜单推荐</h1>
      <div class="mobai-recommand__itembox">
        <div v-for="index in 3" class="mobai-recommand__item">
          <div class="mobai-recommand__imgitem">畅销榜</div>
          <span class="mobai-recommand__titleitem">畅销榜</span>
        </div>
      </div>
    </div>
    <div class="mobai-normal__box">
      <div class="mobai-normal__title">
        <img src="http://p3.music.126.net/0ZrFKozxhB6nPQYZl4lsEA==/109951163421145421.png" alt="">官方榜
      </div>
      <div v-for="index in 6" class="mobai-normal__item">
        <div class="mobai-normal__item_left">
          <p>飙升榜</p>
          <img src="http://p1.music.126.net/GjpC4y21lxvh-wbvRZCPDQ==/109951165602360304.jpg?imageView=1&type=webp&thumbnail=370x0" alt="">
        </div>
        <div class="mobai-normal__item_right">
          <ul>
            <li>1. for ya - 蒋小妮</li>
            <li>2. 你的轮廓 - 叶琼琳</li>
            <li>3. 睡在风里 - 彭席彦</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="mobai-line"></div>
    <div class="mobai-featured__box">
      <p>精选榜</p>
      <van-grid :border="false" :column-num="3">
        <van-grid-item v-for="index in 5">
          <div>Test</div>
        </van-grid-item>
      </van-grid>
    </div>

    <div style="width: 100%; height: 10rem; background-color: #F5F5F5"></div>
  </div>
</template>

<script>

import { Tab, Tabs } from 'vant';
import { Grid, GridItem } from 'vant';

export default {
  name: 'Home',
  components: {
    [Tab.name]: Tab,
    [Tabs.name]: Tabs,
    [Grid.name]: Grid,
    [GridItem.name]: GridItem,
  },
};
</script>

<style lang="less">
.van-tabs {
}
.van-tabs__nav {
  background-color: #F5F5F5;
}
.van-tab__text {
  z-index: 999;
  font-size: 0.4rem;
}
.van-tab--active .van-tab__text {
  font-weight: bold;
}
.van-tabs__line {
  height: 0.2rem;
  top: 40%;
  z-index: 0;
}
.mobai-line {
  width: 100%;
  height: 0.3rem;
  background-color: #EEEEEE;
}
.mobai-recommand__box {
  width: 90%;
  background-color: #ffffff;
  margin: 0.1rem auto;
  box-sizing: border-box;
  padding: 0.4rem 0.5rem;
  border-radius: 0.2rem;
}
.mobai-recommand__title {
  width: 100%;
  text-align: left;
  font-size: 0.5rem;
}
.mobai-recommand__itembox {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 0.5rem;
}
.mobai-recommand__item {
  flex: 1;
  width: 100%;
  height: 2.5rem;
  margin: 0 0.1rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.mobai-recommand__imgitem {
  width: 100%;
  height: 2.5rem;
  display: flex;
  justify-content: center;
  align-items: center;
}
.mobai-recommand__item:nth-child(1) .mobai-recommand__imgitem {
  background-color: red;
}
.mobai-recommand__item:nth-child(2) .mobai-recommand__imgitem {
  background-color: green;
}
.mobai-recommand__item:nth-child(3) .mobai-recommand__imgitem {
  background-color: cornflowerblue;
}
.mobai-recommand__titleitem {
  width: 100%;
  text-align: left;
}

.mobai-normal__box {
  width: 100%;
  padding: 0.5rem 0.5rem;
  box-sizing: border-box;
}
.mobai-normal__title {
  width: 100%;
  display: flex;
  align-items: center;
  font-size: 0.4rem;
  font-weight: bold;
}
.mobai-normal__title img {
  width: 0.5rem;
  height: 0.5rem;
  border-radius: 100%;
  margin-right: 0.1rem;
}
.mobai-normal__item {
  width: 100%;
  background-color: #F3E0E6;
  padding: 0.5rem 0.6rem;
  box-sizing: border-box;
  border-radius: 0.5rem;
  margin-top: 0.5rem;
  display: flex;
}
.mobai-normal__item_left {
  flex: 3;
  width: 100%;
  height: 100%;
}
.mobai-normal__item_left p {
  width: 100%;
  text-align: left;
  font-size: 0.6rem;
  color: #E82E78;
  font-weight: bold;
}
.mobai-normal__item_left img {
  display: block;
  width: 2rem;
  height: 2rem;
  border-radius: 0.3rem;
  margin-top: 0.3rem;
}
.mobai-normal__item_right {
  flex: 7;
  width: 100%;
  height: inherit;
  padding: 0 0 0 0.5rem;
}
.mobai-normal__item_right ul {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: center;
}
.mobai-normal__item_right li {
  width: 100%;
  height: 0.8rem;
  line-height: 0.8rem;
  text-align: left;
}
.mobai-featured__box {
  width: 100%;
  padding: 0.5rem 0.5rem;
  box-sizing: border-box;
}
.mobai-featured__box p {
  width: 100%;
  text-align: left;
  font-size: 0.4rem;
  font-weight: bold;
}
.van-grid-item {

}
</style>
