<template>
  <v-content>
    <v-parallax
      v-resize="onResize"
      id="paralax"
      dark
      :src="require('@/assets/xbg.jpg')"
      :height="paralaxHeight"
    >
      <v-row align="center" justify="center">
        <v-col class="text-center" cols="12">
          <h1 class="display-1 font-weight-thin mb-4">Vuetify.js</h1>
          <h4 class="subheading">Build your application today!</h4>
        </v-col>
      </v-row>
    </v-parallax>
    <v-container>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Est harum esse doloribus odit ea qui nihil eum officia, veniam quam sed laborum, temporibus consectetur saepe id voluptate illo! Vel, et vitae veritatis ab dolorem perspiciatis voluptate asperiores, eius voluptates impedit similique minus quidem consequuntur, ipsam porro enim. Ea recusandae, quaerat incidunt, delectus earum mollitia blanditiis maxime, vero nesciunt rerum beatae! Sunt commodi molestiae necessitatibus nulla qui ex repellendus ullam ipsum, aliquam expedita. Error accusamus nobis expedita! Nulla unde molestiae dolores, ipsam officia vel alias laudantium tenetur et autem sunt. Exercitationem architecto ut iusto! Numquam maxime neque delectus dolore fugiat tempora facilis, consectetur, quo quos totam quaerat deleniti sed sunt corporis ad, sapiente nesciunt id quisquam dicta! Quam assumenda excepturi, porro itaque suscipit minus possimus eos, nostrum fugit velit dolore a ullam illum similique, repudiandae rem nihil temporibus impedit. Quidem quaerat similique fugit, delectus quos sapiente dolorem. Adipisci in eligendi assumenda. Ipsa, pariatur animi molestias veniam voluptatibus odit aliquam quaerat praesentium illum illo repellat. Hic iusto a sit reiciendis recusandae quidem. Voluptatibus sit consequatur, blanditiis voluptatum perspiciatis laboriosam deleniti ducimus possimus, laborum quaerat nemo maxime dicta architecto ex, adipisci autem minus rem in culpa dignissimos debitis amet esse quis. Vitae, praesentium.</p>
    </v-container>
  </v-content>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      windowSize: null,
      paralaxHeight: 500
    }
  },
  mounted() {
    this.onResize()
  },
  methods: {
    onResize() {
      this.windowSize = { x: window.innerWidth, y: window.innerHeight }
      this.paralaxHeight = this.windowSize.y - 64;
    }
  }
}
</script>
<style scoped>
.test {
  height: 1000px;
}
</style>
