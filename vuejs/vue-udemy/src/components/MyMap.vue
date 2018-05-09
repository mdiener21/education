<template>
    <div class="row">
        <map-sidebar></map-sidebar>
        <div class="col-xs-12 col-sm-6" id="mymap">is this a super map</div>

    </div>


</template>
<script>

    import 'ol/ol.css';
    import Map from 'ol/map';
    import View from 'ol/view';
    import TileLayer from 'ol/layer/tile';
    import XYZ from 'ol/source/xyz';
    import MapSideBar from "./MapSideBar.vue";

    export default {
        name: 'mymap',
        components: {
            "map-sidebar" : MapSideBar

        },
        methods: {
            initMap(){
                new Map({
                        target: 'mymap',
                        layers: [
                            new TileLayer({
                            source: new XYZ({
                                url: 'https://{a-c}.tile.openstreetmap.org/{z}/{x}/{y}.png'
                            })
                            })
                        ],
                        view: new View({
                            center: [1587952.987396, 5879660.425867],
                            zoom: 16
                        })
                    })


            }
        },
        mounted() {
            this.initMap()
        }

    }
</script>

<style>
    #mymap {
    width: 100%;
    }
</style>
