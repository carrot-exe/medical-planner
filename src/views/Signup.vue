<template>
  <v-form v-model="valid">
    <v-container fill-height>
      <v-row align="center"
    justify="center">

        <v-col
          cols="12"
          md="4"
          align="center"
        > 
          <div align="left">
          <v-btn
            class="ma-2"
            color="orange darken-2"
            dark
            href="/"
          >
            <v-icon
              dark
              left
            >
              mdi-arrow-left
            </v-icon>Back
          </v-btn>
        </div>
        <v-img
              src="../assets/login.png"
              contain="true"
              max-height="700"
              position="center"
          ></v-img>
          <div>
          <v-text-field
            v-model="user"
            :rules="userR"
            label="username"
            required
          ></v-text-field>
          <v-text-field
            :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
            :type="show1 ? 'text' : 'password'"
            name="input-10-2"
            label="password"
            @click:append="show1 = !show1"
          ></v-text-field>
          <v-text-field
            name="nombre"
            label="nombre"
          ></v-text-field>
          <v-text-field
            name="ap_p"
            label="apellido paterno"
          ></v-text-field>
          <v-text-field
            name="ap_m"
            label="apellido materno"
          ></v-text-field>
          <v-text-field
            name="tel"
            label="telefono"
          ></v-text-field>
          <v-text-field
            name="dir"
            label="direccion"
          ></v-text-field>
        </div>
         <div>
          <v-btn
            class="ma-2"
            color="success"
            dark
            href="/login"
          >
            Register
            <v-icon
              dark
              right
            >
              mdi-checkbox-marked-circle
            </v-icon>
          </v-btn>

        </div>
          <br>
          <br>
          <br>
          <br>
          <p>If you have an account, <a href="/login">Log In</a>.</p>
        </v-col>
      </v-row>
    </v-container>
  </v-form>
</template>

<script>
  export default {
    data: () => ({ 
      show1: false,
      show2: true,
      show3: false,
      show4: false,
      valid: false,
      user: '',
      userR: [
        v => !!v || 'username is required',
      ],
      pass: '',
      required: [
        v => !!v || 'password is required',
      ],
    }),
    methods: {
      link(){
        
      }
    }
  }
</script>