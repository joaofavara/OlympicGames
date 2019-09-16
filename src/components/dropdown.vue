<template>
  <div class="dropdown" @click="dropdown" :class="{ 'is-active':clickDropdown }">
    <div class="dropdown-trigger">
      <button class="button" aria-haspopup="true" aria-controls="dropdown-menu">
        <span>{{ this.value ? this.value : `Select the ${this.labels.name}` }}</span>
        <span class="icon is-small">
          <i class="fas fa-angle-down" aria-hidden="true"></i>
        </span>
      </button>
    </div>
    <div class="dropdown-menu" id="dropdown-menu" role="menu">
      <div class="dropdown-content">
      <div v-for="items in this.labels.title">
        <div @click="setValue(items)" class="dropdown-item">
          {{ items }}
          <hr class="dropdown-divider">
        </div>
      </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    // clickOpen: Boolean,
    // open: Function,
    // close: Function,
    labels: Object,
  },
  data() {
    return {
      clickDropdown: false,
      value: null,
    };
  },
  mounted() {
    console.log('this.labels: ', this.labels);
  },
  methods: {
    dropdown() {
      console.log('teste....', this.labels);
      this.clickDropdown ? this.closeDropdown() : this.openDropdown();
    },
    openDropdown() {
      this.clickDropdown = true;
    },
    closeDropdown() {
      this.clickDropdown = false;
    },
    setValue(data) {
      this.value = data;
      console.log('this.value: ', this.value);
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
