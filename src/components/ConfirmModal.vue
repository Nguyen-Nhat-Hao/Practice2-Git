<template>
  <div>
    <b-button v-b-modal.modal-1 class="btn-demo-modal"
      >Launch demo modal</b-button
    >
    <b-modal
      id="modal-1"
      headerClass=" p-0 border-bottom-0 "
      footerClass="p-2 border-top-0 my-3"
    >
      <slot></slot>
    </b-modal>
  </div>
  
 <!-- --------------------------------- -->

</template>

<script>
export default {
  
  data() {
    return {
    
    }
  },
};
</script>
<style>
#modal-1 {
  position: fixed;
  width: auto;
  height: auto;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  
}

button.close {
  padding: 0 10px;
  text-transform: uppercase;
  border: none;
  border-top-right-radius: 8px;
  background: #fff;
  font-weight: 700;
  font-size: larger;
  color: #ccc;
}
button.btn.btn-secondary,
button.btn.btn-primary {
  background: #fff;
  border: none;
  color: #000;
}
button.btn.btn-demo-modal {
  background: #ccc;
  border: 1px solid #ccc;
}
div#modal-1___BV_modal_body_ {
  padding: 0 16px;
}
.modal-footer {
  display: flex;
  justify-content: space-around !important;
}
</style>