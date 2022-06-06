<template>
    <v-app id="inspire">

        <v-container fluid fill-height>
            <v-layout align-center justify-center>
                <v-flex xs12 sm8 md4>
                    <v-card class="elevation-12">
                        <v-toolbar dark color="primary">
                            <v-toolbar-title>Login form</v-toolbar-title>
                        </v-toolbar>
                        <v-card-text>
                            <v-form>
                                <v-text-field autocomplete="false" color="primary" placeholder="emailModel"
                                    v-model="emailModel" filled :rules="username" name="login" label="username"
                                    type="text">
                                </v-text-field>
                                <v-text-field autocomplete="false" v-model="passwordModel" filled placeholder="password"
                                    :rules="password" id="password" name="password" label="Password" type="password">
                                </v-text-field>
                            </v-form>
                        </v-card-text>
                        <v-card-actions>
                            <v-spacer></v-spacer>
                            <v-btn @click.prevent="login" block rounded color="primary">Login</v-btn>
                        </v-card-actions>
                    </v-card>
                </v-flex>
            </v-layout>
        </v-container>

    </v-app>
</template>

<script>
export default {
    data: () => ({
        emailModel: '',
        passwordModel: '',
        username: [
            value => !!value || 'email required.',

        ],
        password: [
            value => !!value || 'password required.',
            value => (value && value.length >= 5) || 'Min 5 characters',
        ],
    }),
    methods: {
        login() {
            if (this.emailModel === 'admin' && this.passwordModel === 'admin') {
                this.$router.push('/')
            }
        }
    }
}
</script>

<style>
.theme--dark.v-input input,
.theme--dark.v-input textarea {
    color: #000;
}

.theme--dark.v-card {
    background-color: #fff;
    /* color: #FFFFFF; */
}
</style>