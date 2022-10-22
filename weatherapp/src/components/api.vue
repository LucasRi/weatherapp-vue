<template>
    <h1>hello</h1>
    {{ info }}
</template>

<script>
import axios from 'axios'

export default {
    name: 'hello',
    data() {
        return {
            info: null
        }
    },
    mounted() {
        axios.get('https://api.openweathermap.org/data/2.5/weather?lat=48.148598&lon=17.107748&units=metric&lang=sk&appid=9a940b74ba054ec407a90bf5159392db')
        .then(response => (this.info = response))

        }
}
</script>
