<template web>
  <Page>
    <ActionBar :title="navbarTitle" />
    <GridLayout rows="auto, auto">
      <!-- copy-webpack-plugin copies asset from src/assets to project output/build directory /assets -->
      <Img src="~/assets/logo.png" row="0" class="m-20" />
      <HelloWorld :msg="msg" row="1" />
    </GridLayout>
  </Page>
</template>
<template native>
  <Page>
    <ActionBar :title="navbarTitle" />
    <GridLayout rows="auto, auto">
      <!-- copy-webpack-plugin copies asset from src/assets to project output/build directory /assets -->
      <Image src="~/assets/logo.png" row="0" class="m-20" />
      <HelloWorld :msg="msg" row="1" />
    </GridLayout>
  </Page>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HelloWorld from "components/HelloWorld.vue";

const { VUE_APP_MODE, VUE_APP_PLATFORM } = process.env;

@Component({
  components: {
    HelloWorld
  }
})
export default class App extends Vue {
  private navbarTitle: string = `App.vue`;
  private msg: string = `Mode=${VUE_APP_MODE} and Platform=${VUE_APP_PLATFORM}`;
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style web lang="scss">
@import "~styles/style-one";

.w-page {
  height: 100%;
  width: 100%;
}

.nvw-action-bar {
  color: #42b983;
}
</style>
<style native lang="scss">
@import "~styles/style-one";
</style>
