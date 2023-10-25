
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
                <div class="md:flex-[150%] md:h-[56px]">
                    <div :style="{ border: error ? '#FF5466 solid 1px' : '' }"
                        class="w-full h-10 rounded-[28px] border-[1px] border-[#4C7BF3] flex items-center py-1 px-3 pl-3 md:flex-[150%] md:h-[56px]">
                        <input v-model="email" class="font-light outline-none w-full h-full text-sm md:text-base"
                            type="email" placeholder="Your email address…">
                    </div>
                    <p v-show="error" class="text-[#FF5466] text-xs md:text-sm ml-4">Please provide a valid email address
                    </p>
                    <p v-show="sent" class="ml-4 text-[#2ECC71]">Good job !</p>
                </div>
                <button @click="validateEmail"
                    class="w-full h-10 bg-[#4C7BF3] rounded-[28px] font-semibold text-white md:h-[56px] hover:opacity-75">Notify
                    Me</button>
            </div>
        </div>
        <div class="px-6 w-full mt-16 flex justify-center">
            <div class="img"></div>
        </div>
        <footer class="w-full flex flex-col items-center justify-end absolute bottom-12">
            <div>
                <ul class="flex gap-6">



                    <a href="https://www.facebook.com/" target="_blank">
                        <li
                            class="w-[30px] h-[30px] rounded-full border-[1px] border-gray-200 hover:bg-[#4C7BF3] flex items-center justify-center">
                            <i @mouseover="iconOver" @mouseout="iconOut" class="fa-brands fa-facebook-f hover:text-white"
                                style="color: #4C7BF3; padding: 10px;"></i>
                        </li>
                    </a>
                    <a href="https://twitter.com/" target="_blank">
                        <li
                            class="w-[30px] h-[30px] rounded-full border-[1px] border-gray-200 hover:bg-[#4C7BF3] flex items-center justify-center">
                            <i @mouseover="iconOver" @mouseout="iconOut" class="fa-brands fa-twitter hover:text-white"
                                style="color: #4C7BF3; padding: 10px;"></i>
                        </li>
                    </a>
                    <a href="https://www.instagram.com/" target="_blank">
                        <li
                            class="w-[30px] h-[30px] rounded-full border-[1px] border-gray-200 hover:bg-[#4C7BF3] flex items-center justify-center">
                            <i @mouseover="iconOver" @mouseout="iconOut" class="fa-brands fa-instagram hover:text-white"
                                style="color: #4C7BF3; padding: 10px;"></i>
                        </li>
                    </a>
                </ul>
            </div>
            <p class="mt-6 text-[#9B9B9B]">© Copyright Ping. All rights reserved.</p>
        </footer>
    </div>
</template>

<script>
export default {
    data() {
        return {
            error: false,
            email: '',
            sent: false
        }
    },
    methods: {
        validateEmail() {
            if (this.emailValidate(this.email)) {
                this.error = false;
                this.sent = true;
            }
            else if (this.email.length == 0) {
                this.error = false;
            }
            else {
                this.error = true
            }
        },
        emailValidate(email) {
            const emailPattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}$/;
            return emailPattern.test(email);
        },
        iconOver(event) {
            let tar = event.target;
            tar.style.color = 'white'
        },
        iconOut(event) {
            let tar = event.target;
            tar.style.color = '#4C7BF3'
        }
    }
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
