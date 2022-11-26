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
        id="scrollDive"
        :src="src"
        width="100%"
        height="500px"
        frameborder="0"
        @scroll="test"
      >
      </iframe>

      <p>this 3</p>

      <!-- <a href="/assets/pdfs/example.pdf" download="">Download</a> -->

      <p>this 4</p>

      <!-- <div
        contenteditable="true"
        id="scrollDive"
        class="scroll-div"
        @scroll="test"
      >
        x x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x
        x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x x
        x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x x
        x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x x
        x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x x
        x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x x
        x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x x
        x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x x
        x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x x
        x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x x
        x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x x
        x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x x
        x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x x
        x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x x
        x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x x
        x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x xx x x x x x
      </div> -->
    </v-col>
  </v-row>
</template>

<script>
import pdf from 'vue-pdf'

export default {
  name: 'IndexPage',
  components: {
    pdf,
  },
  data() {
    return {
      src:
        'https://cdn.rawgit.com/mozilla/pdf.js/c6e8ca86/test/pdfs/freeculture.pdf' +
        '#toolbar=0',
      // src: require('@/assets/pdfs/example.pdf') + '#toolbar=0',

      // src: 'https://www.pexels.com/search/tiger',
    }
  },
  methods: {
    // onScroll({ target: { scrollTop, clientHeight, scrollHeight } }) {
    //   print('=========', scrollTop, clientHeight, scrollHeight)
    //   if (scrollTop + clientHeight >= scrollHeight) {
    //     // this.loadMorePosts()
    //     print('=========')
    //   }
    // },
    test(e) {
      // console.log('scroll', this.$refs.scrollHeight)
      // console.log('scroll', this.$refs.scrollHeight)

      console.log('1', e)
      console.log('this.value = window.scrollY;', (this.value = window.scrollY))
      // scrollDive
    },
  },

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
<style scoped>
.scroll-div {
  margin-top: 20px;
  border: 1px solid;
  height: 60px;
  overflow: auto;
}
</style>
