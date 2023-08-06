<template>
  <div class="home">
    <div class="top">
      <h3>微信读书</h3>
      <br>
      <SearCh></SearCh>
    </div>

    <div class="comment">
      <div class="bx">
        <div class="bx1">
          <div class="nas">
            <img
              src="https://dogefs.s3.ladydaily.com/~/source/wallhaven/full/yx/wallhaven-yx5vog.jpg?w=2560&h=1440&fmt=webp"
              alt="" class="imgs">
            <span class="wx">微信用户</span> <span class="ty">体验卡今日到期</span>
            <div class="fankui">
              <span>反馈</span>
            </div>
          </div>
        </div>
        <div class="shu">
          <div class="shujia">
            <br>
            <img src="https://img1.baidu.com/it/u=4128112777,3592295491&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500" alt=""
              class="shuimg">
            <div class="shup">书架<span class="sp"><svg t="1691326299443" class="icon" viewBox="0 0 1024 1024" version="1.1"
                  xmlns="http://www.w3.org/2000/svg" p-id="4654" width="32" height="32">
                  <path
                    d="M478.4 768.64a32 32 0 0 1 0-45.216l222.4-222.4-222.4-222.4a32 32 0 1 1 45.248-45.248L768.672 478.4a32 32 0 0 1 0 45.248L523.648 768.672a32 32 0 0 1-45.248 0z"
                    fill="#b8b8b8" p-id="4655"></path>
                </svg></span></div>
          </div>
        </div>
      </div>
    </div>

    <!-- Tab切换 -->
    <div id="WeChatPagenav">
      <!-- v-for="(tab, index) in tabs" :key="index" :class="{ 'active': index === activeTab }" @click="activeTab = index" -->
      <ul>
        <li v-for="(tab, index) in tabs" :key="index" :class="{ 'active': index === activeTab }"
          @click="activeTab = index"> {{ tab.name }}</li>
      </ul>
    </div>

    <!--这是切换子组件 -->
    <div id="WeChatPage_qiehuan">
      <div v-for="(tab, index) in tabs" :key="index" v-show="index === activeTab">
        <component :is="tab.component" @add-data="addData"></component>
      </div>
    </div>
    <div class="gongneng">
      <div class="box_tt">
        <div class="item">
          <svg t="1691324938478" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg"
            p-id="5981" width="32" height="32">
            <path
              d="M1003.746212 414.274258l0-110.517069c-3.069919-80.84119-86.981027-84.934414-86.981027-84.934414l-42.97886 1.023306c0 0 65.491597-86.981027-13.302981-142.239562-155.542542-93.120864-339.737658 124.843356-339.737658 124.843356l-2.046612 736.780463 332.574514 0c91.074252-1.023306 92.097558-78.794577 92.097558-78.794577l0-337.691045c-1.023306-18.419512-6.139837-29.67588-6.139837-29.67588C1007.839437 473.626018 1003.746212 414.274258 1003.746212 414.274258zM802.106796 111.887276c56.281841 18.931165 30.187533 58.328453 30.187533 58.328453s-1.534959 16.884552-35.815717 49.118698l-212.847689 0C583.630922 219.334427 698.241216 91.932806 802.106796 111.887276zM883.459638 534.001083l0 327.457983c0 0-3.069919 25.582655-34.280758 24.559349l-299.317063 0 0-388.856355 307.503513 0C857.36533 497.16206 885.506251 501.255285 883.459638 534.001083zM943.834704 418.367483c0 0-7.163143 25.582655-29.67588 23.536043l-364.80866 0-0.511653-166.79891 367.878578 0c0 0 23.536043 2.558265 27.117614 27.629267L943.834704 418.367483z"
              fill="#5D5D5D" p-id="5982"></path>
            <path
              d="M104.327602 493.067812c0 0-5.116531 11.256368-6.139837 29.67588l0 337.691045c0 0 1.023306 77.771271 92.097558 78.794577l332.574514 0-2.046612-736.780463c0 0-184.195116-217.96422-339.737658-124.843356-78.794577 55.258535-13.302981 142.239562-13.302981 142.239562l-42.97886-1.023306c0 0-83.911108 4.093225-86.981027 84.934414l0 110.517069C37.812699 414.273235 33.719474 473.624994 104.327602 493.067812zM457.927989 219.333404l-212.847689 0c-34.280758-32.234145-35.815717-49.118698-35.815717-49.118698s-26.094308-39.397289 30.187533-58.328453C343.317695 91.931782 457.927989 219.333404 457.927989 219.333404zM184.193581 497.161037l307.503513 0 0 388.856355-299.317063 0c-31.210839 1.023306-34.280758-24.559349-34.280758-24.559349l0-327.457983C156.05266 501.254262 184.193581 497.161037 184.193581 497.161037zM97.724207 302.732859c3.581572-25.071002 27.117614-27.629267 27.117614-27.629267l367.878578 0-0.511653 166.79891-364.80866 0c-22.512736 2.046612-29.67588-23.536043-29.67588-23.536043L97.724207 302.732859z"
              fill="#5D5D5D" p-id="5983"></path>
          </svg>
        </div>
        <div class="item1">福利</div>
      </div>
      <div class="box_xx">
        <div class="item">
          <svg t="1691325206656" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg"
            p-id="8563" width="37" height="37">
            <path
              d="M648.84736 775.49568c-40.73472 0-107.74528 11.63264-116.46976 37.84704h-37.84704c-11.65312-26.19392-75.71456-37.84704-116.49024-37.84704H162.6112v-564.8384h232.91904c49.50016 0 93.16352 26.19392 116.46976 64.04096 23.30624-37.84704 66.99008-64.04096 116.46976-64.04096H861.3888v564.85888H648.84736z m-154.3168-448.38912c0-46.57152-49.50016-78.60224-96.07168-78.60224H203.38688v486.23616h174.67392c37.86752 0 99.00032 0 116.49024 29.12256V327.10656z m329.0112-78.60224h-195.072c-49.47968 0-96.07168 32.01024-96.07168 78.60224v433.82784c17.48992-29.12256 78.60224-29.12256 116.46976-29.12256h174.6944V248.50432z m0 0"
              fill="" p-id="8564"></path>
          </svg>
        </div>
        <div class="item1">书城</div>
      </div>
      <div class="box_kk">
        <div class="item">
          <svg t="1691325328939" class="icon" viewBox="0 0 1025 1024" version="1.1" xmlns="http://www.w3.org/2000/svg"
            p-id="10503" width="32" height="32">
            <path
              d="M512.61025 48.820024a463.790226 463.790226 0 1 0 463.790227 463.790226A463.790226 463.790226 0 0 0 512.61025 48.820024z m0 854.350417a390.560191 390.560191 0 1 1 390.560191-390.560191 390.560191 390.560191 0 0 1-390.560191 390.560191z m0-592.675089a226.769011 226.769011 0 0 0-227.501311 226.28081v122.05006A56.631228 56.631228 0 0 0 341.740167 713.504648h28.315614a56.631228 56.631228 0 0 0 56.875327-56.387127v-84.946842a56.631228 56.631228 0 0 0-56.875327-56.387127h-43.205721a186.980691 186.980691 0 0 1 371.520381 0h-43.449821a56.631228 56.631228 0 0 0-56.875328 56.387127v84.946842a56.631228 56.631228 0 0 0 56.875328 56.387127H683.480334a56.387128 56.387128 0 0 0 56.631227-56.387127v-122.05006A226.769011 226.769011 0 0 0 512.61025 309.274851z"
              p-id="10504" fill="#515151"></path>
          </svg>
        </div>
        <div class="item1">听书</div>
      </div>
    </div>
  </div>
