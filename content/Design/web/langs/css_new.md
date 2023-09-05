# Draft: CSS Features That Aren't Widely Supported But Should Be

<style>
    @supports (initial-letter:2) or (-webkit-initial-letter:2) {
  p.fltest:first-letter {
    -webkit-initial-letter: 2;
    initial-letter: 2;
    margin: 0 .5rem 0 0;
    text-shadow: .3em .3em 2px black;
    font-family: 'Roboto Mono', monospace;
  }
}
.balance-text{
  text-wrap: balance;
}
</style>



* element() - https://www.stefanjudis.com/a-firefox-only-minimap/

  * It's highly unlikely chrome will ever support these

* [has()](https://caniuse.com/css-has) - Coming Soon™ to a browser near you. (It's waiting on Firefox, but is already there behind a feature flag)

* [@scope](https://caniuse.com/css-cascade-scope) - Still quite new, but looks promising.

* [text-wrap: balance](https://caniuse.com/css-text-wrap-balance) - seems to be polyfill-able, https://github.com/adobe/balance-text but should get widespread support directly soon-ish.

  This page will also check if the polyfill works. It seems to just fine. I don't want to condone using it yet though, as the polyfill shouldn't be necessary for long.
  
<script src="https://cdnjs.cloudflare.com/ajax/libs/balance-text/3.3.1/balancetext.min.js"></script>
<script>balanceText();</script>

  <h1 class="heading balance-text">This heading will not have a weirdly long top line</h1>

Compared to,

# This heading will not have a weirdly long top line

* [@when / @else](https://caniuse.com/css-when-else) - nobody supports this at all at time of writing.

* [lch() & lab()](https://caniuse.com/css-lch-lab) - totally supported on desktop, but GOD FUCKING DAMN SAMSUNG WHY THE FUCK ARE YOU SHIPPING YOUR OWN PIECE OF SHIT BROWSER. I'm debating putting something on this site just making a modal saying use a different browser for your own good. If I can 

  Both of the following should be a similar (but not the same) light blue.

  <p style="color:lch(72% 47 246);">LCH TEST</p>

  <p style="color:lab(70% -25 -100);">LAB TEST</p>

  * Related, [color-mix](https://developer.chrome.com/blog/whats-new-css-ui-2023/#color-mix) already has decent support

* [Initial Letter](https://caniuse.com/?search=initial%20letter) - It's weird that this isn't already broadly supported, given almost everything already has it behind a flag.

The 'W' in the following lyrics should be large and have a backing shadow.

> <p class="fltest">We're no strangers to love</br>You know the rules and so do I<br>A full commitment's what I'm thinking of</br>You wouldn't get this from any other guy</br><p class="fltest">I just wanna tell you how I'm feeling</br>Gotta make you understand</br>Never gonna give you up</br>Never gonna let you down</p>

* [@scroll-timeline](https://caniuse.com/?search=%40scroll-timeline) - It's still behind flags, but does appear to be at least actively worked on.

* [masonry](https://caniuse.com/?search=mason) flows, grids, and columns are all supported in Firefox but no other browsers at the time of writing. This one [looks quite nice](https://codepen.io/jensimmons/full/vYNeRZw) if it works in your browser.

* Firefox for the longest time, and still probably now, has had gradients without dithering, so they have obvious banding. 

  <div style="height:100px;background-image: linear-gradient(to right, #000, #333);">a</div>

  You can work around this by using an image, but that's annoying.