<template>
  <div class="home">
    <dropdown :open="this.openDropdown" :close="this.closeDropdown" :clickOpen="clickDropdown" />
  </div>
</template>

<script>
// @ is an alias to /src
import dropdown from '@/components/dropdown.vue';

export default {
  name: 'home',
  components: {
    dropdown,
  },
  data() {
    return {
      clickDropdown: false,
    };
  },
  methods: {
    openDropdown() {
      console.log('this.clickDropdown 1', this.clickDropdown);
      this.clickDropdown = true;
      console.log('this.clickDropdown 2', this.clickDropdown);
    },
    closeDropdown() {
      console.log('this.clickDropdown 3', this.clickDropdown);
      this.clickDropdown = false;
      console.log('this.clickDropdown 4', this.clickDropdown);
    },
  },
};
</script>
