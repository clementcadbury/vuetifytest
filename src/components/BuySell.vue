<template>
    <v-card class="mx-auto" prepend-icon="mdi-gender-transgender">
        <template v-slot:title>
            <div class="text-right">
                <v-btn variant="tonal">
                    Buy
                </v-btn>
                <v-btn>
                    Sell
                </v-btn>
            </div>
        </template>

        <v-card-text class="pt-2">
            <v-card class="pa-2">
                <v-row>
                    <v-col>
                        <v-text-field label="you pay" placeholder="0" persistent-placeholder hide-details="auto"
                            variant="plain" value="1000"></v-text-field>
                    </v-col>
                    <v-col cols="4"><v-select :items="['agEUR', 'LVMH']" value="agEUR"
                            hide-details="auto"></v-select></v-col>
                </v-row>
            </v-card>
            <v-card class="mt-2 pa-2">
                <v-row>
                    <v-col>
                        <v-text-field label="you get" placeholder="0" persistent-placeholder hide-details="auto"
                            variant="plain" value="64"></v-text-field>
                    </v-col>
                    <v-col cols="4"><v-select :items="['agEUR', 'LVMH']" value="LVMH"
                            hide-details="auto"></v-select></v-col>
                </v-row>
            </v-card>
            <div class="my-2" style="text-align: center;">1 LVMH = 15.26 agEUR</div>
            <v-expansion-panels v-model="panel">
                <v-expansion-panel expand title="details">
                    <v-expansion-panel-text>
                        <div class="my-2" style="text-align: center;">1000 agEUR is all you pay, fees included</div>
                        <v-row>
                            <v-col>Ramp fee</v-col>
                            <v-col style="text-align: right;">2.32 agEUR</v-col>
                        </v-row>
                        <v-row class="mt-0">
                            <v-col>Network fee <v-icon icon="mdi-information-outline" size="small"></v-icon></v-col>
                            <v-col style="text-align: right;">6.71 agEUR</v-col>
                        </v-row>
                        <v-row>
                            <v-col>Total fee</v-col>
                            <v-col style="text-align: right;">9.03 agEUR</v-col>
                        </v-row>
                    </v-expansion-panel-text>

                </v-expansion-panel>
            </v-expansion-panels>
            <div class="my-4" style="text-align: center;">Estimated time : 17 minutes</div>
            <v-btn block size="x-large">
                <v-row>
                    <v-col>Proceed</v-col>
                    <v-col style="text-align: right;">></v-col>
                </v-row>
            </v-btn>
        </v-card-text>
    </v-card>
</template>

<script>
export default {
    data: () => ({
        panel: [0],
    }),
}
</script>