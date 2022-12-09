<template>
    <div>
        <div  :class="$route.name=='static' ? ['bg-transparent px-6 pt-8 flex justify-between  fixed z-50 w-auto'] : ['bg-transparent px-6 pt-8 flex justify-between  w-full fixed z-50']" >
            <div>
                <h1 class="text-9xl font-bold text-blue-900">Animation Nuxtjs</h1>
                <p class="text-white font-bold drop-shadow-lg text-xl " >Decorative & interective & sexo</p>
                <div class="py-4 flex ">
                    <div v-for="(item, i) in NavItems" :key="i">
                        <NuxtLink :to="item.path" class="m-2  text-blue-900 font-bold hover:text-red-900 duration-300"> <span >{{ item.name }}</span>
                        </NuxtLink>
                    </div>
                </div>
            </div>
            <Icons-Menu-Icon v-if="$route.name!='static'" class="text-white  drop-shadow-lg "></Icons-Menu-Icon>
        </div>
        <div>
            <Nuxt />
        </div>
    </div>
</template>

<script>
export default {
    name: "LayoutDefault",
    data() {
        return {
            NavItems: [
                { name: 'Scrolleable', path: '/scrolleable' }, {
                    name: 'Static', path: '/static'
                }]
        }
    }

}
</script>
<style>
a.nuxt-link-active {
    color: rgb(239, 68, 68) ;
}
</style>

