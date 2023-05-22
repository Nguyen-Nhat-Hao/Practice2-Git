<template>
  <div id="app">
    
    <div>
    <testEmitComponent @button-clicked="handleButtonClicked"></testEmitComponent>
    <p>{{ message }}</p>
  </div>

    <img alt="Vue logo" src="./assets/logo.png" />
    

    <ConfirmModal :user="user">
      <div class="modal-content">
        <h3 class="title-content">{{ title }}</h3>
        <p class="content my-4">{{ contentModal }}</p>
        <b-form-checkbox
          id="checkbox-1"
          v-model="status"
          name="checkbox-1"
          value="accepted"
          unchecked-value="not_accepted"
        >
          I accept the terms and use
        </b-form-checkbox>
      </div>
    </ConfirmModal>

    
    <!-- demo v-slot -->
    <template>
  <div>
    <b-button v-b-toggle.sidebar-variant>Toggle Sidebar</b-button>
    <b-sidebar id="sidebar-variant" title="Sidebar" bg-variant="dark" text-variant="light" shadow>
      <div class="px-3 py-2">
        <p>
          Cras mattis consectetur purus sit amet fermentum. Cras justo odio, dapibus ac facilisis
          in, egestas eget quam. Morbi leo risus, porta ac consectetur ac, vestibulum at eros.
        </p>
        <b-img src="https://picsum.photos/500/500/?image=54" fluid thumbnail></b-img>
      </div>
    </b-sidebar>
  </div>
</template>

  </div>
</template>

<script>
import ConfirmModal from "./components/ConfirmModal.vue";
import testEmitComponent from "./components/testEmitComponent.vue";
export default {
  name: "App",
  data() {
    return {
      contentModal:
        " Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nemo ab voluptates eveniet accusamus consequatur! Ipsam animi magnam excepturi temporibus accusamus. Deserunt nisi voluptatibus consectetur sed molestias vel eos tenetur magnam!",
      title: "BootstrapVue !!!",
     
      message: '',
      date: new Date(),
      timer: null
      }
      
    
  },
  methods: {
    onSlideStart() {
      this.sliding = true;
    },
    onSlideEnd() {
      this.sliding = false;
    },
    handleButtonClicked(data) {
      this.message = data;
    }
  },
  components: {
    ConfirmModal,
    testEmitComponent,
  },
  mounted() {
    this.timer = setInterval( () => {
      this.date = new Date()
    }, 1000 )
  }
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.modal-content {
  border: none !important;
  text-align: center;
  .title-content {
    font-size: 24px;
    text-align: center;
    margin-bottom: 12px;
  }
  .content {
    letter-spacing: -1;
    word-spacing: -1px;
    text-align: justify;
    margin: 0 !important;
  }
  #checkbox-1 {
    margin-right: 6px;
    display: inline-block;
  }
}
</style>
