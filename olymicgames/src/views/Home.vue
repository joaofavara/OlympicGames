<template>
  <div class="home">
    <div v-for="items in this.options">
      <dropdown :labels="items" />
      <br />
    </div>
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
        {
          title: [ 'Teste 1', 'Teste 2', 'Teste 3', 'Teste 4', 'Teste 5' ],
        },
        {
          title: [ 'Teste 11', 'Teste 22', 'Teste 33', 'Teste 44', 'Teste 55' ],
        },
        {
          title: [ 'Teste 111', 'Teste 222', 'Teste 333', 'Teste 444', 'Teste 555' ],
        }
      ],
    };
  },
  methods: {
    // make a function that get the data from olympic games 
    /*
    data: {
      Sex
      Age 
      Weight
      Height
      Country
      Year - City
      Season
      Sport
      Event
    }
    */
    openDropdown() {
      this.clickDropdown = true;
    },
    closeDropdown() {
      this.clickDropdown = false;
    },
  },
};
</script>
