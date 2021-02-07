<template>
  <div class="main-div">
    <innerDiv />
    <innerDiv />
    <innerDiv />
  </div>
</template>

<script>
import innerDiv from "./innerDiv";
export default {
  components: {
    innerDiv
  }
};
</script>

<style>
.main-div {
  display: flex;
  padding: 30px 30px;
  align-items: center;
  justify-content: center;
  position: relative;
  top: 72px;
}
</style>