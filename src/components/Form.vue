<template>
  <div>
    <my-header :cartItemCount="cartItemCount"></my-header>
      <div class="row">
        <div class="col-md-10 col-md-offset-1">
          <div class="panel panel-info">
            <div class="panel-heading">Pet Depot Checkout</div>
            <div class="panel-body">
              <div class="form-group">
                <div class="col-md-12">
                  <h4><strong>Enter Your Information</strong></h4>
                </div>
              </div>
            </div>
        </div><!--end of col-md-10 col-md-offset-1-->
      </div><!--end of row-->
    </div>
  </div>
</template>
<script>
import MyHeader from './Header.vue';
export default {
  name: 'Form',
  props: ['cartItemCount'],
  data () {
    return {
      states: {
        AL: 'Alabama',
        AK: 'Alaska',
        AR: 'Arizona',
        CA: 'California',
        NV: 'Nevada'
      },
      order: {
        firstName: '',
        lastName: '',
        address: '',
        city: '',
        zip: '',
        state: '',
        method: 'Home Address',
        business: 'Business Address',
        home: 'Home Address',
        gift:'',
        sendGift: 'Send As A Gift',
        dontSendGift: 'Do Not Send As A Gift'
      }
 
    }
  },
  components: { MyHeader },
  methods: {
    submitForm() {
      alert('Submitted');
    }
  }
}
</script>
<style scoped>
</style>
