<template>
    <q-drawer show-if-above v-model="leftDrawerOpen" side="left" behavior="desktop" :width="90">
        <div class="flex flex-center column q-mb-md q-mt-md">
            <q-list>
                <q-item clickable :active="link === 'user'" @click="link = 'user' " active-class="border">
                    <q-item-section avatar class="flex flex-center column">
                        <q-icon name="fas fa-user-circle" />
                    </q-item-section>
                </q-item>
                <q-item clickable :active="link === 'doc'" @click="link = 'doc' " active-class="border">
                    <q-item-section avatar class="flex flex-center column">
                        <q-icon name="fas fa-file-alt" />
                    </q-item-section>
                </q-item>
                <q-item clickable :active="link === 'shopping'" @click="link = 'shopping' " active-class="border">
                    <q-item-section avatar class="flex flex-center column">
                        <q-icon name="fas fa-shopping-basket" />
                    </q-item-section>
                </q-item>
                <q-item clickable :active="link === 'search'" @click="link = 'search' " round active-class="border">
                    <q-item-section avatar rounded class="flex flex-center column">
                        <q-icon round rounded name="fas fa-search" />
                    </q-item-section>
                </q-item>
            </q-list>
        </div>
        <div style="position: absolute; bottom:20px; margin-left:auto; margin-right:auto; left:0; right:0; text-align: center;">
            <div class="text-overline">EUR</div>
            <div class="text-overline">US</div>
        </div>
    </q-drawer>
</template>

<script>
import {ref} from "vue";
export default{
    setup() {
        const leftDrawerOpen = ref(false);
        return {
            link: ref("user"),
            leftDrawerOpen,
        }
    }
}
</script>

<style>
.border{
    background: #60c471;
    border-radius: 50%;
}
.q-item_section--side{
    padding-right: 0px !important;
}.q-item_section--avatar{
    color: black !important;
}
.q-item{
    padding: 16px 0px !important;
}
</style>