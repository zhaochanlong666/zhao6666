<template>
  <div>
    <div>
      <input type="text" class="search" placeholder="搜索">
      <svg t="1691065888144" id="icons" class="icon" viewBox="0 0 1024 1024" version="1.1"
        xmlns="http://www.w3.org/2000/svg" p-id="2294" width="16" height="16">
        <path
          d="M1015.7783 938.2318 723.5205 644.0489c118.8301-156.9516 106.7182-381.4717-36.393-524.5819-156.4109-156.4109-410.0045-156.4109-566.4154 0-156.4109 156.375-156.4109 409.9697 0 566.3805 143.06 143.06 367.404 155.2425 524.3433 36.606l292.3223 294.2136c9.6051 9.6041 25.2221 9.6041 34.8252 0l43.5763-43.5763C1025.4172 963.4519 1025.4172 947.8369 1015.7783 938.2318zM194.9153 613.8132c-114.8621-114.8611-114.8621-301.0826 0-415.9089 114.8631-114.8621 301.0458-114.8621 415.9099 0 114.8631 114.8262 114.8631 301.0478 0 415.9089C495.9611 728.6764 309.7784 728.6764 194.9153 613.8132z"
          fill="#dbdbdb" p-id="2295"></path>
      </svg>
    </div>
  </div>
</template>

<script>
export default {
  name: 'VueSearch',

  data() {
    return {

    };
  },

  mounted() {

  },

  methods: {

  },
};
</script>

<style scoped>
.search {
  width: 300px;
  height: 35px;
  border-radius: 20px;
  background-color: aliceblue;
  border: 1px solid rgb(240, 242, 244);
  position: relative;
  left: 8px;
}

#icons {
  float: left;
  position: relative;
  left: 33px;
  top: 10px;
}

input {
  padding-left: 30px;
}
</style>