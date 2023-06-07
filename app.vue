<script setup lang="ts">
import ProductList from './components/ProductList.vue';
import { reactive } from 'vue';
import {Person, QaList} from "~/types";

const list = [
  {
    id: 1,
    description: 'Item 1',
    price: 1.5,
  },
  {
    id: 2,
    description: 'Item 2',
    price: 20.0,
  },
  {
    id: 3,
    description: 'Item 3',
    price: 1.99,
  },
  {
    id: 4,
    description: 'Item 4',
    status: 'sold out',
  },
];
const person =new Person('nakada', 'nomuyuki')
const qaList = new QaList(
    'test title',
    30,
    [
      {
        category: 'type a',
        categoryId: 'a1',
        categoryScore: 25,
        questionList: [
          {
            questionText: 'this is question a1',
            questionId: 'a1-01',
            ansState: false,
            singleScore: 0,
            answerOptions: [
              {
                optionText: 'this is choice a1-01-option1',
                optionScore: 0,
                optionId: 'a1-01-option1',
              },
              {
                optionText: 'this is choice a1-01-option2',
                optionScore: 1,
                optionId: 'a1-01-option2',
              },
              {
                optionText: 'this is choice a1-01-option3',
                optionScore: 2,
                optionId: 'a1-01-option3',
              },
              {
                optionText: 'this is choice a1-01-option4',
                optionScore: 3,
                optionId: 'a1-01-option4',
              },
              {
                optionText: 'this is choice a1-01-option5',
                optionScore: 4,
                optionId: 'a1-01-option5',
              },
            ],
          },
          {
            questionText: 'this is question a2',
            questionId: 'a1-02',
            ansState: false,
            singleScore: 0,
            answerOptions: [
              {
                optionText: 'this is choice a1-02-option1',
                optionScore: 0,
                optionId: 'a1-02-option1',
              },
              {
                optionText: 'this is choice a1-02-option2',
                optionScore: 1,
                optionId: 'a1-02-option2',
              },
              {
                optionText: 'this is choice a1-02-option3',
                optionScore: 2,
                optionId: 'a1-02-option3',
              },
              {
                optionText: 'this is choice a1-02-option4',
                optionScore: 3,
                optionId: 'a1-02-option4',
              },
              {
                optionText: 'this is choice a1-02-option5',
                optionScore: 4,
                optionId: 'a1-02-option5',
              },
            ],
          },
          {
            questionText: 'this is question a3',
            questionId: 'a1-03',
            ansState: false,
            singleScore: 0,
            answerOptions: [
              {
                optionText: 'this is choice a1-03-option1',
                optionScore: 0,
                optionId: 'a1-03-option1',
              },
              {
                optionText: 'this is choice a1-03-option2',
                optionScore: 1,
                optionId: 'a1-03-option2',
              },
              {
                optionText: 'this is choice a1-03-option3',
                optionScore: 2,
                optionId: 'a1-03-option3',
              },
              {
                optionText: 'this is choice a1-03-option4',
                optionScore: 3,
                optionId: 'a1-03-option4',
              },
              {
                optionText: 'this is choice a1-03-option5',
                optionScore: 4,
                optionId: 'a1-03-option5',
              },
            ],
          },
        ],
      },
      {
        category: 'type b',
        categoryId: 'b1',
        categoryScore: 25,
        questionList: [
          {
            questionText: 'this is question b1',
            questionId: 'b1-01',
            ansState: false,
            singleScore: 0,
            answerOptions: [
              {
                optionText: 'this is choice b1-01-option1',
                optionScore: 0,
                optionId: 'b1-01-option1',
              },
              {
                optionText: 'this is choice b1-01-option2',
                optionScore: 1,
                optionId: 'b1-01-option2',
              },
              {
                optionText: 'this is choice b1-01-option3',
                optionScore: 2,
                optionId: 'b1-01-option3',
              },
              {
                optionText: 'this is choice b1-01-option4',
                optionScore: 3,
                optionId: 'b1-01-option4',
              },
              {
                optionText: 'this is choice b1-01-option5',
                optionScore: 4,
                optionId: 'b1-01-option5',
              },
            ],
          },
          {
            questionText: 'this is question b2',
            questionId: 'b1-02',
            ansState: false,
            singleScore: 0,
            answerOptions: [
              {
                optionText: 'this is choice b1-02-option1',
                optionScore: 0,
                optionId: 'b1-02-option1',
              },
              {
                optionText: 'this is choice b1-02-option2',
                optionScore: 1,
                optionId: 'b1-02-option2',
              },
              {
                optionText: 'this is choice b1-02-option3',
                optionScore: 2,
                optionId: 'b1-02-option3',
              },
              {
                optionText: 'this is choice b1-02-option4',
                optionScore: 3,
                optionId: 'b1-02-option4',
              },
              {
                optionText: 'this is choice b1-02-option5',
                optionScore: 4,
                optionId: 'b1-02-option5',
              },
            ],
          },
          {
            questionText: 'this is question b3',
            questionId: 'b1-03',
            ansState: false,
            singleScore: 0,
            answerOptions: [
              {
                optionText: 'this is choice b1-03-option1',
                optionScore: 0,
                optionId: 'b1-03-option1',
              },
              {
                optionText: 'this is choice b1-03-option2',
                optionScore: 1,
                optionId: 'b1-03-option2',
              },
              {
                optionText: 'this is choice b1-03-option3',
                optionScore: 2,
                optionId: 'b1-03-option3',
              },
              {
                optionText: 'this is choice b1-03-option4',
                optionScore: 3,
                optionId: 'b1-03-option4',
              },
              {
                optionText: 'this is choice b1-03-option5',
                optionScore: 4,
                optionId: 'b1-03-option5',
              },
            ],
          },
        ],
      },
    ]
)

</script>

<template>
  <div id="app">
    <product-list :list="list" :person="person" :qa-list="qaList"></product-list>
  </div>
</template>
