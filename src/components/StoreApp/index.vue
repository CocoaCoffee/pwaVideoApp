<template>
  <div class="appicon-size margin-bottom-10 margin-left-right-175">
    <a :href="appList.iosUrl" class="app-size">
      <img :src="appList.image" alt="">
    </a>
    <div class="text text-color-6a6a6a">{{ appList.name }}</div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component({
  components: {}
})
export default class StoreApp extends Vue {
  @Prop() private appList!: any
}
</script>

<style lang="scss" scoped>
// 文字
.text {
  font-family: STHeitiTC;
  font-size: 0.875rem ;
  font-weight: 500;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  text-align: center;
}

.text-color-6a6a6a {
  color: #6a6a6a;
}

// appIcon
.appicon-size {
  width: 3rem;
  height: auto;
}

.app-size {
  width: 48px;
  height: 48px;
  img {
    min-width: 48px;
    min-height: 48px;
    width: 100%;
    margin-bottom: 5px;
  }
}

// 排版
.margin-bottom-10 {
  margin-bottom: 10px;
}

.margin-left-right-175 {
  margin-left: 17.5px;
  margin-right: 17.5px;
}
</style>
