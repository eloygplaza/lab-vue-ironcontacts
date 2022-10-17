<template>

    <div class="section">
        <div class="container">
            <h1 class="title is-1">Iron contacts</h1>

            <table class="table">
                <tr>
                    <th>Picture</th>
                    <th>Name</th>
                    <th>Popularity</th>
                    <th>Won Oscar</th>
                    <th>Won Emmy</th>
                </tr>
                <tr v-for="contact in contacts">
                    <td><img  :src="`${contact.pictureUrl}`" class='image is-128x128' style="object-fit: cover;" alt=""></td>
                    <td>{{contact.name}}</td>
                    <td>{{contact.popularity}}</td>
                    <td></td>
                    <td></td>
                </tr>
            </table>
        </div>
    </div>
    
</template>
<script setup>
    import allContacts from './data/contacts.json';

    const contacts = allContacts.slice(0,5);

    console.log(contacts);
</script>
<style scoped>
</style>