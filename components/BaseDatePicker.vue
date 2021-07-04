<template>
  <v-dialog ref="dialog" :return-value.sync="date" width="290px">
    <template #activator="{ on }">
      <base-text-field v-model="date" readonly v-bind="$attrs" v-on="on"/>
    </template>
    <v-date-picker v-model="date" >

      <v-spacer />
      <v-btn text @click="$emit('cancel')">Cancel</v-btn>
      <v-btn color="primary" @click="$refs.dialog.save(date)">OK</v-btn>
    </v-date-picker>
  </v-dialog>
</template>

<script>
export default {
  data () {
    return {
      date: null
    }
  }
}
</script>
