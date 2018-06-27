<template>
    <nav class="navbar navbar-expand navbar-dark bg-dark">
        <router-link to="/" class="navbar-brand">Home</router-link>
        <dropdown id="component-dropdown" :options="userOptions"></dropdown>
    </nav>
</template>

<script>
    import Dropdown from '@/components/dropdown'

    export default {
        components: {
            'dropdown': Dropdown
        },

        data () {
            return {
                selectedUser: 'Apple',
                userOptions: {
                    'Apple': 'Apple',
                    'Banana': 'Banana',
                    'Blueberry': 'Blueberry',
                    'Kiwi': 'Kiwi',
                    'Pear': 'Pear',
                    'Pineapple': 'Pineapple',
                    'Watermelon': 'Watermelon'
                }
            }
        }
    }
</script>
