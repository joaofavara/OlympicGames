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
        <a href="#" class="dropdown-item">
          Dropdown item
        </a>
        <a class="dropdown-item">
          Other dropdown item
        </a>
        <a href="#" class="dropdown-item ">
          Active dropdown item
        </a>
        <a href="#" class="dropdown-item">
          Other dropdown item
        </a>
        <hr class="dropdown-divider">
        <a href="#" class="dropdown-item">
          With a divider
        </a>
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
  },
  methods: {
    dropdown() {
      console.log('teste....');
      this.clickOpen ? this.close() : this.open();
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
