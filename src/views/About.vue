<template web>
  <Page>
    <GridLayout>
      <Label
        text="This is an about page"
        :textWrap="true"
        horizontalAlignment="center"
        verticalAlignment="center"
      />
    </GridLayout>
  </Page>
</template>
<template native>
  <Page>
    <ActionBar :title="navbarTitle" />
    <GridLayout>
      <Label
        text="This is an about page"
        :textWrap="true"
        horizontalAlignment="center"
        verticalAlignment="center"
      />
    </GridLayout>
  </Page>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  name: "about"
})
export default class About extends Vue {
  private navbarTitle: string = `About.vue`;
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "~styles/style-two";
@import "~styles/style-one";

.nvw-label {
  height: 100%;
  width: 100%;
  padding-top: 3em;
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  justify-content: top;
  align-items: center;
}
</style>
