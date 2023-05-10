<template>
   
   








                         <ul v-if="!form.required">
                    <li>
                        <div class="col-4 d-pack form-group text-left checkbox-xl">
                            <label for="checkbox-1" class="col-form-label form-check-label col-form-label-sm justify-content-start">
                                Platinum Membership: </label>
                            <input type="checkbox"  class=" f-top form-check-input" id="checkbox-1" name="" value="">   
                        <div v-for="error of v$.form.$errors" class="div invalid-feedback" :key="error.$uid">
                {{ error.$message }}
            </div>
                        </div>
                    </li>
                    
                    <li>
                        <div class="col-4 d-pack form-group text-left checkbox-xl">
                            <label for="checkbox-1" class="col-form-label form-check-label col-form-label-sm justify-content-start">
                                Platinum Membership: </label>
                            <input type="checkbox"  class=" f-top form-check-input" id="checkbox-1" name="" value="">   
                        </div>
                    </li>
                    
                    <li>
                        <div class="col-4 d-pack form-group text-left checkbox-xl">
                            <label for="checkbox-1" class="col-form-label form-check-label col-form-label-sm justify-content-start">
                                Platinum Membership: </label>
                            <input type="checkbox"  class=" f-top form-check-input" id="checkbox-1" name="" value="">   
                        </div>
                    </li>
                    
                </ul>



                         
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
