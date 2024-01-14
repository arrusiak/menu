<template>
  <div class="container faq-container">
    <h2 class="container-title">FAQ</h2>
    <v-row justify="center" class="mt-6 m-2">
      <div class="col-12">
        <v-expansion-panels v-for="item in items" class="faq-list">
          <v-expansion-panel>
            <v-expansion-panel-header class="font-weight-bold">{{item.text}}</v-expansion-panel-header>
            <v-expansion-panel-content>
              {{item.description}}
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
      </div>
    </v-row>
  </div>
</template>

<script>
export default {
  name: 'FAQ',
  data() {
    return {
      items: [
        {
          text: 'How is the nutrition program designed?',
          description: '180 g / 200 ccal',
        },
        {
          text: 'Can I be sure of the quality and safety of the products?',
          description: ' • Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.',
        },
        {
          text: 'Can I be sure of the quality and safety of the products?',
          description: '180 g / 200 ccal',
        },
        {
          text: 'Can I be sure of the quality and safety of the products?',
          description: '180 g / 200 ccal',
        },
      ],
    }
  }
};
</script>
