<template>
  <div class="flex-row wrapper">
    <Mind class="mind"></Mind>
    <div class="all-coins">
      <div class="kasuma">
        <Kusama></Kusama>
      </div>
      <div class="flex-row two-coins">
        <div class="polkadot">
          <Polkadot></Polkadot>
        </div>
        <div class="etherium">
          <Ethereum></Ethereum>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Mind from "./Mind";
import Ethereum from "./Ethereum";
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
@media screen and (min-width: 1050px) and (max-width: 1750px) {
  .all-coins .kasuma {
    margin-right: 50px;
    margin-left: 0;
    transition: all .7s;
  }
}

/*@media screen and (min-width: 1500px) and (max-width: 1750px){*/
/*  .all-coins svg path {*/
/*    fill: var(--main) !important;*/
/*  }*/
/*}*/
.wrapper {
  margin-left: 50px;
  height: 150px;
  width: 500px;
}

.mind{
  margin-top: 100px;
}
.flex-row {
  display: flex;
  flex-direction: row;
}

.all-coins {
  margin-left: 20px;
}

.two-coins {
  height: 150px;
  gap: 30px;
}

.etherium {
  display: flex;
  align-items: flex-end;
  justify-content: flex-end;
}

.kasuma {
  display: flex;
  margin-left: 50px;
  margin-bottom: 50px;
  justify-content: flex-end;
  transition: all .7s;
}

svg {
  z-index: 20;
}

</style>