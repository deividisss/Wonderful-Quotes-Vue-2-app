<template>
  <div>
    <div class="container border border-top-0 rounded">
      <app-header>
        <slot>{{ name }}</slot>
      </app-header>
      <div class="container">
        <ul class="nav nav-tabs">
          <li class="nav-item">
            <a class="nav-link active" href="#">Active</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Link</a>
          </li>
        </ul>
      </div>
      <br />
      <app-progress-bar :quotesCount="quotesCount" />

      <app-new-quote
        :quotes="quotes"
        :quotesCount="quotesCount"
        @update-count="quotesCount = $event"
      ></app-new-quote>
      <div class="container">
        <app-info-bar>
          <slot> <b>Info:</b> Cick on Quote to delete it </slot>
        </app-info-bar>
        <hr />
        <h2>Quotes List</h2>
        <app-quote-list :quotes="quotes"></app-quote-list>
      </div>

      <br />
    </div>
    <br />
    <div class="kontiks pt-3"><app-Wall></app-Wall></div>
  </div>
</template>

<script>
// App.vue ToDo List
// Form visi chekai
// Quotes Displayed on a real wall picture
// Panaikint Hover New Quote Componente +
// Margin auto Quote when used in NewQuote component +
// gggggggggggggggggggggggg bug (jei kartoji simboli ir nededi tarpu neveik break point )
// Real time appearing Quote +
// Su Enter submit form +
// Alert box kuris saka istrink quotes, jei nori pridėt paildomai virsijus limita
// Quote wall Limit 10
// Tweet quote
// Fetch Quote
// Quote Design pagal temą
// Local storage
// Add Border animation
// Active component switch
// Progress Bars spalvas pagal Quote pasirinkta dizaina
// Auto kalba

import appHeader from "./components/layout/Header.vue";
import appQuote from "./components/Quote.vue";
import appQuoteList from "./components/QuoteList.vue";
import appInfoBar from "./components/InfoBar.vue";
import appNewQuote from "./components/NewQuote.vue";
import appProgressBar from "./components/ProgressBar.vue";
import appWall from "./components/Wall.vue";

export default {
  components: {
    appQuote,
    appHeader,
    appQuoteList,
    appInfoBar,
    appNewQuote,
    appProgressBar,
    appWall,
  },
  methods: {},
  computed: {
    quotesCount() {
      return this.quotes.length;
    },
  },
  data() {
    return {
      name: "Wonderfull Quotes",

      quotes: [
        {
          quote:
            "Life isn’t about getting and having, it’s about giving and being.",
          author: "Kevin Kruse",
        },
        {
          quote:
            "Whatever the mind of man can conceive and believe, it can achieve.",
          author: "Napoleon Hill",
        },
        {
          quote: "Strive not to be a success, but rather to be of value.",
          author: "Albert Einstein",
        },
        {
          quote:
            "Two roads diverged in a wood, and I—I took the one less traveled by, And that has made all the difference.",
          author: "Robert Frost",
        },
        {
          quote:
            "I attribute my success to this: I never gave or took any excuse.",
          author: "Florence Nightingale",
        },
        {
          quote: "You miss 100% of the shots you don’t take.",
          author: "Wayne Gretzky",
        },
        {
          quote:
            "I’ve missed more than 9000 shots in my career. I’ve lost almost 300 games. 26 times I’ve been trusted to take the game winning shot and missed. I’ve failed over and over and over again in my life. And that is why I succeed.",
          author: "Michael Jordan",
        },
        {
          quote:
            "The most difficult thing is the decision to act, the rest is merely tenacity.",
          author: "Amelia Earhart",
        },
        {
          quote: "Every strike brings me closer to the next home run.",
          author: "Babe Ruth",
        },
        {
          quote:
            "Definiteness of purpose is the starting point of all achievement.",
          author: "W. Clement Stone",
        },
      ],
    };
  },
};
</script>

<style>
.kontiks {
  min-height: 900px;
  background: #eef2f7;
}
</style>

