<template>
  <div class="bg-dark p-3">
    <div class="row mx-0 py-3 bg-light">
      <div class="col-sm-8">
        <p>
          Order #88
          <small class="text-mute">Today, 20 Mar 2022, 02:34 PM</small>
        </p>
        <div class="catePanel">
          <!-- <horizontal-scroll> -->
            <div class="wrapper">
              <tabs :mode="mode">
                  <tab />
              </tabs>
            </div>
          <!-- </horizontal-scroll> -->
        </div>
        <div style="height: 50px">
          <p style="padding: 15px">CATEGORY</p>
        </div>
        <div class="catePanel" style="height: 500px">
            <products/>
        </div>
        <div>

        </div>
      </div>
      <div class="col-sm-4">Text</div>
    </div>
  </div>
</template>

<script>
import Tab from "./Tab.vue";
import Tabs from "./Tabs.vue";
import Products from './product.vue';

export default {
  data() {
    return {
      mode: "light",
    };
  },
  components: {
    Products,
    Tab,
    Tabs,
  },
};
</script>

<style scoped>
p {
  font-family: serif;
}
.catePanel {
  box-sizing: 1px;
  border: none;
  border-radius: 20px;
  padding: 15px 15px 15px 15px;
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
}
</style>
