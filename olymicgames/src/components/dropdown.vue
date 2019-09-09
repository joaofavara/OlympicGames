<template>
  <div class="dropdown" @click="dropdown" :class="{ 'is-active':clickOpen }">
    <div class="dropdown-trigger">
      <button class="button" aria-haspopup="true" aria-controls="dropdown-menu">
        <span>Dropdown button</span>
        <span class="icon is-small">
          <i class="fas fa-angle-down" aria-hidden="true"></i>
        </span>
      </button>
    </div>
    <div class="dropdown-menu" id="dropdown-menu" role="menu">
      <div class="dropdown-content">
      <div v-for="items in this.labels">
        <a href="#" class="dropdown-item">
          {{ items.title }}
        </a>
      </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    clickOpen: Boolean,
    open: Function,
    close: Function,
    labels: Array,
  },
  methods: {
    dropdown() {
      console.log('teste....', this.labels);
      this.clickOpen ? this.close() : this.open();
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
