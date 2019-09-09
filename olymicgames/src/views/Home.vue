<template>
  <div class="home">
    <dropdown :labels="this.options"  :open="this.openDropdown" :close="this.closeDropdown" :clickOpen="clickDropdown" />
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
      options: [
        {title: 'Teste 1'},
        {title: 'Teste 2'},
        {title: 'Teste 3'},
        {title: 'Teste 4'},
        {title: 'Teste 5'},
      ]
    };
  },
  methods: {
    openDropdown() {
      this.clickDropdown = true;
    },
    closeDropdown() {
      this.clickDropdown = false;
    },
  },
};
</script>
