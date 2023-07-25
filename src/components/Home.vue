<template>
  <Layout>
    <template #header>
      <Header></Header>
    </template>
    <template #resume>
      <Resume :label="'Ahorro Total'" :amount="amount" :total-amount="1000000">
        <template #graphic></template>
        <template #action></template>
      </Resume>
    </template>
    <template #movements>
      <Movements></Movements>
    </template>
  </Layout>
</template>
<script>
import Layout from "@/components/Layout.vue";
import Header from "@/components/Header.vue";
import Resume from "@/components/Resume/Index.vue";
import Movements from "@/components/Movements.vue";
export default {
  components: {
    Layout,
    Header,
    Resume,
    Movements,
  },
  data() {
    return {
      amount: null,
    };
  },
};
</script>
<style scoped></style>
