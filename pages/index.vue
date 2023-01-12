<template>

  <div>
    <client-only>
      <ul class="list-group" v-sortable>
        <li class="list-group-item">Foo</li>
        <li class="list-group-item">Bar</li>
        <li class="list-group-item">Baz</li>
      </ul>
    </client-only>
  </div>

</template>

<script>
// import Vue from 'vue'
// import VSortable from 'vue-sortable'
// Vue.use(Sortable)

export default {
  // components: { Sortable },
  plugins: [
    // '~/plugins/vue-sortable.js',
    { src: '~/plugins/vue-sortable.js', mode: 'client' },
  ],
  name: 'IndexPage',

  // directives: {
  //   VSortable
  // },
  mounted() {

    console.log(this.$sortable);
  },
  methods: {}
}
</script>

<style scoped>
.list-group {
  padding-left: 0;
  margin-bottom: 20px;
}

.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}

.list-group-item:first-child {
  border-top-left-radius: 4px;
  border-top-right-radius: 4px;
}

.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 4px;
  border-bottom-left-radius: 4px;
}
</style>
