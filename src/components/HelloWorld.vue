<template>
  <v-container>
    <v-btn @click="isDialogVisible = !isDialogVisible">
      Dialog
    </v-btn>

    <v-dialog v-model="isDialogVisible">
      <v-card>
        <v-card-text>
          <v-list>
            <v-list-item v-for="i in 75" :key="i" prepend-icon="mdi-home">
              <v-list-item-title>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem provident quo ullam
                voluptate officiis ut, at, expedita molestiae dolore quis nemo hic repellat fugit vitae recusandae ex,
                debitis ad dolor!
              </v-list-item-title>

              <template #append>
                <v-btn>Close</v-btn>
              </template>
            </v-list-item>
          </v-list>
        </v-card-text>
      </v-card>
    </v-dialog>
  </v-container>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const isDialogVisible = ref(false)
</script>
