<template>
  <div class="container">
    <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
    <div class="row">
      <div class="col-md-12 text-center p-3">
        <div class="alert alert-info">
          Info:Click on Quote to Delete it!
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";
import Header from "./components/Header.vue";

export default {
  data() {
    return {
      quotes: ["This is a Quote"],
      maxQuotes: 10,
    };
  },
  methods: {
    newQuote(quote) {
      if(this.quotes.length>=this.maxQuotes){
        return alert("Please Delete Quotes First!");
      }
      this.quotes.push(quote);
    },
    deleteQuote(index){
      this.quotes.splice(index, 1);
    }
  },
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote,
    appHeader:Header
  },
};
</script>

<style></style>
