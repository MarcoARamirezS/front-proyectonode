<template>
  <v-card width="400" shaped class="card">
    <v-card-title>Iniciar Sesión</v-card-title>
    <v-card-text>
      <v-form ref="form" v-mode="valid" lazy-validation>
        <v-text-field
          v-model="usuario"
          :rules="rulesUsuario"
          required
          label="User"
          placeholder="Write your user"
        />
        <v-text-field
          v-model="password"
          :rules="rulesUsuario"
          required
          label="Password"
          placeholder="Write your password"
        />
      </v-form>
    </v-card-text>
    <v-card-actions>
      <v-btn>
        Login
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data () {
    return {
      valid: false,
      usuario: '',
      password: '',
      rulesUsuario: [
        v => !!v || 'Usuario is required'
      ]
    }
  }
}
</script>

<style scoped>
.card {
background: #90CAF9;
}
</style>
