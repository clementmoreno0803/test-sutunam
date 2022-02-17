<template>
      <div class="sub_menu">
        <table>
          <tr v-for='(item,index) in items' :key="index">{{item.category}}</tr>
        </table>
      </div>
</template>

<script>
export default {
name:'ProductDropdown',
props: ['items']
}
</script>

<style>

</style>
