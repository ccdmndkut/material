<template>
  <div id='app'>
    <mdc-layout-grid>
      <mdc-layout-cell
        align='middle'
        desktop='12'
        tablet='3'
      >
        <mdc-layout-inner-grid>
          <mdc-layout-cell
            desktop='2'
            tablet='3'
          ></mdc-layout-cell>
          <mdc-layout-cell
            class='mid'
            desktop='8'
            tablet='3'
          >
            <mdc-layout-inner-grid>
              <mdc-layout-cell
                :desktop='space'
                tablet='3'
              ></mdc-layout-cell>

              <mdc-layout-cell
                :desktop='desktop'
                tablet='3'
              >
                <div @click='test'>
                  <HelloWorld/>
                </div>
              </mdc-layout-cell>
            </mdc-layout-inner-grid>
          </mdc-layout-cell>
        </mdc-layout-inner-grid>
      </mdc-layout-cell>
    </mdc-layout-grid>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "app",
  components: {
    HelloWorld
  },
  data() {
    return {
      desktop: 10
    };
  },
  computed: {
    space() {
      var half = this.desktop / 2;
      var minus = 6 - half
      return minus
    }
  },
  methods: {
    test() {
      if (this.desktop == 10) {
        this.desktop = 8;
      } else {
        this.desktop = 10;
      }
    }
  }
};
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;

  background-color: #f5f5f5;
  height: 100vh;
}
.mid {
  background-color: #f5f5f5;
}
</style>
