<template>
    <div class="col-xs-12 col-sm-6">
        <ul class="list-group">
            <li class="list-group-item" v-for="(item, index) in 5" :key="index">
                POI TREE #{{ index }}
            </li>
        </ul>
    </div>
</template>

<script>

    export default {
        name: 'mapLeftSide',
        methods: {
        }

    }
</script>

<style>

</style>
