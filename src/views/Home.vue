<template>
  <div class="home">
  <div class="personal">
  <h4>Personal Infomation</h4>
    <div name="Name" class="container">
      Name:&nbsp;&nbsp;
      <input class="input" type="text" placeholder="Text input">
    </div>
    <br />

    <div name="Sex" class="container">
      Sex:&nbsp;&nbsp;
      <div class="field">
        <div class="control">
          <div class="select">
            <select>
              <option>Select dropdown</option>
              <option>With options</option>
            </select>
          </div>
        </div>
      </div>
    </div>  
    <br />


    <div name="Age" class="container">
      Age:&nbsp;&nbsp;
      <div class="field">
        <div class="control">
          <div class="select">
            <select>
              <option>Select dropdown</option>
              <option>With options</option>
            </select>
          </div>
        </div>
      </div>
    </div>
    <br />

    <div name="Weight" class="container">
      Weight:&nbsp;&nbsp;
      <div class="field">
        <div class="control">
          <div class="select">
            <select>
              <option>Select dropdown</option>
              <option>With options</option>
            </select>
          </div>
        </div>
      </div>
    </div>
    <br />

    <div name="Height" class="container">
      Height:&nbsp;&nbsp;
      <div class="field">
        <div class="control">
          <div class="select">
            <select>
              <option>Select dropdown</option>
              <option>With options</option>
            </select>
          </div>
        </div>
      </div>
    </div>
    <br />

    <div name="Country" class="container">
      Country:&nbsp;&nbsp;
      <div class="field">
        <div class="control">
          <div class="select">
            <select>
              <option>Select dropdown</option>
              <option>With options</option>
            </select>
          </div>
        </div>
      </div>
    </div>
    <br />
  </div>

  <div class="games">
  <h4>Games Infomation</h4>
    <div name="Year - City" class="container">
      Year - City:&nbsp;&nbsp;
      <div class="field">
        <div class="control">
          <div class="select">
            <select>
              <option>Select dropdown</option>
              <option>With options</option>
            </select>
          </div>
        </div>
      </div>
    </div>
    <br />

    <div name="Season" class="container">
      Season:&nbsp;&nbsp;
      <div class="field">
        <div class="control">
          <div class="select">
            <select>
              <option>Select dropdown</option>
              <option>With options</option>
            </select>
          </div>
        </div>
      </div>
    </div>
    <br />

    <div name="Sport" class="container">
      Sport:&nbsp;&nbsp;
      <div class="field">
        <div class="control">
          <div class="select">
            <select>
              <option>Select dropdown</option>
              <option>With options</option>
            </select>
          </div>
        </div>
      </div>
    </div>
    <br />

    <div name="Event" class="container">
      Event:&nbsp;&nbsp;
      <div class="field">
        <div class="control">
          <div class="select">
            <select>
              <option>Select dropdown</option>
              <option v-for="items in this.options[0].title">{{ items }}</option>
            </select>
          </div>
        </div>
      </div>
    </div>
    <br />
  </div>
    

  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'home',
  data() {
    return {
      options: [
        {
          name: 'Year',
          title: [ 'Teste 1', 'Teste 2', 'Teste 3', 'Teste 4', 'Teste 5' ],
        },
        {
          name: 'Sport',
          title: [ 'Teste 11', 'Teste 22', 'Teste 33', 'Teste 44', 'Teste 55' ],
        },
        {
          name: 'Event',
          title: [ 'Teste 111', 'Teste 222', 'Teste 333', 'Teste 444', 'Teste 555' ],
        }
      ],
    };
  },
  methods: {
    // make a function that get the data from olympic games 
    /*
    data: {
      Name
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
  },
};
</script>

<style scoped lang="scss">
.home {
display: flex;
justify-content: center;
border: 1px solid red;
background-image: url('../assets/download.jpeg');
background-repeat: no-repeat;
background-position: center center;
background-size: 750px;

  .personal {
    margin: 5px;
    padding: 15px;
    border: 1px solid blue;
  }

  .games {
    margin: 5px;
    padding: 15px;
    border: 1px solid yellow;
  }
}
.container {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  // border: 1px red solid;
  margin: 2px;
  padding: 10px;
}
</style>
