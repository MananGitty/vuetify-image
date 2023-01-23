<template>
    <v-navigation-drawer 
    expand-on-hover
    rail>
    <v-list>
          <v-list-item
            prepend-avatar="https://randomuser.me/api/portraits/men/85.jpg"
            title="Abdul Manan"
            subtitle="abdulmanan@gmail.com"
          ></v-list-item>
        </v-list>

        <v-divider/>

            <v-list density="compact" nav>
                <v-list-item
                prepend-icon="mdi-image"
                title="Color Gallery"
                value="color"
                @click="selectOption(true)"
                />
                <v-list-item
                prepend-icon="mdi-dialpad"
                title="Grey Scale"
                value="color"
                @click="selectOption(false)"
                />
            </v-list>

    </v-navigation-drawer>
</template>

<script setup>
import { defineEmits } from 'vue';

    const emits = defineEmits (['selectOption',])
     const selectOption =(isColor) =>{
        emits('selectOption', isColor)
    }



</script>