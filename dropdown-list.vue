<template>
    <div>
        <li class="nav-item dropdown" :class="{ 'show': showDropDown}">
            <a href="#" v-on:click.prevent="showDropDown=!showDropDown" class="nav-link dropdown-toggle">First Last</a>
            <div v-if="showDropDown" class="dropdown-menu" :class="{ 'show': showDropDown}">
                <a class="dropdown-item" href="#" v-for="(option, name) in options" :value="option">{{ name }}</a>
            </div>
        </li>
    </div>
</template>

<script>

    export default {
        data() {
            return {
                showDropDown: true,
            }
        },
        props: {
            options: {
                type: Object,
                required: true
            }
        },

    }
</script>
