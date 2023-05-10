<template>
    <form id="singup-form" @submit="onSubmit">
        <div class="row">
            
            <label class=" mb-1 text-center col-form-label-lg">Movement Against Hunger Membership Registraion Form</label>
            <div class="col-4 c-tials form-group text-left">
                <label class="col-form-label col-form-label-sm justify-content-start">
                    Full Name <span class="text-danger">*</span></label>
                <input type="text"   class="form-control   form-control-sm"
                
                    v-model.trim="form.fullname"
                    @input="$event => setTouched('fullname')"
                    :class="v$.form.fullname.$error?'is-invalid':''"
                
                >
                <div v-for="error of v$.form.fullname.$errors" class="div invalid-feedback" :key="error.$uid">
                    {{ error.$message }}
                </div>
            </div>
            <div class="col-4 c-tials form-group ">
                <label class="col-form-label col-form-label-sm justify-content-start">
                    Phone Number <span class="text-danger">*</span></label>
                <input type="tel"    class="form-control   form-control-sm"
                
                v-model.trim="form.phonenumber"
                @input="$event => setTouched('phonenumber')"
                :class="v$.form.phonenumber.$error?'is-invalid':''"
                    
                    >
                    <div v-for="error of v$.form.phonenumber.$errors" class="div invalid-feedback" :key="error.$uid">
                        {{ error.$message }}
                    </div>
            </div>
            <div class="col-4 c-tials form-group ">
                <label class="col-form-label col-form-label-sm justify-content-start">
                    Email <span class="text-danger">*</span></label>
                <input type="email"  class="form-control   form-control-sm"
                
                v-model.trim="form.email"
                @input="$event => setTouched('email')"
                :class="v$.form.email.$error?'is-invalid':''"
            
                    >
                    <div v-for="error of v$.form.email.$errors" class="div invalid-feedback" :key="error.$uid">
                        {{ error.$message }}
                    </div>
            </div>
            <label class=" mb-1 mt-1 text-center col-form-label-lg">Residential Living Area Location</label>

            <div class="col-3 d-pack form-group text-left">
                <label class="col-form-label col-form-label-sm justify-content-start">
                    City <span class="text-danger">*</span></label>
                <input type="text"  class="form-control    form-control-sm"
                
                v-model.trim="form.city"
                @input="$event => setTouched('city')"
                :class="v$.form.city.$error?'is-invalid':''"
            
            >
            <div v-for="error of v$.form.city.$errors" class="div invalid-feedback" :key="error.$uid">
                {{ error.$message }}
            </div>
                </div>
            <div class="col-3 d-pack form-group text-left">
                <label class="col-form-label col-form-label-sm justify-content-start">
                    Sub City <span class="text-danger">*</span></label>
                <input type="text"  class="form-control    form-control-sm"
                
                v-model.trim="form.subcity"
                @input="$event => setTouched('subcity')"
                :class="v$.form.subcity.$error?'is-invalid':''"
            
            >
            <div v-for="error of v$.form.subcity.$errors" class="div invalid-feedback" :key="error.$uid">
                {{ error.$message }}
            </div>
                 </div>
            <div class="col-3 d-pack form-group text-left">
                <label class="col-form-label col-form-label-sm justify-content-start">
                    District <span class="text-danger">*</span></label>
                <input type="text"  class="form-control    form-control-sm"
                
                v-model.trim="form.district"
                @input="$event => setTouched('district')"
                :class="v$.form.district.$error?'is-invalid':''"
            
            >
            <div v-for="error of v$.form.district.$errors" class="div invalid-feedback" :key="error.$uid">
                {{ error.$message }}
            </div>
                 </div>
            <div class="col-3 d-pack form-group text-left">
                <label class="col-form-label col-form-label-sm justify-content-start">
                    House Number <span class="text-danger">*</span></label>
                <input type="number"   class="form-control   form-control-sm"
                
                v-model.trim="form.housenumber"
                @input="$event => setTouched('housenumber')"
                :class="v$.form.housenumber.$error?'is-invalid':''"
            
            >
            <div v-for="error of v$.form.housenumber.$errors" class="div invalid-feedback" :key="error.$uid">
                {{ error.$message }}
            </div>
                </div>
            <label class=" mb-1 mt-1 text-center col-form-label-lg">Desired Membership Packages</label>
            
           
            <div class="col-4 d-pack form-group text-left checkbox-xl">
                    <label for="checkbox-1" class="col-form-label form-check-label col-form-label-sm justify-content-start">
                        Platinum Membership: </label>
                        <input type="radio"  class=" f-top form-check-input" id="checkbox-1" name="" value="platinum"
                        
                        v-model.trim="form.membership"
                                >
                                
             </div>
                <div class="col-4 d-pack form-group text-left">
                    <label for="checkbox-2" class="col-form-label col-form-label-sm justify-content-start">
                    Gold Membership: </label>
                        <input type="radio"  class="f-top form-check-input" id="checkbox-2" name="" value="gold"  v-model.trim="form.membership" >
                                    
                                
                </div>
                <div class="col-4 d-pack form-group text-left">
                    <label for="checkbox-3" class="col-form-label col-form-label-sm justify-content-start">
                        Silver Membership: </label>
                        <input type="radio" class=" f-top form-check-input" id="checkbox-3" name="" value="silver"
                        
                        v-model.trim="form.membership">
                     

                                
                              
                </div>
       




                         
            
            <label class=" mb-1 mt-1 text-center col-form-label-lg">
                Upload Photo/Receit of Bank Transfer Payment Verification Receit</label>

           
                
                <form>
                    <div class="custom-file">
                        <input type="file"  class="form-control   form-control-sm" form-control id="customFile"  >
                        
                                
                                    
                                    
                                
                    </div>
                        
                        
                </form>
            <div class="col-12 btn-top-marigine form-group text-center">
                <button class="btn btn-vue btn-lg col-md-4 mb-2">Sign Up</button>
            </div>
        </div>
    </form>
