<template>
  <div class="wrapper">
    <g-layout class="layout-wrapper">
      <g-header class="header-wrapper"> header </g-header>
      <g-layout class="layout-wrapper">
        <g-sider class="sider-wrapper"> sider </g-sider>
        <g-content class="content-wrapper"> content </g-content>
      </g-layout>
      <g-footer class="footer-wrapper"> footer </g-footer>
    </g-layout>
    <br />
    <g-layout class="layout-wrapper">
      <g-header class="header-wrapper"> header </g-header>
      <g-content class="content-wrapper"> content </g-content>
      <g-footer class="footer-wrapper"> footer </g-footer>
    </g-layout>
    <br />
  </div>
</template>
<style lang="scss" scoped>
$background: rgb(253, 208, 0);
.wrapper {
  > .layout-wrapper {
    height: 30vh;
    > .header-wrapper {
      height: 3em;
      background: $background;
    }
    > .content-wrapper {
      background: lighten($background, 25%);
    }
    > .layout-wrapper {
      height: 6em;
      > .sider-wrapper {
        width: 3em;
        background: lighten($background, 15%);
      }
      > .content-wrapper {
        background: lighten($background, 25%);
      }
      > .layout-wrapper {
        > .content-wrapper {
          background: lighten($background, 40%);
        }
        > .footer-wrapper {
          background: $background;
        }
      }
    }
    > .footer-wrapper {
      background: $background;
    }
  }
}
</style>
<script>
import Layout from "../../../src/layout";
import Header from "../../../src/header";
import Sider from "../../../src/sider";
import Content from "../../../src/content";
import Footer from "../../../src/footer";
export default {
  components: {
    "g-layout": Layout,
    "g-header": Header,
    "g-sider": Sider,
    "g-content": Content,
    "g-footer": Footer,
  },
};
</script>
