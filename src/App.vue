<template>
  <div class="black-bg" v-if="modal == true">
    <div class="white-bg">
      <h4>상세페이지</h4>
      <p>상세페이지 내용</p>
      <button @click="modal = false">닫기</button>
    </div>
  </div>

  <div class="menu">
    <a v-for="menuname in topmenu" :key="menuname">{{ menuname }}</a>
  </div>

  <div>
    <img :src="roominfo[0].image" class="room-img" />
    <h4>{{ roominfo[0].title }}</h4>
    <p>{{ roominfo[0].price }}원</p>
  </div>
  <div>
    <img :src="roominfo[1].image" class="room-img" />
    <h4>{{ roominfo[1].title }}</h4>
    <p>{{ roominfo[1].price }}원</p>
  </div>
  <div>
    <img :src="roominfo[2].image" class="room-img" />
    <h4>{{ roominfo[2].title }}</h4>
    <p>{{ roominfo[2].price }}원</p>
  </div>
  <div>
    <img :src="roominfo[3].image" class="room-img" />
    <h4>{{ roominfo[3].title }}</h4>
    <p>{{ roominfo[3].price }}원</p>
  </div>
  <div>
    <img :src="roominfo[4].image" class="room-img" />
    <h4>{{ roominfo[4].title }}</h4>
    <p>{{ roominfo[4].price }}원</p>
  </div>
  <div>
    <img :src="roominfo[5].image" class="room-img" />
    <h4>{{ roominfo[5].title }}</h4>
    <p>{{ roominfo[5].price }}원</p>
  </div>
</template>

<script>
import datas from "./data";

export default {
  name: "App",
  data() {
    return {
      roominfo: datas,
      modal: false,
      counting: [0, 0, 0],
      topmenu: ["HOME", "SHOP", "About"],
      products: ["당산동 원룸", "양평동 원룸", "문래동 원룸"],
    };
  },
  methods: {
    increase() {
      this.counting += 1;
    },
  },
  components: {},
};
</script>

<style>
body {
  margin: 0;
}

div {
  box-sizing: border-box;
}

.black-bg {
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  padding: 20px;
}

.white-bg {
  width: 100%;
  background: white;
  border-radius: 8px;
  padding: 20px;
}

.room-img {
  width: 100%;
  margin-top: 40px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 10px;
  text-decoration: none;
}
</style>
