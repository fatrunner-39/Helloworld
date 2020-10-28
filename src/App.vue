<template>
  <v-app>
    <v-main 
      v-for="(i) in 5"
      :key="i"
      >  
      <div class="text-center">
        
        <v-dialog
          width="800"
        >
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              color="red lighten-2"
              width="800"
              dark
              v-bind="attrs"
              v-on="on"
            >
              Click Me
            </v-btn>
          </template>

          <v-card>
            <v-card-title class="blue">
              Privacy Policy
            </v-card-title>

            <v-card-text>
              Lokomotiv Moscow
            </v-card-text>

            <v-divider></v-divider>

            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn
                color="primary"
                text
                click="dialog = false"
              >
                I accept
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
      </div>
    </v-main>
  </v-app>
</template>

<script>

export default {
  

  data: () => ({
    //
    dialog:false
  }),
};
</script>
