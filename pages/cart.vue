<template>
    <v-app>

        <v-simple-table style="height:170px" class="mt-3 pink">
            <template v-slot:default>
                <thead>
                    <tr>
                        <th class="text-left">
                            product
                        </th>
                        <th class="text-left">
                            price
                        </th>
                        <th class="text-left">
                            quantity
                        </th>
                        <th class="text-left">
                            subtotal
                        </th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>
                            <v-img class="mt-3" max-height="60" max-width="110" src="img9.jpg"
                                style="width:230px;height:170px" alt="">
                            </v-img>

                        </td>
                        <td>130</td>
                        <td>3</td>
                        <td>5</td>
                        <td>
                            <v-icon style="cursor:pointer" large color="white ">
                                {{ icons.mdiDelete }}
                            </v-icon>
                        </td>
                    </tr>
                </tbody>
            </template>
        </v-simple-table>
    </v-app>

</template>

<script>
import {
    mdiDelete,
} from '@mdi/js'
export default {
    data: () => ({
        icons: {

            mdiDelete,
        },
    }),
}
</script>

<style>
</style>