</template>
<script>
import useVuelidate from '@vuelidate/core'
import { required, email, sameAs, between, minValue, maxValue, alpha, numeric, minLength, maxLength, helpers } from '@vuelidate/validators'
export default {
    name: 'SignupForm',

    setup(){
        return { v$: useVuelidate() }
    },
    data(){
        return {
            form: {
                fullname: '',
                phonenumber: '',
                email: '',
                city: '',
                subcity: '',
                district: '',
                housenumber: '',
                membership: '',
               // file: ''
            }
        }
    },

    validations(){
        return {
            form: {
                fullname: {
                    required,
                    alpha,//:helpers.withMessage('Seriously a number in your name', alpha),
                    minLength: minLength(3),
                    maxLength: maxLength(15)
                },
                phonenumber: {
                    
                    required,
                    minLength: minLength(10),
                    maxLength: maxLength(10)
                },

                
                email: {
                    email,
                    required

                },
                city: {

                    required
                },
                subcity: {

                    required
                },
                district: {

                    required
                },
                housenumber: {

                    required
                }
                  /*platinummembership: {

                    required
                },
                goldmembership: {
                    required
                },
                silvermembership: {
                    required
              }
                //file: {
                   // required
               }  */
            }
        }
    },

    methods: {

        setTouched(theModel){
            if(theModel == 'fullname' || theModel == 'all'){this.v$.form.fullname.$touch()}
            if(theModel == 'phonenumber' || theModel == 'all'){this.v$.form.phonenumber.$touch()}
            if(theModel == 'email' || theModel == 'all'){this.v$.form.email.$touch()}
            if(theModel == 'city' || theModel == 'all'){this.v$.form.city.$touch()}
            if(theModel == 'subcity' || theModel == 'all'){this.v$.form.subcity.$touch()}
            if(theModel == 'district' || theModel == 'all'){this.v$.form.district.$touch()}
            if(theModel == 'housenumber' || theModel == 'all'){this.v$.form.housenumber.$touch()}
           //if(theModel == 'file' || theModel == 'all'){this.v$.form.file.$touch()}

            

            
        },




        async onSubmit(event){
            event.preventDefault()
            console.log(this.form.membership)
            this.setTouched('all');
            if(!this.v$.$invalid){
            alert('The form has been submited succssefuly')
           
            }
        },
    },
   
}
</script>
<style>
.text-left{
    text-align: left !important;
}
.btn-top-marigine{
    margin-top: 2rem !important;
}
.f-top{
   margin-top: 1rem !important;
   margin-left: 0.3rem !important;
}
.btn-vue{
    background: #d4af37 !important;
    color: #31485D !important;
    font-weight: bold !important;
}
.btn-vue:hover{
    background: #c09f32 !important;
    color: #ffffff !important;
    font-weight: bold !important;

}
.form-group label{
    margin-top: 0.5rem !important;
}

@media (max-width: 768px) {
  .d-pack {
  width: 15rem !important;
  }
}

@media (max-width: 768px) {
  .d-pack {
  width: 15rem !important;
  margin-left: 4rem !important;
  }
}
@media (max-width: 768px) {
  .c-tials {
  width: 15rem !important;
  margin-left: 4rem !important;
  }
}

</style>