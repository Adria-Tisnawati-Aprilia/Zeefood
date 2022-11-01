<template>
    <div class="pesanan-sukses">
        <NavItem/>
        <div class="container">
            <div class="row justify-content-center mt-5">
                <div class="col text-center">
                    <img src="../assets/images/menunggu.png" width="300"/>
                    <h2><strong>Sukses!!</strong></h2>
                    <h4>Pesanan Anda sedang diproses <br> Mohon menunggu</h4>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import NavItem from '@/components/NavItem.vue';

export default {
    name : 'PesananSukses',
    components: {
        NavItem,
    },
};
</script>

<style>

</style>