</template>
<style lang="less" scoped>
* {
  margin: 0;
  padding: 0;
  list-style: none;
  text-decoration: none;
}

#WeChatPagenav {
  height: 50px;
  line-height: 50px;
  background-color: #fff;
  position: sticky;
  top: 90px;
  z-index: 999;

  ul {
    font-weight: 900;
    height: 50px;
    line-height: 50px;
    color: #858C96;
    display: flex;
    justify-content: space-around;
  }
}

.top {
  width: 100%;
  height: 100px;
  position: fixed;
  top: 0px;
  background-color: #fff;
  z-index: 999;
}

.active {
  color: #1B88EE;
  font-weight: 900;
}

.top h3 {
  margin-top: 20px;
  text-align: center;
}

#icons {
  float: left;
  position: relative;
  left: 30px;
  top: 5px;
}

.comment {
  position: relative;
  top: 15px;
  width: 100%;
  height: 170px;
}

.bx {
  width: 90%;
  height: 150px;
  background-color: gray;
  border-radius: 15px;
  margin: auto;
  margin-top: 100px;
}

.bx1 {
  width: 80%;
  height: 40px;
}

.imgs {
  width: 20px;
  height: 20px;
  border-radius: 50px;
  position: relative;
  top: 5px;

}

.nas {
  width: 74%;
  height: 30px;
  position: relative;
  top: 10px;
  margin-left: 23px;
  font-size: 10px;
}

