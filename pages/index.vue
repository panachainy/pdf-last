<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6" style="background-color: green">
      <p>this 1</p>
      <img :src="require('~/assets/imgs/example.png')" />
      <p>this 2</p>

      <!-- <pdf
        src="https://cdn.rawgit.com/mozilla/pdf.js/c6e8ca86/test/pdfs/freeculture.pdf"
        @num-pages="pageCount = $event"
        @page-loaded="currentPage = $event"
      ></pdf> -->

      <iframe
        src="https://cdn.rawgit.com/mozilla/pdf.js/c6e8ca86/test/pdfs/freeculture.pdf#toolbar=0"
        width="100%"
        height="500px"
        frameborder="0"
      >
      </iframe>

      <p>this 3</p>

      <a href="/assets/pdfs/example.pdf" download="">Download</a>
    </v-col>
  </v-row>
</template>

<script>
import pdf from 'vue-pdf'

// var loadingTask = pdf.createLoadingTask(
//   'https://cdn.rawgit.com/mozilla/pdf.js/c6e8ca86/test/pdfs/freeculture.pdf'
// )

export default {
  name: 'IndexPage',
  components: {
    pdf,
  },
  // data() {
  //   return {
  //     show: true,
  //     src: 'https://cdn.rawgit.com/mozilla/pdf.js/c6e8ca86/test/pdfs/freeculture.pdf',
  //     loadedRatio: 0,
  //     page: 1,
  //     numPages: 0,
  //     rotate: 0,
  //   }
  // },

  // data() {
  //   return {
  //     currentPage: 0,
  //     pageCount: 0,
  //     numPages: undefined,
  //     src: loadingTask,
  //     // dd: require('@/assets/pdfs/example.pdf'),
  //     // @src="require('@/assets/pdfs/example.pdf')"
  //     //         :src="require('assets/pdfs/example.pdf')"
  //     // src="~/assets/pdfs/example.pdf"
  //     // :src="require('~/assets/pdfs/example.pdf')"
  //   }
  // },
  // mounted() {
  //   this.src.promise.then((pdf) => {
  //     this.numPages = pdf.numPages
  //   })
  // },
}
</script>
