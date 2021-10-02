<template>
  <div class="flex-row">
    <div>
<!--      <div>-->
<!--        <Kusama></Kusama>-->
<!--      </div>-->
<!--      <div>-->
<!--        <Polkadot></Polkadot>-->
      <div id="123">
        <Mind></Mind>
        <Ethereum></Ethereum>
      </div>
<!--      </div>-->
    </div>
  </div>
</template>

<script>
import Ethereum from "./Ethereum";
import Mind from "./Mind";
import Kusama from "./Kusama";
import Polkadot from "./Polkadot";

export default {
  name: "CoinsAndIdeas",
  components: {
    Ethereum,
    Mind,
    Kusama,
    Polkadot
  }
}
</script>

<style scoped>
.flex-row {
  display: flex;
  flex-direction: row;
}

svg {
  z-index: 20;
}

</style>