.nas .wx {
  color: white;
  position: relative;
  top: 5px;
  margin-left: 8px;
}

.nas .ty {
  color: rgb(164, 163, 163);
  position: relative;
  top: 5px;
}

.nas .fankui {
  width: 40px;
  height: 20px;
  float: right;
  margin-top: 5px;
  border-bottom-left-radius: 20px;
  border-top-left-radius: 20px;
  color: white;
  text-align: center;
  background-color: rgb(143, 142, 142);
  position: relative;
  left: 115px;
}

.shu {
  width: 80%;
  height: 110px;
}

.shu .shujia {
  width: 74%;
  height: 110px;
  margin-left: 20px;
}

.shu .shuimg {
  width: 60px;
  height: 80px;
  position: relative;
  bottom: 10px;
}

.shu .shup {

  float: right;
  position: relative;
  top: 10px;
  left: 110px;
  color: white;
  writing-mode: vertical-rl;
  text-orientation: upright;
}

.shup .sp {
  position: relative;
  bottom: 30px;
  left: 13px;
  color: rgb(204, 204, 204);
}

.footer {
  width: 100%;
}

.dibu {
  width: 100%;
  height: 60px;
  background-color: white;
  position: fixed;
  bottom: 40px;
}

.dibu ul li {
  width: 125px;
  height: 60px;
  text-align: center;
  float: left;
}

.dibu ul li span {
  line-height: 100px;
}

.tab {
  width: 100%;
  height: 60px;
}

.dingwei {
  background-color: #fff;
  position: sticky;
  top: 80px;
  height: 50px;
  line-height: 50px;
}

.tab ul li {
  width: 20%;
  line-height: 60px;
  float: left;
  font-weight: 600;
  text-align: center;
}

.dibu ul li .icon {
  position: relative;
  left: 32px;
  bottom: 15px;
}

.tabs {
  width: 100%;
  float: left;

}

.gongneng {
  display: flex;
  position: fixed;
  top: 607px;
  z-index: 999;
  width: 100%;
  height: 60px;
  background-color: #ffffff;
}

.box_tt {
  flex: 1;
  display: flex;
  flex-direction: column;
}

.box_xx {
  flex: 1;
  display: flex;
  flex-direction: column;
}

.box_kk {
  flex: 1;
  display: flex;
  flex-direction: column;
}

.item {
  width: 100%;
  height: 62%;
  text-align: center;
  position: relative;
  top: 5px;
  cursor: pointer;
}

.item1 {
  width: 100%;
  height: 38%;
  text-align: center;
  color: #494949;
  cursor: pointer;
}</style>
<script>
import SearCh from '../components/SearCh.vue'
import Tab from '../components/TabTwo.vue'
import TabOne from '../components/TabOne.vue'
import TabThree from '../components/TabThree.vue'
import TabFour from '../components/TabFour.vue'
import TabFive from '../components/TabFive.vue'
export default {
  components: {
    SearCh,
    Tab, TabOne,
    TabThree,
    TabFour,
    TabFive
  },
  data() {
    return {
      tabs: [
        { name: '推荐', component: Tab },
        { name: '分类', component: TabOne },
        { name: '排行', component: TabThree },
        { name: '文学', component: TabFour },
        { name: '哲学', component: TabFive },
      ],
      activeTab: 0,
    }
  },

}

</script>