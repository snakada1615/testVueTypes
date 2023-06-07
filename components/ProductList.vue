<script lang="ts" setup>
import {arrayOf, instanceOf} from 'vue-types';
import ListItem from './ListItem.vue';
import {Person, QaList} from "~/types";

defineProps({
  list: arrayOf(ListItem.props),
  person: instanceOf(Person),
  qaList: instanceOf(QaList)
});
</script>
<template>
  <div>
    <h4>Products list</h4>
    <ul>
      <list-item
          v-for="item in list"
          :key="item.id"
          :id="item.id"
          :description="item.description"
          :price="item.price"
          :status="item.status"
      />
      {{person}}
      {{qaList}}
    </ul>
  </div>
</template>
