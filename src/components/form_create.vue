<template>
    <div>
      <ValidationObserver v-slot="{ invalid }">
        <form id="frmTournament" role="form" @submit.prevent="save">
          <ValidationProvider
            slim
            v-slot="{ errors, classes }"
            rules="required|exact_length:1,Must select only one day of the week for playing"
          >
            <div :class="classes">
              <label class="control-label">Day(s) of the week played</label>
              <div class="checks">
                <label class="checkbox-inline">
                  <input type="checkbox" value="0" v-model="daysSelected">Sunday
                </label>
                <label class="checkbox-inline">
                  <input type="checkbox" value="1" v-model="daysSelected">Monday
                </label>
                <label class="checkbox-inline">
                  <input type="checkbox" value="2" v-model="daysSelected">Tuesday
                </label>
                <label class="checkbox-inline">
                  <input type="checkbox" value="3" v-model="daysSelected">Wednesday
                </label>
                <label class="checkbox-inline">
                  <input type="checkbox" value="4" v-model="daysSelected">Thursday
                </label>
                <label class="checkbox-inline">
                  <input type="checkbox" value="5" v-model="daysSelected">Friday
                </label>
                <label class="checkbox-inline">
                  <input type="checkbox" value="6" v-model="daysSelected">Saturday
                </label>
              </div>
              <span class="help-block" v-if="errors[0]">It failed - {{ errors[0] }}</span>
            </div>
          </ValidationProvider>
  
          <button type="button" :disabled="invalid">Save</button>
        </form>
      </ValidationObserver>
      Selected Days: {{ daysSelected }}
    </div>
  </template>
  
  <script>
  export default {
    name: "Demo",
    data() {
      return {
        daysSelected: []
      };
    },
    methods: {
      save() {
        console.log("Will save");
      }
    }
  };
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  </style>
  