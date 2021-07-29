<template>
  <v-container>
    <v-row :align="align" no-gutters style="height: 150px;">
      <v-col v-for="n in 3" :key="n">
        <Card />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Card from '../components/Card'

export default {
  name: 'HelloWorld',
  components: {
    Card
  },
  data: () => {}
}
</script>
