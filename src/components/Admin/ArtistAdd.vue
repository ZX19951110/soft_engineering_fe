<template>
    <div>
    <div id="content">
        <div id="title">Add New Artist</div>
        <img id="photo" src="2.jpg"/>
        <button id="upload">Upload Picture</button>
        <button id="publish" v-on:click="upload">Publish</button>
        <div id="basic">
            <p>Basic Information</p>
            <label for="name">Name</label>
            <input id="name" type="text">
            <label for="position">Position</label>
            <input id="position" type="text">
            <label for="description">Description</label>
            <textarea id="description" ></textarea>
        </div>
    </div>
    <div id="introduce">
        <img id="admin_head" src="2.jpg">
        <ul id="functions">
            <li>Function1</li>
            <li>Function2</li>
            <li>Function3</li>
            <li>Function4</li>
        </ul>
    </div>
    </div>
</template>

<script>
    import Vue from 'vue'
    import axios from 'axios'
    import VueAxios from 'vue-axios'
    Vue.use(VueAxios, axios)
    export default {
        name: "ArtistAdd",
        methods: {
            upload: function () {
                Vue.axios.get('https://api.coindesk.com/v1/bpi/currentprice.json')
                    .then(function(response){window.console.log(response)})
            }
        }
    }
</script>

<style scoped>
    #content{
        border-style: solid;
        border-color: #c96567;
        border-width: 2px;
        position: absolute;
        width: 700px;
        height: 600px;
        left: 130px;
    }
    #title{
        height: 30px;
        font-size: 18px;
        color: #ffffff;
        background-color: #c96567;
        vertical-align: middle;
    }
    #introduce {
        left: 1030px;
        width: 300px;
        height: 600px;
        border-style: solid;
        border-color: #c96567;
        border-width: 2px;
        position: absolute;
    }
    #photo{
        margin-top: 25px;
        margin-left: 30px;
        width: 210px;
        height: 290px;
        position: absolute;
        top: 30px;
        left: 0px;
    }
    #basic{
        top: 55px;
        left: 270px;
        position: absolute;
        height: 290px;
        width: 350px;
        margin-left: 30px;
    }
    #basic p{
        margin-top: 0px;
        font-size: 24px;
        margin-bottom: 10px;
        text-align: left;
    }
    #basic label{
        display: block;
        margin-top: 13px;
        padding: 5px;
        font-size: 14px;
        text-align: left;
    }
    #name{
        border-style: solid;
        border-color: #c96567;
        border-width: 1px;
        position: absolute;
        top: 33px;
        left: 80px;
        margin-top: 10px;
        margin-left: 10px;
        height: 20px;
        width: 250px;
    }
    #position{
        border-style: solid;
        border-color: #c96567;
        border-width: 1px;
        position: absolute;
        top: 73px;
        left: 80px;
        margin-top: 10px;
        margin-left: 10px;
        height: 20px;
        width: 250px;
    }
    #description{
        resize: none;
        border-style: solid;
        border-color: #c96567;
        border-width: 1px;
        position: absolute;
        top: 113px;
        left: 80px;
        margin-top: 10px;
        margin-left: 10px;
        height: 161px;
        width: 250px;
    }
    #upload{
        color: white;
        display: block;
        position: absolute;
        top : 365px;
        left: 70px;
        background-color: #c96567;
        border-radius:75px;
        width: 130px;
    }
    #publish{
        color: white;
        display: block;
        position: absolute;
        top : 365px;
        left: 510px;
        background-color: #c96567;
        border-radius:75px;
        width: 130px;
    }
    #admin_head{
        position: absolute;
        height: 100px;
        width: 100px;
        left: 100px;
        top: 50px;
        border-radius: 50%;
    }
    #functions{
        position: absolute;
        top: 200px;
        left: 50px;
        width: 200px;
        list-style-type: none;
        text-align: center;
        padding: 0px;
    }
    #functions li{
        margin-top: 20px;
        text-decoration:underline;
        text-decoration-color: #c96567;
    }
</style>