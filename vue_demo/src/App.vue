<template>
    <div>
        <div class="row">
            <div class="col-xs-offset-2 col-xs-8">
                <div class="page-header"><h2>Router Test</h2></div>
            </div>
        </div>

        <div class="row">
            <div class="col-xs-2 col-xs-offset-2">
                <div class="list-group">
                    <router-link to="/about" class="list-group-item">About</router-link>
                    <router-link to="/home" class="list-group-item">Home</router-link>
                </div>
            </div>
            <div class="col-xs-6">
                <div class="panel">
                    <div class="panel-body">
                        <keep-alive>
                            <router-view msg="123"></router-view>
                        </keep-alive>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "App"
}
</script>

<style>
</style>
