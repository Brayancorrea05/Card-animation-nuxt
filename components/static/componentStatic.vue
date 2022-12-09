<template>
    <div class=" relative bottom-[15rem]">
        <div class=" grid grid-cols-3 gap-y-3 gap-x-4  fixed ml-[15rem]"
            style=" transform: skew(-10deg, 20deg) rotate(-4deg) matrix3d(1, 0, 0, 0, -1, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);">
            <div v-for="i in 25" :key="i">
                <div class="capaUno">
                    <div class="capaDos ">
                        <div class="capaTres ">
                            <div class="capaCuatro p-2  ">
                                <img class="w-full rounded-lg "
                                    :src="`https://picsum.photos/id/${Math.floor(Math.random() * 7) * i}/400/250`">
                                <!--  <img src="/diseno.png " alt="" class="rounded-lg">-->
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
    name: 'componentStatic',
    data() {
        return {
        }
    },

}
</script>

<style scoped>
.capaUno {
    border-radius: 10px;
    background: rgba(20, 0, 130, 0.733);

}

.capaDos {
    height: 100%;
    border-radius: 10px;
    background: rgba(50, 5, 82, 0.452);
    transition-duration: 700ms;
   
}

.capaTres {
    height: 100%;
    border-radius: 10px;
    background: rgba(81, 117, 170, 0.747);
    transition-duration: 700ms;

}

.capaCuatro {
    height: 100%;
    border-radius: 10px;
    background: rgb(0, 61, 130);
    border: 1px solid;
    transition-duration: 700ms;

}

img {
    width: 100%;
}

@media (hover: hover) {

    .capaDos:hover {
        transform: translatex(-1.05rem) translatey(-1rem);
        transition-duration: 700ms;
       
    }

    .capaTres:hover {
        transform: translatex(-1.09rem) translatey(-1.05rem);
        transition-duration: 700ms;
      
    }

    .capaCuatro:hover {
        transform: translatex(-1rem) translatey(-1rem);
        transition-duration: 700ms;
       
    }

}
</style>