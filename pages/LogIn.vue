<template>
    <div class="background-title font-new">
        <div class="boardmargin">
            <hr class="stripe_border_t rounded-full">
            <hr class="stripe_border_b rounded-full">
            <hr class="stripe_border_l rounded-full">
            <hr class="stripe_border_r rounded-full">
                <div class="bg test bg-yellow-400 text-yellow-800">
                    <div class="ml-5 mb-32 text-shadow-sm">
                        <div class="explanation underbar-choco-login">
                            welcome to
                        </div>
                        <div class="titlesize underbar-pink-login">
                            Give Me Snack
                        </div>
                    </div>
                    <div class="text-6xl text-center">
                        <div class="flex flex-col">
                            <nuxt-link to="/SignUp" class="buttonsize border-3 shadow-xl text-shadow-sm  rounded-full bg-red-400 border-yellow-800 mx-64">
                            <img src="../assets/photo/round_coffee_white_24dp.png" class="o inline-block" style="width:1em, height:1em">
                                Sign Up
                                <div class="text-xs mt-3 border-yellow-800">
                                    Create an account
                                </div>
                            </nuxt-link>
                            
                            <nuxt-link to="/SignIn" class="buttonsize border-3 shadow-xl text-shadow-sm  rounded-full bg-red-400 border-yellow-800 mx-64">
                            <img src="../assets/photo/cookie.png" class="o inline-block" style="width:1em, height:1em">
                                Sign In
                                <div class="text-xs mt-3 border-yellow-800">
                                    Sign in to Give Me Snack
                                </div>
                            </nuxt-link>
                        
                        </div>
                    </div>
                </div>
        </div>
    </div>
</template>

<script>

export default {
  
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Hachi+Maru+Pop&family=Zen+Maru+Gothic:wght@500&display=swap');
* {
  font-family: 'Hachi Maru Pop' !important;
}
.underbar-choco-login {
    position: relative
}
.underbar-choco-login::after {
    content: '';
    position: absolute;
    top: 90%;
    left: 0;
    width: 25%;
    height: 8px;
    border-radius: 4px;
    background: linear-gradient(to right, #49130b 80%, #f2ba48 80%);
    box-shadow: 0 3px 8px #0008, 0 -3px 2px #0005 inset, 0 1px 2px #0001 inset;
}
.underbar-pink-login {
    position: relative
}
.underbar-pink-login::after {
    content: '';
    position: absolute;
    top: 100%;
    left: 0%;
    width: 80%;
    height: 8px;
    border-radius: 4px;
    background: linear-gradient(to left, #f2cc91 20%, #d98280 20%);
    box-shadow: 0 3px 8px #0008, 0 -3px 2px #0005 inset, 0 1px 2px #0001 inset;
}

.stripe_border_b
{
    position: absolute;
    margin: auto;
    width: 65.5em;
    height: 3em;
    top: 38em; bottom: 0px;
    left: 3em; right: 0px;
    background: repeating-linear-gradient(45deg, rgb(161, 20, 20), red 15px, rgb(161, 161, 161) 10px, white 30px);
    content: '';
    box-shadow: 0 3px 8px #0008, 0 -10px 2px rgba(0, 0, 0, 0.233) inset, 0 5px 2px rgba(255, 255, 255, 0.404) inset;
}
.stripe_border_t
{
    position: absolute;
    margin: auto;
    width: 65.5em;
    height: 3em;
    top: 0em; bottom: 32em;
    left: 0px; right: 3em;
    background: repeating-linear-gradient(45deg, rgb(161, 20, 20), red 15px, rgb(161, 161, 161) 10px, white 30px);
    content: '';
    box-shadow: 0 3px 8px #0008, 0 -10px 2px rgba(0, 0, 0, 0.233) inset, -10px 0 2px rgba(0, 0, 0, 0.233) inset, 0 5px 2px rgba(255, 255, 255, 0.404) inset, 5px 0 2px rgba(255, 255, 255, 0.404) inset;
}
.stripe_border_l
{
    position: absolute;
    margin: auto;
    width: 3em;
    height: 34.5em;
    top: 0.5em; bottom: 0em;
    left: 65.5em; right: 0px;
    background: repeating-linear-gradient(45deg, rgb(161, 20, 20), red 15px, rgb(161, 161, 161) 10px, white 30px);
    content: '';
    box-shadow: 3px 0 8px #0008, -10px 0 2px rgba(0, 0, 0, 0.233) inset, 0 -10px 2px rgba(0, 0, 0, 0.233) inset, 5px 2px 0 rgba(255, 255, 255, 0.404) inset, 0 5px 2px rgba(255, 255, 255, 0.404) inset;;
}

.stripe_border_r
{
    position: absolute;
    margin: auto;
    width: 3em;
    height: 34.5em;
    top: 6em; bottom: 0.5em;
    left: 0px; right: 65.5em;
    background: repeating-linear-gradient(45deg, rgb(161, 20, 20), red 15px, rgb(161, 161, 161) 10px, white 30px);
    content: '';
    z-index: 0;
    box-shadow: 3px 0 8px #0008, -10px 0 2px rgba(0, 0, 0, 0.233) inset, 0 -10px 2px rgba(0, 0, 0, 0.233) inset, 5px 2px 0 rgba(255, 255, 255, 0.404) inset, 0 5px 2px rgba(255, 255, 255, 0.404) inset;;
}


.background{
  background: repeating-linear-gradient(-45deg, #d0546a22, #d0546a22 40px, #d0546a 40px, #d0546a 80px);
}

.boardmargin{
    width: min(80vw,1000px);
    margin: 0 auto;
    margin-top: 5em;
}
.buttonsize{
    width: min(50vw,600px);
    margin: 10px auto;
}

@media screen and (min-width: 1000px){
    .titlesize{
        font-size: 5em;
        transition: 0.5s;
    }
    .explanation{
        font-size: 2em;
        transition: 0.5s;
    }
    .buttonsize{
        width: min(50vw,600px);
        margin: 10px auto;
        font-size: 1em;
    }
}

@media screen and (min-width: 500px) and (max-width: 1000px){
    .titlesize{
        font-size: 3em;
        transition: 0.5s;
    }
    .explanation{
        font-size: 1.5em;
        transition: 0.5s;
    }
    .buttonsize{
        width: min(50vw,600px);
        margin: 10px auto;
        font-size: 0.7em;
    }
}

@media screen and (max-width: 500px){
    .titlesize{
        font-size: 1.5em;
        transition: 0.5s;
    }
    .explanation{
        font-size: 1em;
        transition: 0.5s;
    }
    .buttonsize{
        width: min(50vw,600px);
        margin: 10px auto;
        font-size: 0.5em;
    }
}
.background-title {
    background: repeating-linear-gradient(-45deg, #d0546a22, #d0546a22 40px, #d0546a 40px, #d0546a 80px);
    min-height: 100vh;
    z-index: 99;
}
</style>