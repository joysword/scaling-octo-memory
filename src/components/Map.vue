<template>
    <div id="map-wrapper">
        <MglMap :accessToken="accessToken" :mapStyle.sync="mapStyle">
            <MglNavigationControl v-once :position="navControlPosition" />
        </MglMap>
    </div>
</template>

<script>
    import Mapbox from "mapbox-gl";
    import { MglMap, MglNavigationControl } from "vue-mapbox";

    export default {
        components: {
            MglMap,
            MglNavigationControl
        },
        data() {
            return {
                accessToken: 'pk.eyJ1Ijoiam95c3dvcmQiLCJhIjoiY2p0M2s0cHVxMmI1NTQzb3MxNzJyNzR1YSJ9.KH_S6LificYiQ6whJRAJFg',
                mapStyle: 'mapbox://styles/mapbox/streets-v11',
                navControlPosition: 'top-right'
            }
        },
        created() {
            this.mapbox = Mapbox;
        }
    }
</script>

<style scoped>
    #map-wrapper {
        width: 100%;
        height: 100%;
    }
</style>