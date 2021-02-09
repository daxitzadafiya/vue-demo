<template>
  <b-container class="bv-example-row" fluid>
    <b-row class="text-center">
      <b-col cols="2" class="align-input">
        <b-form-input
          class="mb-2"
          v-model="valueA"
           @change="changeWidth($event)"
          type="number"
          placeholder="Enter value for A (Width)"
        ></b-form-input>
        <b-form-input
          class="mb-2"
          type="number"
          placeholder="Enter value for B (Height)"
          v-model="valueB"
          @change="changeHeight($event)"
        ></b-form-input>
      </b-col>
      <b-col cols="10">
        <center>
          <div class="boxDrag grab-bing" v-dragscroll>
            <img
              src="../assets/temp.png"
              :style="cssVars"
              alt="image not load"
            />
          </div>
        </center>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import { dragscroll } from "vue-dragscroll";
export default {
  data() {
    return {
      valueA: '',
      valueB:'',
      imgwidth: "4in",
      imgheight: "4in"
    };
  },
  computed: {
    cssVars() {
      return {
        "--height": this.imgheight,
        "--width": this.imgwidth,
      };
    }
  },
  methods: {
    changeHeight() {
      this.imgheight = this.valueB + "in";
    },
    changeWidth()
    {
        this.imgwidth = this.valueA + "in";
    }
  },
  directives: {
    dragscroll
  }
};
</script>

<style>
.boxDrag {
  cursor: -webkit-grab;
  cursor: -moz-grab;
  cursor: -o-grab;
  cursor: grab;
  height: 440px;
  width: 1160px;
  overflow: hidden;
  cursor: -webkit-grabbing;
  cursor: -moz-grabbing;
  cursor: -o-grabbing;
  cursor: grabbing;
  background-repeat: no-repeat;
  background-size: contain;
  position: relative;
  top: 50px;
}
img {
  height: var(--height);
  width:  var(--width);
}
.align-input {
  position: relative;
  top: 50px;
}
</style>