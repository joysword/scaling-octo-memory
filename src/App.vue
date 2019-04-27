<template>
    <v-app>
        <v-toolbar app>
            <v-toolbar-title class="headline text-uppercase">
                <span>vue</span>&nbsp;
                <span class="font-weight-light">my travel history</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn
                    flat
                    href="/about"
            >
                <span class="mr-2">About</span>
            </v-btn>
            <v-btn
                    flat
                    href="https://github.com/joysword/scaling-octo-memory"
                    target="_blank"
            >
                <span class="mr-2">Github</span>
            </v-btn>
        </v-toolbar>
        <v-content>
            <Map/>
        </v-content>
    </v-app>
</template>

<script>
    import Map from './components/Map'

    export default {
        name: 'App',
        components: {
            Map
        },
        data () {
            return {
                //
            }
        }
    }
</script>
