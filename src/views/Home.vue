<template web>
  <Page>
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
  name: "home",
  components: {
    HelloWorld
  }
})
export default class Home extends Vue {
  private navbarTitle: string = "Home.vue";
  private msg: string = `Mode=${VUE_APP_MODE} and Platform=${VUE_APP_PLATFORM}`;
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "~styles/style-one";
@import "~styles/style-two";

img,
image {
  display: block;
  margin: auto;
  margin-top: 4em;
}

image {
  height: 20%;
  width: 20%;
}
</style>
