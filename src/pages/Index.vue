<template>
  <Layout>
    <div class="wrapper">
      <div class="steps"></div>
      <div class="content-wrapper"></div>
      <div class="code-snippet">
        <CodeSample></CodeSample>
      </div>

    </div>
  </Layout>
</template>

<script>
import CodeSample from "~/components/CodeSample";
export default {
  name: 'Index',
  components: {
    CodeSample
  },
  metaInfo: {
    title: 'AIRA'
  }
}
</script>

<style>

.steps{
  width: 100px
}

.content-wrapper{
  /*margin-top: 400px;*/
  /*width: 400px;*/
}

.wrapper {
  width: 100vw;
  z-index: 15;
  display: flex;
}
.code-snippet{
  position: fixed;
  right: 150px;
}

</style>
