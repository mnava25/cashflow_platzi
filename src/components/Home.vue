<template>
  <Layout>
    <template #header>
      <Header></Header>
    </template>
    <template #resume>
      <Resume :label="'Ahorro Total'" :amount="amount" :total-amount="1000000">
        <template #graphic>
          <Graphic></Graphic>
        </template>
        <template #action>
          <Action></Action>
        </template>
      </Resume>
    </template>
    <template #movements>
      <Movements :movements="movements"></Movements>
    </template>
  </Layout>
</template>
<script>
import Layout from "@/components/Layout.vue";
import Header from "@/components/Header.vue";
import Resume from "@/components/Resume/Index.vue";
import Movements from "@/components/Movements/Index.vue";
import Action from "@/components/Action.vue";
import Graphic from "@/components/Resume/Graphic.vue";
export default {
  components: {
    Graphic,
    Action,
    Layout,
    Header,
    Resume,
    Movements,
  },
  data() {
    return {
      amount: null,
      movements: [
        {
          id: 1,
          title: "Movimiento",
          description: "Deposito de salario",
          amount: "1000",
        },
        {
          id: 2,
          title: "Movimiento 1",
          description: "Deposito de honorarios",
          amount: "500",
        },
        {
          id: 3,
          title: "Movimiento 3",
          description: "Comida",
          amount: "-100",
        },
        {
          id: 4,
          title: "Movimiento 4",
          description: "Colegiatura",
          amount: "1000",
        },
        {
          id: 5,
          title: "Movimiento 5",
          description: "Reparación equipo",
          amount: "1000",
        },
      ],
    };
  },
};
</script>
<style scoped></style>
