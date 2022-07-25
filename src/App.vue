<template>
  <v-app>
      
    <v-main>
      <FormHelper>
          <div slot="form-header">
            <h1>This is the title of the form</h1>
            <p>Information about the form</p>
          </div>
          <div slot="form-fields">
               <input type="text" placeholder="Name" required />
               <input type="password" placeholder="Password" required />
          </div>
          <div slot="form-controls" >
              <button v-on:click="handleSubmit" >Submit</button>
          </div> 
      </FormHelper>
   
    <!-- Named slots -->
    <h1>Named Slots</h1>
    <NamedSlot class="named">
        <template v-slot:header >
          <h1>Card Header</h1>
        </template>
        <template v-slot:default>
          <h1>Content of the Card</h1>
          <img src="https://media.istockphoto.com/photos/black-panther-picture-id168415745?k=20&m=168415745&s=612x612&w=0&h=QmMOsBdUxmtENuYZpAbI8MXOo3NrE0X4WdZvsqrUi28=" >
        </template>
        <template v-slot:footer>
          <h1>Foooter of the card</h1>
        </template>
    </NamedSlot>


      <!-- Slots as Props -->
        <h2>Slots as Props</h2>
           <SlotsProps>
            <template v-slot:default="slotProps" >              
                    {{slotProps.username}} {{slotProps.lastname}}
            </template>     
           </SlotsProps>

           <SlotsProps>
            <template v-slot:default="slotProps" >              
                    {{slotProps.name}}, {{slotProps.email}}
            </template>     
           </SlotsProps>

           <SlotsProps>
            <template v-slot:default="slotProps" >              
                    {{slotProps.email}}
            </template>     
           </SlotsProps>
      
    </v-main>

  </v-app>
</template>

<script>
import FormHelper from './components/FormHelper.vue';
import SlotsProps from './components/SlotsProps.vue';
import NamedSlot from './components/NamedSlot.vue';

export default {
  name: 'App',

  components: {
    FormHelper,
    SlotsProps,
    NamedSlot
},

  data: () => ({
    title:'I am a dynamic slot title'
  }),
};
</script>

<style scoped>

  img{
    width: 15rem;
    height: 15rem;
  }

  .named{
    max-width: 500px;
    display: flex;
    justify-content: center;
    align-content: center;
    align-items: center;
    flex-direction: column;
  }

</style>
