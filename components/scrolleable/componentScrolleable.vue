<template>

    <div class="fixed">
        <div class=" grid grid-cols-3 gap-y-3 gap-x-4   ml-[15rem]"
            style=" transform: skew(-10deg, 20deg) rotate(-4deg) matrix3d(1, 0, 0, 0, -1, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);">
            <div v-for="i in 10" :key="i">
                <div class="capaUnoScroll">
                    <div class="capaDosScroll ">
                        <div class="capaTres ">
                            <div
                                class="bg-gradient-to-r from-white to-gray-300 border-4 border-black rounded-lg capaTresScroll">
                                <img src="/diseno.png " alt="" class="img">
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'componentScrolleable'
}
</script>

<style>
.capaUnoScroll {
    border-radius: 10px;
    background: rgba(40, 39, 46, 0.301);

}

.capaDosScroll {
    border-radius: 10px;
    background: rgba(255, 255, 255, 0.753);
    transition-duration: 700ms;

}

.capaTresScroll {
    border-radius: 10px;
    width: fit-content;
    transition-duration: 700ms;

}


@media (hover: hover) {

    .capaDosScroll:hover {
        transform: translatex(-1.05rem) translatey(-1rem);
        transition-duration: 700ms;

    }

    .capaTresScroll:hover {
        transform: translatex(-1.09rem) translatey(-1.05rem);
        transition-duration: 700ms;
       

    }

    .img:hover{
        transform: translatex(-7rem) translatey(-5rem) matrix3d(1, 0, 0, 0, 1, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
        transition-duration: 700ms;
       /* transform: matrix3d(1, 0, 0, 0, 1, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);*/
    }


}
</style>