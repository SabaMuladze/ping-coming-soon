
<template>
    <div class="flex flex-col w-full min-h-screen items-center">
        <div class="mt-20 px-12 w-full flex flex-col gap-8 items-center">
            <p class="text-[25px] font-bold flex">PING<span class="text-[#4C7BF3] h-1 w-1 ">.</span></p>
            <div class="flex flex-col gap-3">
                <h2 class="text-[26px] text-[#969696] font-light">We are launching <strong class="text-black">soon!</strong>
                </h2>
                <p class="font-thin flex justify-center">Subscribe and get notified</p>
            </div>
            <div class="w-full flex flex-col gap-[10px] max-w-[700px]">
                <div class="w-full h-10 rounded-3xl border-[2px] border-[#4C7BF3] flex items-center py-1 px-3 pl-3">
                    <input class="font-light outline-none w-full h-full text-sm" type="email"
                        placeholder="Your email address…">
                </div>
                <button class="w-full h-10 bg-[#4C7BF3] rounded-3xl font-semibold text-white">Notify Me</button>
            </div>
        </div>
        <div class="px-6 w-full mt-16">
            <div class="img"></div>
        </div>
    </div>
</template>

<script >

</script>

<style>
.img {
    background-image: url('./assets/illustration-dashboard-mobile.png');
    background-repeat: no-repeat;
    background-size: contain;
    background-position: center;
    width: 100%;
    min-height: 200px;
    height: calc(5px + 5vh);
    padding: 10%;

}
</style>
