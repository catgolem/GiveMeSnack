<template>
    <div class="boardmargin p-12 py-16 bg bg-black rounded-3xl ">
        <div class="mb-32">
            <div class="explanation text-red-400">
                welcome to
            </div>
            <div class="text-red-400 titlesize">
                Give Me Snack
            </div>
        </div>
        <div class="text-red-400 text-6xl text-center">
            <button class="buttonsize border-3 rounded-full border-red-300 mx-64">
                Sign in
                <div  class="text-xs mt-3">
                    Sign in to Give Me Snack
                </div>
            </button>
            <button class="buttonsize border-3 rounded-full border-red-300 mx-64">
                Sign Up
                <div class="text-xs mt-3">
                    Create an account
                </div>
            </button>
        </div>
    </div>
</template>

<script>

export default {
  
}
</script>

<style>

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

@media screen and (max-width: 1000px){
    .titlesize{
        font-size: 2em;
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

</style>