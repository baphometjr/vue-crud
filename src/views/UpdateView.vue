<template>
    <div class="q-pa-md" style="max-width: 400px">
    <q-form @submit="onSubmit" class="q-gutter-md">
        <q-input v-model="id" label="ID" />
        <!-- <q-input v-model="fname" label="First Name" />
        <q-input v-model="lname" label="Last Name" />
        <q-input v-model="username" label="Username" />
        <q-input v-model="password" label="Password" />
        <q-input v-model="email" label="Email" />
        <q-input v-model="avatar" label="Avatar" /> -->
        <q-btn label="Submit" type="submit" color="primary" />
    </q-form>
</div>
</template>

<script setup>
import { ref } from 'vue';
import router from '../router';
import { useRoute } from 'vue-router';
const route = useRoute();

const id = ref(route.params.id)

// const fname = ref('Cat')
// const lname = ref('Chat')
// const username = ref('chat.chat@melivecode.com')
// const password = ref('1234')
// const email = ref('chat.chat@melivecode.com')
// const avatar = ref('https://melivecode.com/users/cat.png')
// const onSubmit = () => {
// var myHeaders = new Headers();
// myHeaders.append("Content-Type", "application/json");

// var raw = JSON.stringify({
//     "fname": fname.value,
//     "lname": lname.value,
//     "username": username.value,
//     "password": password.value,
//     "email": email.value,
//     "avatar": avatar.value
// });

// var requestOption = {
//     method: 'POST',
//     headers: myHeaders,
//     body: raw,
//     redirect: 'follow'
// };


// fetch("https://www.melivecode.com/api/users/create", requestOption)
// .then(response => response.json())
// .then(result => {
//     alert(result.message)
//     if (result.status === "ok") {
//         router.push('/')
//     }
// })
// .catch(error => console.log('error', error));
// }
</script>