<template>
    <div id="mainContainer">
        <div class="row">
            <div class="column">
                <div>
                    <span id="titleText">Help Them Today</span>
                    <p id="subtitleText">The Singapore Zoo is losing funds due to the pandemic and many animals are starving. 
                        Help them now by clicking on the button below and make a change now!</p>
                    <button v-on:click="contribute()" id="contributeButton" type="button">Contribute Now</button>
                </div>
            </div>
            <div class="column"></div>
        </div>
    </div>
</template>
<script>
export default {
    name: "Landing",
    data() {
        
    },
    methods: {
        contribute: function() {
            this.$router.push({ path: '/login' })
        }
    }
}
</script>
<style scoped>
#mainContainer {
    background-image: url("https://www.wallpaperup.com/uploads/wallpapers/2014/03/08/291262/d8902fad8ee915a9b4fe13b23902fc18-700.jpg");
    background-size: cover;
    color: white;
}
.row {
    height: 100vh;
    display: flex;
    flex-wrap: wrap;
}
.row:after {
    display: table;
    clear: both;
}
.column {
    width:50%;
    float:left;
    display: flex;
    flex-wrap: wrap;
    padding: 50px;
    margin-top: 80px
}
#titleText {
    font-size: 50px;
    font-weight: bold;
}
#subtitleText {
    font-size: 18px;
}
#contributeButton {
    background: #055684;
    border: none;
    outline: none;
    font-size: 25px;
    padding: 0px;
    color: white;
    width: 420px;
    height: 70px;
    border-radius: 100px;
    font-weight: bold;
}
#contributeButton:hover {
    color: #055684;
    background: white;
    transition: ease-in-out 200ms;
}
</style>