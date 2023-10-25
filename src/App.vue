
<template>
    <div class="flex flex-col w-full min-h-screen items-center">
        <div class="mt-20 px-12 w-full flex flex-col gap-8 items-center">
            <p class="text-[25px] font-bold flex md:text-[32px]">PING<span class="text-[#4C7BF3] h-1 w-1 ">.</span></p>
            <div class="flex flex-col gap-3">
                <h2 class="text-[26px] text-[#969696] font-light md:text-5xl">We are launching <strong
                        class="text-black">soon!</strong>
                </h2>
                <p class="font-thin flex justify-center md:text-xl">Subscribe and get notified</p>
            </div>
            <div class="w-full flex flex-col gap-[10px] max-w-[700px] md:flex-row">
                <div :style="{ border: error ? 'red solid 1px' : '' }"
                    class="w-full h-10 rounded-[28px] border-[1px] border-[#4C7BF3] flex items-center py-1 px-3 pl-3 md:flex-[150%] md:h-[56px]">
                    <input class="font-light outline-none w-full h-full text-sm md:text-base" type="email"
                        placeholder="Your email address…">
                </div>
                <button class="w-full h-10 bg-[#4C7BF3] rounded-[28px] font-semibold text-white md:h-[56px]">Notify
                    Me</button>
            </div>
        </div>
        <div class="px-6 w-full mt-16 flex justify-center">
            <div class="img"></div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            error: true
        }
    },
    methods: {

    },
}

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

}

@media (min-width:700px) {
    .img {
        background-image: url('./assets/illustration-dashboard-desktop.png');
        background-repeat: no-repeat;
        background-size: contain;
        background-position: center;
        min-width: 650px;
        max-width: 700px;
        min-height: 350px;
        height: calc(5px + 5vh);
    }
}
</style>
