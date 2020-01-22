---
layout: post
title: test ipynb
---

<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />

<title>Analysis CenterNet data processing</title>

<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>



<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.7.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.7.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.7.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff2?v=4.7.0') format('woff2'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.7.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.7.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.7.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.fa-pull-left {
  float: left;
}
.fa-pull-right {
  float: right;
}
.fa.fa-pull-left {
  margin-right: .3em;
}
.fa.fa-pull-right {
  margin-left: .3em;
}
/* Deprecated as of 4.4.0 */
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
.fa-pulse {
  -webkit-animation: fa-spin 1s infinite steps(8);
  animation: fa-spin 1s infinite steps(8);
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=1)";
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2)";
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=3)";
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1)";
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1)";
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook-f:before,
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-feed:before,
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before,
.fa-gratipay:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper-pp:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-resistance:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-y-combinator-square:before,
.fa-yc-square:before,
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
.fa-buysellads:before {
  content: "\f20d";
}
.fa-connectdevelop:before {
  content: "\f20e";
}
.fa-dashcube:before {
  content: "\f210";
}
.fa-forumbee:before {
  content: "\f211";
}
.fa-leanpub:before {
  content: "\f212";
}
.fa-sellsy:before {
  content: "\f213";
}
.fa-shirtsinbulk:before {
  content: "\f214";
}
.fa-simplybuilt:before {
  content: "\f215";
}
.fa-skyatlas:before {
  content: "\f216";
}
.fa-cart-plus:before {
  content: "\f217";
}
.fa-cart-arrow-down:before {
  content: "\f218";
}
.fa-diamond:before {
  content: "\f219";
}
.fa-ship:before {
  content: "\f21a";
}
.fa-user-secret:before {
  content: "\f21b";
}
.fa-motorcycle:before {
  content: "\f21c";
}
.fa-street-view:before {
  content: "\f21d";
}
.fa-heartbeat:before {
  content: "\f21e";
}
.fa-venus:before {
  content: "\f221";
}
.fa-mars:before {
  content: "\f222";
}
.fa-mercury:before {
  content: "\f223";
}
.fa-intersex:before,
.fa-transgender:before {
  content: "\f224";
}
.fa-transgender-alt:before {
  content: "\f225";
}
.fa-venus-double:before {
  content: "\f226";
}
.fa-mars-double:before {
  content: "\f227";
}
.fa-venus-mars:before {
  content: "\f228";
}
.fa-mars-stroke:before {
  content: "\f229";
}
.fa-mars-stroke-v:before {
  content: "\f22a";
}
.fa-mars-stroke-h:before {
  content: "\f22b";
}
.fa-neuter:before {
  content: "\f22c";
}
.fa-genderless:before {
  content: "\f22d";
}
.fa-facebook-official:before {
  content: "\f230";
}
.fa-pinterest-p:before {
  content: "\f231";
}
.fa-whatsapp:before {
  content: "\f232";
}
.fa-server:before {
  content: "\f233";
}
.fa-user-plus:before {
  content: "\f234";
}
.fa-user-times:before {
  content: "\f235";
}
.fa-hotel:before,
.fa-bed:before {
  content: "\f236";
}
.fa-viacoin:before {
  content: "\f237";
}
.fa-train:before {
  content: "\f238";
}
.fa-subway:before {
  content: "\f239";
}
.fa-medium:before {
  content: "\f23a";
}
.fa-yc:before,
.fa-y-combinator:before {
  content: "\f23b";
}
.fa-optin-monster:before {
  content: "\f23c";
}
.fa-opencart:before {
  content: "\f23d";
}
.fa-expeditedssl:before {
  content: "\f23e";
}
.fa-battery-4:before,
.fa-battery:before,
.fa-battery-full:before {
  content: "\f240";
}
.fa-battery-3:before,
.fa-battery-three-quarters:before {
  content: "\f241";
}
.fa-battery-2:before,
.fa-battery-half:before {
  content: "\f242";
}
.fa-battery-1:before,
.fa-battery-quarter:before {
  content: "\f243";
}
.fa-battery-0:before,
.fa-battery-empty:before {
  content: "\f244";
}
.fa-mouse-pointer:before {
  content: "\f245";
}
.fa-i-cursor:before {
  content: "\f246";
}
.fa-object-group:before {
  content: "\f247";
}
.fa-object-ungroup:before {
  content: "\f248";
}
.fa-sticky-note:before {
  content: "\f249";
}
.fa-sticky-note-o:before {
  content: "\f24a";
}
.fa-cc-jcb:before {
  content: "\f24b";
}
.fa-cc-diners-club:before {
  content: "\f24c";
}
.fa-clone:before {
  content: "\f24d";
}
.fa-balance-scale:before {
  content: "\f24e";
}
.fa-hourglass-o:before {
  content: "\f250";
}
.fa-hourglass-1:before,
.fa-hourglass-start:before {
  content: "\f251";
}
.fa-hourglass-2:before,
.fa-hourglass-half:before {
  content: "\f252";
}
.fa-hourglass-3:before,
.fa-hourglass-end:before {
  content: "\f253";
}
.fa-hourglass:before {
  content: "\f254";
}
.fa-hand-grab-o:before,
.fa-hand-rock-o:before {
  content: "\f255";
}
.fa-hand-stop-o:before,
.fa-hand-paper-o:before {
  content: "\f256";
}
.fa-hand-scissors-o:before {
  content: "\f257";
}
.fa-hand-lizard-o:before {
  content: "\f258";
}
.fa-hand-spock-o:before {
  content: "\f259";
}
.fa-hand-pointer-o:before {
  content: "\f25a";
}
.fa-hand-peace-o:before {
  content: "\f25b";
}
.fa-trademark:before {
  content: "\f25c";
}
.fa-registered:before {
  content: "\f25d";
}
.fa-creative-commons:before {
  content: "\f25e";
}
.fa-gg:before {
  content: "\f260";
}
.fa-gg-circle:before {
  content: "\f261";
}
.fa-tripadvisor:before {
  content: "\f262";
}
.fa-odnoklassniki:before {
  content: "\f263";
}
.fa-odnoklassniki-square:before {
  content: "\f264";
}
.fa-get-pocket:before {
  content: "\f265";
}
.fa-wikipedia-w:before {
  content: "\f266";
}
.fa-safari:before {
  content: "\f267";
}
.fa-chrome:before {
  content: "\f268";
}
.fa-firefox:before {
  content: "\f269";
}
.fa-opera:before {
  content: "\f26a";
}
.fa-internet-explorer:before {
  content: "\f26b";
}
.fa-tv:before,
.fa-television:before {
  content: "\f26c";
}
.fa-contao:before {
  content: "\f26d";
}
.fa-500px:before {
  content: "\f26e";
}
.fa-amazon:before {
  content: "\f270";
}
.fa-calendar-plus-o:before {
  content: "\f271";
}
.fa-calendar-minus-o:before {
  content: "\f272";
}
.fa-calendar-times-o:before {
  content: "\f273";
}
.fa-calendar-check-o:before {
  content: "\f274";
}
.fa-industry:before {
  content: "\f275";
}
.fa-map-pin:before {
  content: "\f276";
}
.fa-map-signs:before {
  content: "\f277";
}
.fa-map-o:before {
  content: "\f278";
}
.fa-map:before {
  content: "\f279";
}
.fa-commenting:before {
  content: "\f27a";
}
.fa-commenting-o:before {
  content: "\f27b";
}
.fa-houzz:before {
  content: "\f27c";
}
.fa-vimeo:before {
  content: "\f27d";
}
.fa-black-tie:before {
  content: "\f27e";
}
.fa-fonticons:before {
  content: "\f280";
}
.fa-reddit-alien:before {
  content: "\f281";
}
.fa-edge:before {
  content: "\f282";
}
.fa-credit-card-alt:before {
  content: "\f283";
}
.fa-codiepie:before {
  content: "\f284";
}
.fa-modx:before {
  content: "\f285";
}
.fa-fort-awesome:before {
  content: "\f286";
}
.fa-usb:before {
  content: "\f287";
}
.fa-product-hunt:before {
  content: "\f288";
}
.fa-mixcloud:before {
  content: "\f289";
}
.fa-scribd:before {
  content: "\f28a";
}
.fa-pause-circle:before {
  content: "\f28b";
}
.fa-pause-circle-o:before {
  content: "\f28c";
}
.fa-stop-circle:before {
  content: "\f28d";
}
.fa-stop-circle-o:before {
  content: "\f28e";
}
.fa-shopping-bag:before {
  content: "\f290";
}
.fa-shopping-basket:before {
  content: "\f291";
}
.fa-hashtag:before {
  content: "\f292";
}
.fa-bluetooth:before {
  content: "\f293";
}
.fa-bluetooth-b:before {
  content: "\f294";
}
.fa-percent:before {
  content: "\f295";
}
.fa-gitlab:before {
  content: "\f296";
}
.fa-wpbeginner:before {
  content: "\f297";
}
.fa-wpforms:before {
  content: "\f298";
}
.fa-envira:before {
  content: "\f299";
}
.fa-universal-access:before {
  content: "\f29a";
}
.fa-wheelchair-alt:before {
  content: "\f29b";
}
.fa-question-circle-o:before {
  content: "\f29c";
}
.fa-blind:before {
  content: "\f29d";
}
.fa-audio-description:before {
  content: "\f29e";
}
.fa-volume-control-phone:before {
  content: "\f2a0";
}
.fa-braille:before {
  content: "\f2a1";
}
.fa-assistive-listening-systems:before {
  content: "\f2a2";
}
.fa-asl-interpreting:before,
.fa-american-sign-language-interpreting:before {
  content: "\f2a3";
}
.fa-deafness:before,
.fa-hard-of-hearing:before,
.fa-deaf:before {
  content: "\f2a4";
}
.fa-glide:before {
  content: "\f2a5";
}
.fa-glide-g:before {
  content: "\f2a6";
}
.fa-signing:before,
.fa-sign-language:before {
  content: "\f2a7";
}
.fa-low-vision:before {
  content: "\f2a8";
}
.fa-viadeo:before {
  content: "\f2a9";
}
.fa-viadeo-square:before {
  content: "\f2aa";
}
.fa-snapchat:before {
  content: "\f2ab";
}
.fa-snapchat-ghost:before {
  content: "\f2ac";
}
.fa-snapchat-square:before {
  content: "\f2ad";
}
.fa-pied-piper:before {
  content: "\f2ae";
}
.fa-first-order:before {
  content: "\f2b0";
}
.fa-yoast:before {
  content: "\f2b1";
}
.fa-themeisle:before {
  content: "\f2b2";
}
.fa-google-plus-circle:before,
.fa-google-plus-official:before {
  content: "\f2b3";
}
.fa-fa:before,
.fa-font-awesome:before {
  content: "\f2b4";
}
.fa-handshake-o:before {
  content: "\f2b5";
}
.fa-envelope-open:before {
  content: "\f2b6";
}
.fa-envelope-open-o:before {
  content: "\f2b7";
}
.fa-linode:before {
  content: "\f2b8";
}
.fa-address-book:before {
  content: "\f2b9";
}
.fa-address-book-o:before {
  content: "\f2ba";
}
.fa-vcard:before,
.fa-address-card:before {
  content: "\f2bb";
}
.fa-vcard-o:before,
.fa-address-card-o:before {
  content: "\f2bc";
}
.fa-user-circle:before {
  content: "\f2bd";
}
.fa-user-circle-o:before {
  content: "\f2be";
}
.fa-user-o:before {
  content: "\f2c0";
}
.fa-id-badge:before {
  content: "\f2c1";
}
.fa-drivers-license:before,
.fa-id-card:before {
  content: "\f2c2";
}
.fa-drivers-license-o:before,
.fa-id-card-o:before {
  content: "\f2c3";
}
.fa-quora:before {
  content: "\f2c4";
}
.fa-free-code-camp:before {
  content: "\f2c5";
}
.fa-telegram:before {
  content: "\f2c6";
}
.fa-thermometer-4:before,
.fa-thermometer:before,
.fa-thermometer-full:before {
  content: "\f2c7";
}
.fa-thermometer-3:before,
.fa-thermometer-three-quarters:before {
  content: "\f2c8";
}
.fa-thermometer-2:before,
.fa-thermometer-half:before {
  content: "\f2c9";
}
.fa-thermometer-1:before,
.fa-thermometer-quarter:before {
  content: "\f2ca";
}
.fa-thermometer-0:before,
.fa-thermometer-empty:before {
  content: "\f2cb";
}
.fa-shower:before {
  content: "\f2cc";
}
.fa-bathtub:before,
.fa-s15:before,
.fa-bath:before {
  content: "\f2cd";
}
.fa-podcast:before {
  content: "\f2ce";
}
.fa-window-maximize:before {
  content: "\f2d0";
}
.fa-window-minimize:before {
  content: "\f2d1";
}
.fa-window-restore:before {
  content: "\f2d2";
}
.fa-times-rectangle:before,
.fa-window-close:before {
  content: "\f2d3";
}
.fa-times-rectangle-o:before,
.fa-window-close-o:before {
  content: "\f2d4";
}
.fa-bandcamp:before {
  content: "\f2d5";
}
.fa-grav:before {
  content: "\f2d6";
}
.fa-etsy:before {
  content: "\f2d7";
}
.fa-imdb:before {
  content: "\f2d8";
}
.fa-ravelry:before {
  content: "\f2d9";
}
.fa-eercast:before {
  content: "\f2da";
}
.fa-microchip:before {
  content: "\f2db";
}
.fa-snowflake-o:before {
  content: "\f2dc";
}
.fa-superpowers:before {
  content: "\f2dd";
}
.fa-wpexplorer:before {
  content: "\f2de";
}
.fa-meetup:before {
  content: "\f2e0";
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
div.traceback-wrapper pre.traceback {
  max-height: 600px;
  overflow: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 5px;
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
[dir="rtl"] #ipython_notebook {
  margin-right: 10px;
  margin-left: 0;
}
[dir="rtl"] #ipython_notebook.pull-left {
  float: right !important;
  float: right;
}
.flex-spacer {
  flex: 1;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#kernel_logo_widget {
  margin: 0 10px;
}
span#login_widget {
  float: right;
}
[dir="rtl"] span#login_widget {
  float: left;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
.modal-header {
  cursor: move;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
[dir="rtl"] .center-nav form.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] .center-nav .navbar-text {
  float: right;
}
[dir="rtl"] .navbar-inner {
  text-align: right;
}
[dir="rtl"] div.text-left {
  text-align: right;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  overflow: hidden;
  cursor: pointer;
  opacity: 0;
  z-index: 2;
}
.alternate_upload .btn-xs > input.fileinput {
  margin: -1px -5px;
}
.alternate_upload .btn-upload {
  position: relative;
  height: 22px;
}
::-webkit-file-upload-button {
  cursor: pointer;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
ul#tabs {
  margin-bottom: 4px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
[dir="rtl"] ul#tabs.nav-tabs > li {
  float: right;
}
[dir="rtl"] ul#tabs.nav.nav-tabs {
  padding-right: 0;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons .pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .list_toolbar .col-sm-4,
[dir="rtl"] .list_toolbar .col-sm-8 {
  float: right;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: text-bottom;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
[dir="rtl"] .list_item > div input {
  margin-right: 0;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_modified {
  margin-right: 7px;
  margin-left: 7px;
}
[dir="rtl"] .item_modified.pull-right {
  float: left !important;
  float: left;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
[dir="rtl"] .item_buttons.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .item_buttons .kernel-name {
  margin-left: 7px;
  float: right;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
.sort_button {
  display: inline-block;
  padding-left: 7px;
}
[dir="rtl"] .sort_button.pull-right {
  float: left !important;
  float: left;
}
#tree-selector {
  padding-right: 0px;
}
#button-select-all {
  min-width: 50px;
}
[dir="rtl"] #button-select-all.btn {
  float: right ;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
  margin-top: 2px;
  height: 16px;
}
[dir="rtl"] #select-all.pull-left {
  float: right !important;
  float: right;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.fa-pull-left {
  margin-right: .3em;
}
.folder_icon:before.fa-pull-right {
  margin-left: .3em;
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.fa-pull-left {
  margin-right: .3em;
}
.file_icon:before.fa-pull-right {
  margin-left: .3em;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
#new-menu .dropdown-header {
  font-size: 10px;
  border-bottom: 1px solid #e5e5e5;
  padding: 0 0 3px;
  margin: -3px 20px 0;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.move-button {
  display: none;
}
.download-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
.CodeMirror-dialog {
  background-color: #fff;
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI escape sequences */
/* The color values are a mix of
   http://www.xcolors.net/dl/baskerville-ivorylight and
   http://www.xcolors.net/dl/euphrasia */
.ansi-black-fg {
  color: #3E424D;
}
.ansi-black-bg {
  background-color: #3E424D;
}
.ansi-black-intense-fg {
  color: #282C36;
}
.ansi-black-intense-bg {
  background-color: #282C36;
}
.ansi-red-fg {
  color: #E75C58;
}
.ansi-red-bg {
  background-color: #E75C58;
}
.ansi-red-intense-fg {
  color: #B22B31;
}
.ansi-red-intense-bg {
  background-color: #B22B31;
}
.ansi-green-fg {
  color: #00A250;
}
.ansi-green-bg {
  background-color: #00A250;
}
.ansi-green-intense-fg {
  color: #007427;
}
.ansi-green-intense-bg {
  background-color: #007427;
}
.ansi-yellow-fg {
  color: #DDB62B;
}
.ansi-yellow-bg {
  background-color: #DDB62B;
}
.ansi-yellow-intense-fg {
  color: #B27D12;
}
.ansi-yellow-intense-bg {
  background-color: #B27D12;
}
.ansi-blue-fg {
  color: #208FFB;
}
.ansi-blue-bg {
  background-color: #208FFB;
}
.ansi-blue-intense-fg {
  color: #0065CA;
}
.ansi-blue-intense-bg {
  background-color: #0065CA;
}
.ansi-magenta-fg {
  color: #D160C4;
}
.ansi-magenta-bg {
  background-color: #D160C4;
}
.ansi-magenta-intense-fg {
  color: #A03196;
}
.ansi-magenta-intense-bg {
  background-color: #A03196;
}
.ansi-cyan-fg {
  color: #60C6C8;
}
.ansi-cyan-bg {
  background-color: #60C6C8;
}
.ansi-cyan-intense-fg {
  color: #258F8F;
}
.ansi-cyan-intense-bg {
  background-color: #258F8F;
}
.ansi-white-fg {
  color: #C5C1B4;
}
.ansi-white-bg {
  background-color: #C5C1B4;
}
.ansi-white-intense-fg {
  color: #A1A6B2;
}
.ansi-white-intense-bg {
  background-color: #A1A6B2;
}
.ansi-default-inverse-fg {
  color: #FFFFFF;
}
.ansi-default-inverse-bg {
  background-color: #000000;
}
.ansi-bold {
  font-weight: bold;
}
.ansi-underline {
  text-decoration: underline;
}
/* The following styles are deprecated an will be removed in a future version */
.ansibold {
  font-weight: bold;
}
.ansi-inverse {
  outline: 0.5px dotted;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  position: relative;
  overflow: visible;
}
div.cell:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: transparent;
}
div.cell.jupyter-soft-selected {
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected,
div.cell.selected.jupyter-soft-selected {
  border-color: #ababab;
}
div.cell.selected:before,
div.cell.selected.jupyter-soft-selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #42A5F5;
}
@media print {
  div.cell.selected,
  div.cell.selected.jupyter-soft-selected {
    border-color: transparent;
  }
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
}
.edit_mode div.cell.selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #66BB6A;
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  /* Note that this should set vertical padding only, since CodeMirror assumes
       that horizontal padding will be set on CodeMirror pre */
  padding: 0.4em 0;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. This sets horizontal padding only,
    use .CodeMirror-lines for vertical */
  padding: 0 0.4em;
  border: 0;
  border-radius: 0;
}
.CodeMirror-cursor {
  border-left: 1.4px solid black;
}
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .CodeMirror-cursor {
    border-left: 2px solid black;
  }
}
@media screen and (min-width: 4320px) {
  .CodeMirror-cursor {
    border-left: 4px solid black;
  }
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
div.output_area .mglyph > img {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 1px 0 1px 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul:not(.list-inline),
.rendered_html ol:not(.list-inline) {
  padding-left: 2em;
}
.rendered_html ul {
  list-style: disc;
}
.rendered_html ul ul {
  list-style: square;
  margin-top: 0;
}
.rendered_html ul ul ul {
  list-style: circle;
}
.rendered_html ol {
  list-style: decimal;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin-top: 0;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
  padding: 0px;
  background-color: #fff;
}
.rendered_html code {
  background-color: #eff0f1;
}
.rendered_html p code {
  padding: 1px 5px;
}
.rendered_html pre code {
  background-color: #fff;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  color: #000;
  font-size: 100%;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: none;
  border-collapse: collapse;
  border-spacing: 0;
  color: black;
  font-size: 12px;
  table-layout: fixed;
}
.rendered_html thead {
  border-bottom: 1px solid black;
  vertical-align: bottom;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  text-align: right;
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html tbody tr:nth-child(odd) {
  background: #f5f5f5;
}
.rendered_html tbody tr:hover {
  background: rgba(66, 165, 245, 0.2);
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
.rendered_html .alert {
  margin-bottom: initial;
}
.rendered_html * + .alert {
  margin-top: 1em;
}
[dir="rtl"] .rendered_html p {
  text-align: right;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.rendered .rendered_html tr,
.text_cell.rendered .rendered_html th,
.text_cell.rendered .rendered_html td {
  max-width: none;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.text_cell .dropzone .input_area {
  border: 2px dashed #bababa;
  margin: -1px;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
.jupyter-keybindings {
  padding: 1px;
  line-height: 24px;
  border-bottom: 1px solid gray;
}
.jupyter-keybindings input {
  margin: 0;
  padding: 0;
  border: none;
}
.jupyter-keybindings i {
  padding: 6px;
}
.well code {
  background-color: #ffffff;
  border-color: #ababab;
  border-width: 1px;
  border-style: solid;
  padding: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.tags_button_container {
  width: 100%;
  display: flex;
}
.tag-container {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  overflow: hidden;
  position: relative;
}
.tag-container > * {
  margin: 0 4px;
}
.remove-tag-btn {
  margin-left: 4px;
}
.tags-input {
  display: flex;
}
.cell-tag:last-child:after {
  content: "";
  position: absolute;
  right: 0;
  width: 40px;
  height: 100%;
  /* Fade to background color of cell toolbar */
  background: linear-gradient(to right, rgba(0, 0, 0, 0), #EEE);
}
.tags-input > * {
  margin-left: 4px;
}
.cell-tag,
.tags-input input,
.tags-input button {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  box-shadow: none;
  width: inherit;
  font-size: inherit;
  height: 22px;
  line-height: 22px;
  padding: 0px 4px;
  display: inline-block;
}
.cell-tag:focus,
.tags-input input:focus,
.tags-input button:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.cell-tag::-moz-placeholder,
.tags-input input::-moz-placeholder,
.tags-input button::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.cell-tag:-ms-input-placeholder,
.tags-input input:-ms-input-placeholder,
.tags-input button:-ms-input-placeholder {
  color: #999;
}
.cell-tag::-webkit-input-placeholder,
.tags-input input::-webkit-input-placeholder,
.tags-input button::-webkit-input-placeholder {
  color: #999;
}
.cell-tag::-ms-expand,
.tags-input input::-ms-expand,
.tags-input button::-ms-expand {
  border: 0;
  background-color: transparent;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
.cell-tag[readonly],
.tags-input input[readonly],
.tags-input button[readonly],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  background-color: #eeeeee;
  opacity: 1;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  cursor: not-allowed;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button {
  height: auto;
}
select.cell-tag,
select.tags-input input,
select.tags-input button {
  height: 30px;
  line-height: 30px;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button,
select[multiple].cell-tag,
select[multiple].tags-input input,
select[multiple].tags-input button {
  height: auto;
}
.cell-tag,
.tags-input button {
  padding: 0px 4px;
}
.cell-tag {
  background-color: #fff;
  white-space: nowrap;
}
.tags-input input[type=text]:focus {
  outline: none;
  box-shadow: none;
  border-color: #ccc;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
[dir="rtl"] #kernel_logo_widget {
  float: left !important;
  float: left;
}
.modal .modal-body .move-path {
  display: flex;
  flex-direction: row;
  justify-content: space;
  align-items: center;
}
.modal .modal-body .move-path .server-root {
  padding-right: 20px;
}
.modal .modal-body .move-path .path-input {
  flex: 1;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
[dir="rtl"] #menubar .navbar-toggle {
  float: right;
}
[dir="rtl"] #menubar .navbar-collapse {
  clear: right;
}
[dir="rtl"] #menubar .navbar-nav {
  float: right;
}
[dir="rtl"] #menubar .nav {
  padding-right: 0px;
}
[dir="rtl"] #menubar .navbar-nav > li {
  float: right;
}
[dir="rtl"] #menubar .navbar-right {
  float: left !important;
}
[dir="rtl"] ul.dropdown-menu {
  text-align: right;
  left: auto;
}
[dir="rtl"] ul#new-menu.dropdown-menu {
  right: auto;
  left: 0;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
[dir="rtl"] i.menu-icon.pull-right {
  float: left !important;
  float: left;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
[dir="rtl"] ul#help_menu li a {
  padding-left: 2.2em;
}
[dir="rtl"] ul#help_menu li a i {
  margin-right: 0;
  margin-left: -1.2em;
}
[dir="rtl"] ul#help_menu li a i.pull-right {
  float: left !important;
  float: left;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
[dir="rtl"] .dropdown-submenu > .dropdown-menu {
  right: 100%;
  margin-right: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.fa-pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.fa-pull-right {
  margin-left: .3em;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
[dir="rtl"] .dropdown-submenu > a:after {
  float: left;
  content: "\f0d9";
  margin-right: 0;
  margin-left: -10px;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
[dir="rtl"] #notification_area {
  float: left !important;
  float: left;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] .indicator_area {
  float: left !important;
  float: left;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
[dir="rtl"] #kernel_indicator {
  float: left !important;
  float: left;
  border-left: 0;
  border-right: 1px solid;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] #modal_indicator {
  float: left !important;
  float: left;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  height: 30px;
  margin-top: 4px;
  display: flex;
  justify-content: flex-start;
  align-items: baseline;
  width: 50%;
  flex: 1;
}
span.save_widget span.filename {
  height: 100%;
  line-height: 1em;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
[dir="rtl"] span.save_widget.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] span.save_widget span.filename {
  margin-left: 0;
  margin-right: 16px;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
  white-space: nowrap;
  padding: 0 5px;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
    padding: 0 0 0 5px;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
.toolbar-btn-label {
  margin-left: 6px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
[dir="rtl"] .btn-group > .btn,
.btn-group-vertical > .btn {
  float: right;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
[dir="rtl"] ul.typeahead-list i {
  margin-left: 0;
  margin-right: -10px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
ul.typeahead-list  > li > a.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .typeahead-list {
  text-align: right;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  min-width: 20px;
  color: transparent;
}
[dir="rtl"] .no-shortcut.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .command-shortcut.pull-right {
  float: left !important;
  float: left;
}
.command-shortcut:before {
  content: "(command mode)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
[dir="rtl"] .edit-shortcut.pull-right {
  float: left !important;
  float: left;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
[dir="ltr"] #find-and-replace .input-group-btn + .form-control {
  border-left: none;
}
[dir="rtl"] #find-and-replace .input-group-btn + .form-control {
  border-right: none;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/latest.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">sys</span>
<span class="n">sys</span><span class="o">.</span><span class="n">path</span><span class="o">.</span><span class="n">insert</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="s2">&quot;/media/allen/mass/CenterNet/src/lib&quot;</span><span class="p">)</span>
<span class="kn">import</span> <span class="nn">torch.utils.data</span> <span class="k">as</span> <span class="nn">data</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">torch</span>
<span class="kn">import</span> <span class="nn">json</span>
<span class="kn">import</span> <span class="nn">cv2</span>
<span class="kn">import</span> <span class="nn">os</span>
<span class="kn">from</span> <span class="nn">utils.image</span> <span class="kn">import</span> <span class="n">flip</span><span class="p">,</span> <span class="n">color_aug</span>
<span class="kn">from</span> <span class="nn">utils.image</span> <span class="kn">import</span> <span class="n">get_affine_transform</span><span class="p">,</span> <span class="n">affine_transform</span>
<span class="kn">from</span> <span class="nn">utils.image</span> <span class="kn">import</span> <span class="n">gaussian_radius</span><span class="p">,</span> <span class="n">draw_umich_gaussian</span><span class="p">,</span> <span class="n">draw_msra_gaussian</span>
<span class="kn">from</span> <span class="nn">utils.image</span> <span class="kn">import</span> <span class="n">draw_dense_reg</span>
<span class="kn">import</span> <span class="nn">math</span>
<span class="k">def</span> <span class="nf">_get_border</span><span class="p">(</span><span class="n">border</span><span class="p">,</span> <span class="n">size</span><span class="p">):</span>
    <span class="n">i</span> <span class="o">=</span> <span class="mi">1</span>
    <span class="k">while</span> <span class="n">size</span> <span class="o">-</span> <span class="n">border</span> <span class="o">//</span> <span class="n">i</span> <span class="o">&lt;=</span> <span class="n">border</span> <span class="o">//</span> <span class="n">i</span><span class="p">:</span>
        <span class="n">i</span> <span class="o">*=</span> <span class="mi">2</span>
    <span class="k">return</span> <span class="n">border</span> <span class="o">//</span> <span class="n">i</span>

<span class="kn">from</span> <span class="nn">PIL</span> <span class="kn">import</span> <span class="n">Image</span> 
<span class="k">def</span> <span class="nf">to_pil</span><span class="p">(</span><span class="n">cv_img</span><span class="p">):</span>
    <span class="n">img</span> <span class="o">=</span> <span class="n">cv2</span><span class="o">.</span><span class="n">cvtColor</span><span class="p">(</span><span class="n">cv_img</span><span class="p">,</span> <span class="n">cv2</span><span class="o">.</span><span class="n">COLOR_BGR2RGB</span><span class="p">)</span>
    <span class="k">return</span> <span class="n">Image</span><span class="o">.</span><span class="n">fromarray</span><span class="p">(</span><span class="n">img</span><span class="p">)</span>

<span class="k">def</span> <span class="nf">gaussian2D</span><span class="p">(</span><span class="n">shape</span><span class="p">,</span> <span class="n">sigma</span><span class="o">=</span><span class="mi">1</span><span class="p">):</span>
    <span class="n">m</span><span class="p">,</span> <span class="n">n</span> <span class="o">=</span> <span class="p">[(</span><span class="n">ss</span> <span class="o">-</span> <span class="mf">1.</span><span class="p">)</span> <span class="o">/</span> <span class="mf">2.</span> <span class="k">for</span> <span class="n">ss</span> <span class="ow">in</span> <span class="n">shape</span><span class="p">]</span>
    <span class="n">y</span><span class="p">,</span> <span class="n">x</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">ogrid</span><span class="p">[</span><span class="o">-</span><span class="n">m</span><span class="p">:</span><span class="n">m</span><span class="o">+</span><span class="mi">1</span><span class="p">,</span><span class="o">-</span><span class="n">n</span><span class="p">:</span><span class="n">n</span><span class="o">+</span><span class="mi">1</span><span class="p">]</span>

    <span class="n">h</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">exp</span><span class="p">(</span><span class="o">-</span><span class="p">(</span><span class="n">x</span> <span class="o">*</span> <span class="n">x</span> <span class="o">+</span> <span class="n">y</span> <span class="o">*</span> <span class="n">y</span><span class="p">)</span> <span class="o">/</span> <span class="p">(</span><span class="mi">2</span> <span class="o">*</span> <span class="n">sigma</span> <span class="o">*</span> <span class="n">sigma</span><span class="p">))</span>
    <span class="n">h</span><span class="p">[</span><span class="n">h</span> <span class="o">&lt;</span> <span class="n">np</span><span class="o">.</span><span class="n">finfo</span><span class="p">(</span><span class="n">h</span><span class="o">.</span><span class="n">dtype</span><span class="p">)</span><span class="o">.</span><span class="n">eps</span> <span class="o">*</span> <span class="n">h</span><span class="o">.</span><span class="n">max</span><span class="p">()]</span> <span class="o">=</span> <span class="mi">0</span>
    <span class="k">return</span> <span class="n">h</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">img_path</span> <span class="o">=</span> <span class="s2">&quot;/media/allen/mass/recording/0/CAM1-2019-11-12_10-55-26_58.jpg&quot;</span>
<span class="n">img</span> <span class="o">=</span> <span class="n">cv2</span><span class="o">.</span><span class="n">imread</span><span class="p">(</span><span class="n">img_path</span><span class="p">)</span>
<span class="n">img_h</span><span class="p">,</span> <span class="n">img_w</span> <span class="o">=</span> <span class="n">img</span><span class="o">.</span><span class="n">shape</span><span class="p">[:</span><span class="mi">2</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[128]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">s</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">choice</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="mf">0.6</span><span class="p">,</span> <span class="mf">1.4</span><span class="p">,</span> <span class="mf">0.1</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="n">s</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>0.7999999999999999
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[129]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">in_h</span><span class="p">,</span> <span class="n">in_w</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">img_h</span> <span class="o">*</span> <span class="n">s</span><span class="p">),</span> <span class="nb">int</span><span class="p">(</span><span class="n">img_w</span> <span class="o">*</span> <span class="n">s</span><span class="p">)</span>
<span class="n">scale_img</span> <span class="o">=</span> <span class="n">cv2</span><span class="o">.</span><span class="n">resize</span><span class="p">(</span><span class="n">img</span><span class="p">,</span> <span class="p">(</span><span class="n">in_w</span><span class="p">,</span> <span class="n">in_h</span><span class="p">))</span>
<span class="n">out_h</span><span class="p">,</span> <span class="n">out_w</span> <span class="o">=</span> <span class="n">scale_img</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">//</span> <span class="mi">4</span><span class="p">,</span> <span class="n">scale_img</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">//</span> <span class="mi">4</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[130]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">hm</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="n">num_classes</span><span class="p">,</span> <span class="n">out_h</span><span class="p">,</span> <span class="n">out_w</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
<span class="n">wh</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="mi">128</span><span class="p">,</span> <span class="mi">2</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
<span class="n">reg</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="mi">128</span><span class="p">,</span> <span class="mi">2</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
<span class="n">ind</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="mi">128</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">int64</span><span class="p">)</span>
<span class="n">reg_mask</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="mi">128</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">uint8</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[131]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">draw_gaussian</span> <span class="o">=</span> <span class="n">draw_umich_gaussian</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[132]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">bbox</span> <span class="o">=</span> <span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([</span><span class="mi">1688</span><span class="p">,</span> <span class="mi">387</span><span class="p">,</span> <span class="mi">1821</span><span class="p">,</span> <span class="mi">811</span><span class="p">])</span> <span class="o">*</span> <span class="n">s</span><span class="p">)</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="nb">int</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[133]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">bbox</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[133]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([1350,  309, 1456,  648])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[134]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">to_pil</span><span class="p">(</span><span class="n">scale_img</span><span class="p">[</span><span class="n">bbox</span><span class="p">[</span><span class="mi">1</span><span class="p">]:</span><span class="n">bbox</span><span class="p">[</span><span class="mi">3</span><span class="p">],</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">0</span><span class="p">]:</span><span class="n">bbox</span><span class="p">[</span><span class="mi">2</span><span class="p">],</span> <span class="p">:])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[134]:</div>




<div class="output_png output_subarea output_execute_result">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[135]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">ob_h</span><span class="p">,</span> <span class="n">ob_w</span> <span class="o">=</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span> <span class="o">-</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">1</span><span class="p">],</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span> <span class="o">-</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
<span class="n">radius</span> <span class="o">=</span> <span class="n">gaussian_radius</span><span class="p">((</span><span class="n">ob_h</span><span class="p">,</span> <span class="n">ob_w</span><span class="p">))</span>
<span class="n">radius</span> <span class="o">=</span> <span class="nb">max</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="nb">int</span><span class="p">(</span><span class="n">radius</span><span class="p">))</span>
<span class="n">radius</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[135]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>45</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[136]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">k</span> <span class="o">=</span> <span class="mi">1</span>
<span class="n">bbox</span> <span class="o">=</span> <span class="n">bbox</span> <span class="o">//</span> <span class="mi">4</span>
<span class="n">ct</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([(</span><span class="n">bbox</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">+</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">2</span><span class="p">])</span> <span class="o">/</span> <span class="mi">2</span><span class="p">,</span> <span class="p">(</span><span class="n">bbox</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">+</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">3</span><span class="p">])</span> <span class="o">/</span> <span class="mi">2</span><span class="p">],</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
<span class="n">ct_int</span> <span class="o">=</span> <span class="n">ct</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">int32</span><span class="p">)</span>
<span class="n">hm</span><span class="p">[</span><span class="mi">10</span><span class="p">]</span> <span class="o">=</span> <span class="n">draw_gaussian</span><span class="p">(</span><span class="n">hm</span><span class="p">[</span><span class="mi">10</span><span class="p">],</span> <span class="n">ct_int</span><span class="p">,</span> <span class="n">radius</span><span class="p">)</span>
<span class="n">wh</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="mf">1.</span> <span class="o">*</span> <span class="n">ob_w</span><span class="p">,</span> <span class="mf">1.</span> <span class="o">*</span> <span class="n">ob_h</span>
<span class="n">ind</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="n">ct_int</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">*</span> <span class="n">out_w</span> <span class="o">+</span> <span class="n">ct_int</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
<span class="n">reg</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="n">ct</span> <span class="o">-</span> <span class="n">ct_int</span>
<span class="n">reg_mask</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="mi">1</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[137]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">hm</span><span class="p">[</span><span class="mi">10</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[137]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([[0., 0., 0., ..., 0., 0., 0.],
       [0., 0., 0., ..., 0., 0., 0.],
       [0., 0., 0., ..., 0., 0., 0.],
       ...,
       [0., 0., 0., ..., 0., 0., 0.],
       [0., 0., 0., ..., 0., 0., 0.],
       [0., 0., 0., ..., 0., 0., 0.]], dtype=float32)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[138]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">diameter</span> <span class="o">=</span> <span class="mi">2</span> <span class="o">*</span> <span class="n">radius</span> <span class="o">+</span> <span class="mi">1</span>
<span class="n">gaussian</span> <span class="o">=</span> <span class="n">gaussian2D</span><span class="p">((</span><span class="n">diameter</span><span class="p">,</span> <span class="n">diameter</span><span class="p">),</span> <span class="n">sigma</span><span class="o">=</span><span class="n">diameter</span> <span class="o">/</span> <span class="mi">6</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[139]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">heatmap</span> <span class="o">=</span> <span class="n">hm</span><span class="p">[</span><span class="mi">10</span><span class="p">]</span>
<span class="n">x</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">ct_int</span><span class="p">[</span><span class="mi">0</span><span class="p">]),</span> <span class="nb">int</span><span class="p">(</span><span class="n">ct_int</span><span class="p">[</span><span class="mi">1</span><span class="p">])</span>

<span class="n">height</span><span class="p">,</span> <span class="n">width</span> <span class="o">=</span> <span class="n">heatmap</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">:</span><span class="mi">2</span><span class="p">]</span>

<span class="n">left</span><span class="p">,</span> <span class="n">right</span> <span class="o">=</span> <span class="nb">min</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">radius</span><span class="p">),</span> <span class="nb">min</span><span class="p">(</span><span class="n">width</span> <span class="o">-</span> <span class="n">x</span><span class="p">,</span> <span class="n">radius</span> <span class="o">+</span> <span class="mi">1</span><span class="p">)</span>
<span class="n">top</span><span class="p">,</span> <span class="n">bottom</span> <span class="o">=</span> <span class="nb">min</span><span class="p">(</span><span class="n">y</span><span class="p">,</span> <span class="n">radius</span><span class="p">),</span> <span class="nb">min</span><span class="p">(</span><span class="n">height</span> <span class="o">-</span> <span class="n">y</span><span class="p">,</span> <span class="n">radius</span> <span class="o">+</span> <span class="mi">1</span><span class="p">)</span>

<span class="n">masked_heatmap</span>  <span class="o">=</span> <span class="n">heatmap</span><span class="p">[(</span><span class="n">y</span> <span class="o">-</span> <span class="n">top</span><span class="p">):(</span><span class="n">y</span> <span class="o">+</span> <span class="n">bottom</span><span class="p">),</span> <span class="p">(</span><span class="n">x</span> <span class="o">-</span> <span class="n">left</span><span class="p">):(</span><span class="n">x</span> <span class="o">+</span> <span class="n">right</span><span class="p">)]</span>
<span class="n">masked_gaussian</span> <span class="o">=</span> <span class="n">gaussian</span><span class="p">[(</span><span class="n">radius</span> <span class="o">-</span> <span class="n">top</span><span class="p">):(</span><span class="n">radius</span> <span class="o">+</span> <span class="n">bottom</span><span class="p">),</span> <span class="p">(</span><span class="n">radius</span> <span class="o">-</span> <span class="n">left</span><span class="p">):(</span><span class="n">radius</span> <span class="o">+</span> <span class="n">right</span><span class="p">)]</span>
<span class="k">if</span> <span class="nb">min</span><span class="p">(</span><span class="n">masked_gaussian</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span> <span class="o">&gt;</span> <span class="mi">0</span> <span class="ow">and</span> <span class="nb">min</span><span class="p">(</span><span class="n">masked_heatmap</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span> <span class="o">&gt;</span> <span class="mi">0</span><span class="p">:</span> <span class="c1"># TODO debug</span>
    <span class="n">np</span><span class="o">.</span><span class="n">maximum</span><span class="p">(</span><span class="n">masked_heatmap</span><span class="p">,</span> <span class="n">masked_gaussian</span> <span class="o">*</span> <span class="n">k</span><span class="p">,</span> <span class="n">out</span><span class="o">=</span><span class="n">masked_heatmap</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[159]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">masked_heatmap</span><span class="o">.</span><span class="n">min</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[159]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>0.00015023879</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[118]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">gaussian</span><span class="p">[(</span><span class="n">radius</span> <span class="o">-</span> <span class="n">top</span><span class="p">):(</span><span class="n">radius</span> <span class="o">+</span> <span class="n">bottom</span><span class="p">),</span> <span class="p">(</span><span class="n">radius</span> <span class="o">-</span> <span class="n">left</span><span class="p">):(</span><span class="n">radius</span> <span class="o">+</span> <span class="n">right</span><span class="p">)]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[118]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([], shape=(0, 0), dtype=float64)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[100]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">gt_det</span><span class="o">.</span><span class="n">append</span><span class="p">([</span><span class="n">ct</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">-</span> <span class="n">w</span> <span class="o">/</span> <span class="mi">2</span><span class="p">,</span> <span class="n">ct</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">-</span> <span class="n">h</span> <span class="o">/</span> <span class="mi">2</span><span class="p">,</span> 
                       <span class="n">ct</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">+</span> <span class="n">w</span> <span class="o">/</span> <span class="mi">2</span><span class="p">,</span> <span class="n">ct</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">+</span> <span class="n">h</span> <span class="o">/</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="n">cls_id</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[100]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([0.5, 0.5])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">if</span> <span class="n">ob_h</span> <span class="o">&gt;</span> <span class="mi">0</span> <span class="ow">and</span> <span class="n">w</span> <span class="o">&gt;</span> <span class="mi">0</span><span class="p">:</span>
    <span class="n">radius</span> <span class="o">=</span> <span class="n">gaussian_radius</span><span class="p">(</span><span class="n">ob_h</span><span class="p">,</span> <span class="n">ob_w</span><span class="p">))</span>
    <span class="n">radius</span> <span class="o">=</span> <span class="nb">max</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="nb">int</span><span class="p">(</span><span class="n">radius</span><span class="p">))</span>
    <span class="n">radius</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">opt</span><span class="o">.</span><span class="n">hm_gauss</span> <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">opt</span><span class="o">.</span><span class="n">mse_loss</span> <span class="k">else</span> <span class="n">radius</span>
    <span class="n">ct</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span>
      <span class="p">[(</span><span class="n">bbox</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">+</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">2</span><span class="p">])</span> <span class="o">/</span> <span class="mi">2</span><span class="p">,</span> <span class="p">(</span><span class="n">bbox</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">+</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">3</span><span class="p">])</span> <span class="o">/</span> <span class="mi">2</span><span class="p">],</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
    <span class="n">ct_int</span> <span class="o">=</span> <span class="n">ct</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">int32</span><span class="p">)</span>
    <span class="n">draw_gaussian</span><span class="p">(</span><span class="n">hm</span><span class="p">[</span><span class="n">cls_id</span><span class="p">],</span> <span class="n">ct_int</span><span class="p">,</span> <span class="n">radius</span><span class="p">)</span>
    <span class="n">wh</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="mf">1.</span> <span class="o">*</span> <span class="n">w</span><span class="p">,</span> <span class="mf">1.</span> <span class="o">*</span> <span class="n">h</span>
    <span class="n">ind</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="n">ct_int</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">*</span> <span class="n">output_w</span> <span class="o">+</span> <span class="n">ct_int</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
    <span class="n">reg</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="n">ct</span> <span class="o">-</span> <span class="n">ct_int</span>
    <span class="n">reg_mask</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="mi">1</span>
    <span class="n">cat_spec_wh</span><span class="p">[</span><span class="n">k</span><span class="p">,</span> <span class="n">cls_id</span> <span class="o">*</span> <span class="mi">2</span><span class="p">:</span> <span class="n">cls_id</span> <span class="o">*</span> <span class="mi">2</span> <span class="o">+</span> <span class="mi">2</span><span class="p">]</span> <span class="o">=</span> <span class="n">wh</span><span class="p">[</span><span class="n">k</span><span class="p">]</span>
    <span class="n">cat_spec_mask</span><span class="p">[</span><span class="n">k</span><span class="p">,</span> <span class="n">cls_id</span> <span class="o">*</span> <span class="mi">2</span><span class="p">:</span> <span class="n">cls_id</span> <span class="o">*</span> <span class="mi">2</span> <span class="o">+</span> <span class="mi">2</span><span class="p">]</span> <span class="o">=</span> <span class="mi">1</span>
    <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">opt</span><span class="o">.</span><span class="n">dense_wh</span><span class="p">:</span>
      <span class="n">draw_dense_reg</span><span class="p">(</span><span class="n">dense_wh</span><span class="p">,</span> <span class="n">hm</span><span class="o">.</span><span class="n">max</span><span class="p">(</span><span class="n">axis</span><span class="o">=</span><span class="mi">0</span><span class="p">),</span> <span class="n">ct_int</span><span class="p">,</span> <span class="n">wh</span><span class="p">[</span><span class="n">k</span><span class="p">],</span> <span class="n">radius</span><span class="p">)</span>
    <span class="n">gt_det</span><span class="o">.</span><span class="n">append</span><span class="p">([</span><span class="n">ct</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">-</span> <span class="n">w</span> <span class="o">/</span> <span class="mi">2</span><span class="p">,</span> <span class="n">ct</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">-</span> <span class="n">h</span> <span class="o">/</span> <span class="mi">2</span><span class="p">,</span> 
                   <span class="n">ct</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">+</span> <span class="n">w</span> <span class="o">/</span> <span class="mi">2</span><span class="p">,</span> <span class="n">ct</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">+</span> <span class="n">h</span> <span class="o">/</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="n">cls_id</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">c</span><span class="o">/</span><span class="mi">4</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[10]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([301.32648, 134.34888], dtype=float32)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[104]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">sys</span>
<span class="n">sys</span><span class="o">.</span><span class="n">path</span><span class="o">.</span><span class="n">insert</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="s2">&quot;/media/allen/mass/CenterNet/src/lib&quot;</span><span class="p">)</span>
<span class="kn">import</span> <span class="nn">torch.utils.data</span> <span class="k">as</span> <span class="nn">data</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">torch</span>
<span class="kn">import</span> <span class="nn">json</span>
<span class="kn">import</span> <span class="nn">cv2</span>
<span class="kn">import</span> <span class="nn">os</span>
<span class="kn">from</span> <span class="nn">utils.image</span> <span class="kn">import</span> <span class="n">flip</span><span class="p">,</span> <span class="n">color_aug</span>
<span class="kn">from</span> <span class="nn">utils.image</span> <span class="kn">import</span> <span class="n">get_affine_transform</span><span class="p">,</span> <span class="n">affine_transform</span>
<span class="kn">from</span> <span class="nn">utils.image</span> <span class="kn">import</span> <span class="n">gaussian_radius</span><span class="p">,</span> <span class="n">draw_umich_gaussian</span><span class="p">,</span> <span class="n">draw_msra_gaussian</span>
<span class="kn">from</span> <span class="nn">utils.image</span> <span class="kn">import</span> <span class="n">draw_dense_reg</span>
<span class="kn">import</span> <span class="nn">math</span>


<span class="c1">#     img_id = self.images[index]</span>
<span class="c1">#     file_name = self.coco.loadImgs(ids=[img_id])[0][&#39;file_name&#39;]</span>
<span class="n">img_path</span> <span class="o">=</span> <span class="s2">&quot;/media/allen/mass/recording/0/CAM1-2019-11-12_10-55-26_58.jpg&quot;</span>
<span class="c1">#     ann_ids = self.coco.getAnnIds(imgIds=[img_id])</span>
<span class="c1">#     anns = self.coco.loadAnns(ids=ann_ids)</span>
<span class="n">num_objs</span> <span class="o">=</span> <span class="mi">1</span>

<span class="n">img</span> <span class="o">=</span> <span class="n">cv2</span><span class="o">.</span><span class="n">imread</span><span class="p">(</span><span class="n">img_path</span><span class="p">)</span>
<span class="n">height</span><span class="p">,</span> <span class="n">width</span> <span class="o">=</span> <span class="n">img</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="n">img</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> 
<span class="n">long_side</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">max</span><span class="p">([</span><span class="n">height</span><span class="p">,</span> <span class="n">width</span><span class="p">])</span>
<span class="n">canvas</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">([</span><span class="n">long_side</span><span class="p">,</span> <span class="n">long_side</span><span class="p">,</span> <span class="mi">3</span><span class="p">])</span>
<span class="n">h_offset</span><span class="p">,</span> <span class="n">w_offset</span> <span class="o">=</span> <span class="nb">int</span><span class="p">((</span><span class="n">long_side</span><span class="o">-</span><span class="n">height</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span> <span class="nb">int</span><span class="p">((</span><span class="n">long_side</span><span class="o">-</span><span class="n">width</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span>
<span class="n">canvas</span><span class="p">[</span><span class="n">h_offset</span><span class="p">:(</span><span class="n">height</span><span class="o">+</span><span class="n">h_offset</span><span class="p">),</span> <span class="n">w_offset</span><span class="p">:(</span><span class="n">width</span><span class="o">+</span><span class="n">w_offset</span><span class="p">),</span> <span class="p">:]</span> <span class="o">=</span> <span class="n">img</span>
<span class="n">img</span> <span class="o">=</span> <span class="n">canvas</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">uint8</span><span class="p">)</span>   
<span class="n">scale</span> <span class="o">=</span> <span class="mi">512</span> <span class="o">/</span> <span class="n">long_side</span>
<span class="n">img</span> <span class="o">=</span> <span class="n">cv2</span><span class="o">.</span><span class="n">resize</span><span class="p">(</span><span class="n">img</span><span class="p">,</span> <span class="p">(</span><span class="mi">512</span><span class="p">,</span> <span class="mi">512</span><span class="p">))</span>
<span class="n">height</span><span class="p">,</span> <span class="n">width</span> <span class="o">=</span> <span class="n">img</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="n">img</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> 
<span class="n">c</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([</span><span class="n">img</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">/</span> <span class="mf">2.</span><span class="p">,</span> <span class="n">img</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">/</span> <span class="mf">2.</span><span class="p">],</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>

<span class="n">input_h</span> <span class="o">=</span> <span class="p">(</span><span class="n">height</span> <span class="o">|</span> <span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="mi">1</span>
<span class="n">input_w</span> <span class="o">=</span> <span class="p">(</span><span class="n">width</span> <span class="o">|</span> <span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="mi">1</span>
<span class="n">s</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([</span><span class="n">input_w</span><span class="p">,</span> <span class="n">input_h</span><span class="p">],</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>        


<span class="n">sf</span> <span class="o">=</span> <span class="mf">0.4</span>
<span class="n">cf</span> <span class="o">=</span> <span class="mf">0.1</span>
<span class="n">c</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">=</span> <span class="n">c</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">+</span> <span class="n">s</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">clip</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">randn</span><span class="p">()</span><span class="o">*</span><span class="n">cf</span><span class="p">,</span> <span class="o">-</span><span class="mi">2</span><span class="o">*</span><span class="n">cf</span><span class="p">,</span> <span class="mi">2</span><span class="o">*</span><span class="n">cf</span><span class="p">)</span>
<span class="n">c</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">=</span> <span class="n">c</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">+</span> <span class="n">s</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">clip</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">randn</span><span class="p">()</span><span class="o">*</span><span class="n">cf</span><span class="p">,</span> <span class="o">-</span><span class="mi">2</span><span class="o">*</span><span class="n">cf</span><span class="p">,</span> <span class="mi">2</span><span class="o">*</span><span class="n">cf</span><span class="p">)</span>
<span class="n">s</span> <span class="o">=</span> <span class="n">s</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">clip</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">randn</span><span class="p">()</span><span class="o">*</span><span class="n">sf</span> <span class="o">+</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">1</span> <span class="o">-</span> <span class="n">sf</span><span class="p">,</span> <span class="mi">1</span> <span class="o">+</span> <span class="n">sf</span><span class="p">)</span>


<span class="n">trans_input</span> <span class="o">=</span> <span class="n">get_affine_transform</span><span class="p">(</span><span class="n">c</span><span class="p">,</span> <span class="n">s</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="p">[</span><span class="n">input_w</span><span class="p">,</span> <span class="n">input_h</span><span class="p">])</span>

<span class="n">inp</span> <span class="o">=</span> <span class="n">cv2</span><span class="o">.</span><span class="n">warpAffine</span><span class="p">(</span><span class="n">img</span><span class="p">,</span> <span class="n">trans_input</span><span class="p">,</span> 
                     <span class="p">(</span><span class="n">input_w</span><span class="p">,</span> <span class="n">input_h</span><span class="p">),</span>
                     <span class="n">flags</span><span class="o">=</span><span class="n">cv2</span><span class="o">.</span><span class="n">INTER_LINEAR</span><span class="p">)</span>

<span class="n">output_h</span> <span class="o">=</span> <span class="n">input_h</span> <span class="o">//</span> <span class="mi">4</span>
<span class="n">output_w</span> <span class="o">=</span> <span class="n">input_w</span> <span class="o">//</span> <span class="mi">4</span>
<span class="n">num_classes</span> <span class="o">=</span> <span class="mi">5</span>
<span class="n">trans_output</span> <span class="o">=</span> <span class="n">get_affine_transform</span><span class="p">(</span><span class="n">c</span><span class="p">,</span> <span class="n">s</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="p">[</span><span class="n">output_w</span><span class="p">,</span> <span class="n">output_h</span><span class="p">])</span>

<span class="n">hm</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="n">num_classes</span><span class="p">,</span> <span class="n">output_h</span><span class="p">,</span> <span class="n">output_w</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
<span class="n">wh</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="mi">128</span><span class="p">,</span> <span class="mi">2</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
<span class="n">dense_wh</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="mi">2</span><span class="p">,</span> <span class="n">output_h</span><span class="p">,</span> <span class="n">output_w</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
<span class="n">reg</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="mi">128</span><span class="p">,</span> <span class="mi">2</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
<span class="n">ind</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="mi">128</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">int64</span><span class="p">)</span>
<span class="n">reg_mask</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="mi">128</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">uint8</span><span class="p">)</span>

<span class="n">draw_gaussian</span> <span class="o">=</span> <span class="n">draw_umich_gaussian</span>

<span class="n">gt_det</span> <span class="o">=</span> <span class="p">[]</span>
<span class="k">for</span> <span class="n">k</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">num_objs</span><span class="p">):</span>

    <span class="n">bbox</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([</span><span class="mi">1688</span><span class="p">,</span> <span class="mi">387</span><span class="p">,</span> <span class="mi">1821</span><span class="p">,</span> <span class="mi">811</span><span class="p">])</span>
    <span class="n">bbox</span><span class="p">[[</span><span class="mi">0</span><span class="p">,</span> <span class="mi">2</span><span class="p">]]</span> <span class="o">+=</span> <span class="n">w_offset</span>
    <span class="n">bbox</span><span class="p">[[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">3</span><span class="p">]]</span> <span class="o">+=</span> <span class="n">h_offset</span>
    <span class="n">bbox</span> <span class="o">=</span> <span class="p">(</span><span class="n">bbox</span> <span class="o">*</span> <span class="n">scale</span><span class="p">)</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="nb">int</span><span class="p">)</span>
    <span class="n">cls_id</span> <span class="o">=</span> <span class="mi">1</span>
<span class="c1">#             if flipped:</span>
<span class="c1">#                 bbox[[0, 2]] = width - bbox[[2, 0]] - 1</span>
    <span class="n">bbox</span><span class="p">[:</span><span class="mi">2</span><span class="p">]</span> <span class="o">=</span> <span class="n">affine_transform</span><span class="p">(</span><span class="n">bbox</span><span class="p">[:</span><span class="mi">2</span><span class="p">],</span> <span class="n">trans_output</span><span class="p">)</span>
    <span class="n">bbox</span><span class="p">[</span><span class="mi">2</span><span class="p">:]</span> <span class="o">=</span> <span class="n">affine_transform</span><span class="p">(</span><span class="n">bbox</span><span class="p">[</span><span class="mi">2</span><span class="p">:],</span> <span class="n">trans_output</span><span class="p">)</span>
    <span class="n">bbox</span><span class="p">[[</span><span class="mi">0</span><span class="p">,</span> <span class="mi">2</span><span class="p">]]</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">clip</span><span class="p">(</span><span class="n">bbox</span><span class="p">[[</span><span class="mi">0</span><span class="p">,</span> <span class="mi">2</span><span class="p">]],</span> <span class="mi">0</span><span class="p">,</span> <span class="n">output_w</span> <span class="o">-</span> <span class="mi">1</span><span class="p">)</span>
    <span class="n">bbox</span><span class="p">[[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">3</span><span class="p">]]</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">clip</span><span class="p">(</span><span class="n">bbox</span><span class="p">[[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">3</span><span class="p">]],</span> <span class="mi">0</span><span class="p">,</span> <span class="n">output_h</span> <span class="o">-</span> <span class="mi">1</span><span class="p">)</span>
    <span class="n">h</span><span class="p">,</span> <span class="n">w</span> <span class="o">=</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span> <span class="o">-</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">1</span><span class="p">],</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span> <span class="o">-</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
    <span class="k">if</span> <span class="n">h</span> <span class="o">&gt;</span> <span class="mi">0</span> <span class="ow">and</span> <span class="n">w</span> <span class="o">&gt;</span> <span class="mi">0</span><span class="p">:</span>
        <span class="n">radius</span> <span class="o">=</span> <span class="n">gaussian_radius</span><span class="p">((</span><span class="n">math</span><span class="o">.</span><span class="n">ceil</span><span class="p">(</span><span class="n">h</span><span class="p">),</span> <span class="n">math</span><span class="o">.</span><span class="n">ceil</span><span class="p">(</span><span class="n">w</span><span class="p">)))</span>
        <span class="n">radius</span> <span class="o">=</span> <span class="nb">max</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="nb">int</span><span class="p">(</span><span class="n">radius</span><span class="p">))</span>
        <span class="n">ct</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span>
          <span class="p">[(</span><span class="n">bbox</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">+</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">2</span><span class="p">])</span> <span class="o">/</span> <span class="mi">2</span><span class="p">,</span> <span class="p">(</span><span class="n">bbox</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">+</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">3</span><span class="p">])</span> <span class="o">/</span> <span class="mi">2</span><span class="p">],</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
        <span class="n">ct_int</span> <span class="o">=</span> <span class="n">ct</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">int32</span><span class="p">)</span>
        <span class="n">draw_gaussian</span><span class="p">(</span><span class="n">hm</span><span class="p">[</span><span class="n">cls_id</span><span class="p">],</span> <span class="n">ct_int</span><span class="p">,</span> <span class="n">radius</span><span class="p">)</span>
        <span class="n">wh</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="mf">1.</span> <span class="o">*</span> <span class="n">w</span><span class="p">,</span> <span class="mf">1.</span> <span class="o">*</span> <span class="n">h</span>
        <span class="n">ind</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="n">ct_int</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">*</span> <span class="n">output_w</span> <span class="o">+</span> <span class="n">ct_int</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
        <span class="n">reg</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="n">ct</span> <span class="o">-</span> <span class="n">ct_int</span>
        <span class="n">reg_mask</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="mi">1</span>
        
<span class="n">ret</span> <span class="o">=</span> <span class="p">{</span><span class="s1">&#39;input&#39;</span><span class="p">:</span> <span class="n">inp</span><span class="p">,</span> <span class="s1">&#39;hm&#39;</span><span class="p">:</span> <span class="n">hm</span><span class="p">,</span> <span class="s1">&#39;reg_mask&#39;</span><span class="p">:</span> <span class="n">reg_mask</span><span class="p">,</span> <span class="s1">&#39;ind&#39;</span><span class="p">:</span> <span class="n">ind</span><span class="p">,</span> <span class="s1">&#39;wh&#39;</span><span class="p">:</span> <span class="n">wh</span><span class="p">}</span>        
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">sys</span>
<span class="n">sys</span><span class="o">.</span><span class="n">path</span><span class="o">.</span><span class="n">insert</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="s1">&#39;/media/allen/mass/deep-learning-works/&#39;</span><span class="p">)</span>
<span class="kn">import</span> <span class="nn">pycocotools.coco</span> <span class="k">as</span> <span class="nn">coco</span>
<span class="kn">import</span> <span class="nn">os.path</span> <span class="k">as</span> <span class="nn">osp</span>
<span class="kn">from</span> <span class="nn">tools.logger</span> <span class="kn">import</span> <span class="n">setup_logger</span>
<span class="n">logger</span> <span class="o">=</span> <span class="n">setup_logger</span><span class="p">(</span><span class="s2">&quot;.&quot;</span><span class="p">)</span>
<span class="kn">from</span> <span class="nn">data</span> <span class="kn">import</span> <span class="n">data_manager</span>
<span class="kn">from</span> <span class="nn">data.build_data</span> <span class="kn">import</span> <span class="n">build_DFKP_dataset</span>
<span class="c1"># from data.sampler import IdBasedSampler</span>
<span class="c1"># from data.build_transform import build_transform</span>
<span class="c1"># from torch.utils import data</span>
<span class="kn">from</span> <span class="nn">config.config_manager</span> <span class="kn">import</span> <span class="n">_C</span> <span class="k">as</span> <span class="n">cfg</span>
<span class="n">cfg</span><span class="o">.</span><span class="n">merge_from_file</span><span class="p">(</span><span class="s1">&#39;../keypoint.yml&#39;</span><span class="p">)</span>
<span class="n">cfg</span><span class="o">.</span><span class="n">DATASET</span><span class="o">.</span><span class="n">TRAIN_PATH</span> <span class="o">=</span> <span class="s1">&#39;/media/allen/mass/DeepFashion&#39;</span>
<span class="n">cfg</span><span class="o">.</span><span class="n">TASK</span> <span class="o">=</span> <span class="s1">&#39;reid&#39;</span>
<span class="n">cfg</span><span class="o">.</span><span class="n">MODEL</span><span class="o">.</span><span class="n">NUM_CLASSES</span> <span class="o">=</span> <span class="mi">5297</span>
<span class="n">cfg</span><span class="o">.</span><span class="n">EVALUATE</span> <span class="o">=</span> <span class="s1">&#39;../caffe_models/OSNet_merge_cels_triplet_center_Adam_lr_0.003_warmup_10_0.01_plateau_10_flip_crop_erase_imagenet_0.7096.pth&#39;</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">model.managers.manager_reid_trick</span> <span class="kn">import</span> <span class="n">TrickManager</span>
<span class="n">manager</span> <span class="o">=</span> <span class="n">TrickManager</span><span class="p">(</span><span class="n">cfg</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>2019-11-21 09:13:18,300 logger INFO: Evaluating model from ../caffe_models/OSNet_merge_cels_triplet_center_Adam_lr_0.003_warmup_10_0.01_plateau_10_flip_crop_erase_imagenet_0.7096.pth
2019-11-21 09:13:18,947 logger INFO: opt_0 is skipped
2019-11-21 09:13:18,950 logger INFO: opt_1 is skipped
2019-11-21 09:13:18,980 logger INFO: model backbone.conv1.conv.weight                              ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,982 logger INFO: model backbone.conv1.bn.weight                                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,983 logger INFO: model backbone.conv1.bn.bias                                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,984 logger INFO: model backbone.conv1.bn.running_mean                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,985 logger INFO: model backbone.conv1.bn.running_var                           ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,987 logger INFO: model backbone.conv2.0.conv1.conv.weight                      ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,988 logger INFO: model backbone.conv2.0.conv1.bn.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,989 logger INFO: model backbone.conv2.0.conv1.bn.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,990 logger INFO: model backbone.conv2.0.conv1.bn.running_mean                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,991 logger INFO: model backbone.conv2.0.conv1.bn.running_var                   ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,992 logger INFO: model backbone.conv2.0.conv2a.conv1.weight                    ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,993 logger INFO: model backbone.conv2.0.conv2a.conv2.weight                    ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,994 logger INFO: model backbone.conv2.0.conv2a.bn.weight                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,995 logger INFO: model backbone.conv2.0.conv2a.bn.bias                         ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,996 logger INFO: model backbone.conv2.0.conv2a.bn.running_mean                 ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,997 logger INFO: model backbone.conv2.0.conv2a.bn.running_var                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,997 logger INFO: model backbone.conv2.0.conv2b.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,998 logger INFO: model backbone.conv2.0.conv2b.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:18,999 logger INFO: model backbone.conv2.0.conv2b.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,001 logger INFO: model backbone.conv2.0.conv2b.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,002 logger INFO: model backbone.conv2.0.conv2b.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,003 logger INFO: model backbone.conv2.0.conv2b.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,005 logger INFO: model backbone.conv2.0.conv2b.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,006 logger INFO: model backbone.conv2.0.conv2b.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,007 logger INFO: model backbone.conv2.0.conv2b.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,008 logger INFO: model backbone.conv2.0.conv2b.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,010 logger INFO: model backbone.conv2.0.conv2b.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,010 logger INFO: model backbone.conv2.0.conv2b.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,011 logger INFO: model backbone.conv2.0.conv2c.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,012 logger INFO: model backbone.conv2.0.conv2c.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,013 logger INFO: model backbone.conv2.0.conv2c.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,014 logger INFO: model backbone.conv2.0.conv2c.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,015 logger INFO: model backbone.conv2.0.conv2c.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,016 logger INFO: model backbone.conv2.0.conv2c.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,016 logger INFO: model backbone.conv2.0.conv2c.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,017 logger INFO: model backbone.conv2.0.conv2c.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,018 logger INFO: model backbone.conv2.0.conv2c.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,019 logger INFO: model backbone.conv2.0.conv2c.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,020 logger INFO: model backbone.conv2.0.conv2c.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,021 logger INFO: model backbone.conv2.0.conv2c.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,022 logger INFO: model backbone.conv2.0.conv2c.2.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,023 logger INFO: model backbone.conv2.0.conv2c.2.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,024 logger INFO: model backbone.conv2.0.conv2c.2.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,025 logger INFO: model backbone.conv2.0.conv2c.2.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,026 logger INFO: model backbone.conv2.0.conv2c.2.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,029 logger INFO: model backbone.conv2.0.conv2c.2.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,031 logger INFO: model backbone.conv2.0.conv2d.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,032 logger INFO: model backbone.conv2.0.conv2d.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,033 logger INFO: model backbone.conv2.0.conv2d.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,034 logger INFO: model backbone.conv2.0.conv2d.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,035 logger INFO: model backbone.conv2.0.conv2d.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,036 logger INFO: model backbone.conv2.0.conv2d.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,037 logger INFO: model backbone.conv2.0.conv2d.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,038 logger INFO: model backbone.conv2.0.conv2d.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,038 logger INFO: model backbone.conv2.0.conv2d.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,039 logger INFO: model backbone.conv2.0.conv2d.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,041 logger INFO: model backbone.conv2.0.conv2d.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,042 logger INFO: model backbone.conv2.0.conv2d.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,044 logger INFO: model backbone.conv2.0.conv2d.2.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,045 logger INFO: model backbone.conv2.0.conv2d.2.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,046 logger INFO: model backbone.conv2.0.conv2d.2.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,047 logger INFO: model backbone.conv2.0.conv2d.2.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,048 logger INFO: model backbone.conv2.0.conv2d.2.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,050 logger INFO: model backbone.conv2.0.conv2d.2.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,052 logger INFO: model backbone.conv2.0.conv2d.3.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,053 logger INFO: model backbone.conv2.0.conv2d.3.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,054 logger INFO: model backbone.conv2.0.conv2d.3.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,056 logger INFO: model backbone.conv2.0.conv2d.3.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,057 logger INFO: model backbone.conv2.0.conv2d.3.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,058 logger INFO: model backbone.conv2.0.conv2d.3.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,059 logger INFO: model backbone.conv2.0.gate.fc1.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,060 logger INFO: model backbone.conv2.0.gate.fc1.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,061 logger INFO: model backbone.conv2.0.gate.fc2.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,062 logger INFO: model backbone.conv2.0.gate.fc2.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,063 logger INFO: model backbone.conv2.0.conv3.conv.weight                      ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,064 logger INFO: model backbone.conv2.0.conv3.bn.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,065 logger INFO: model backbone.conv2.0.conv3.bn.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,066 logger INFO: model backbone.conv2.0.conv3.bn.running_mean                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,067 logger INFO: model backbone.conv2.0.conv3.bn.running_var                   ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,068 logger INFO: model backbone.conv2.0.downsample.conv.weight                 ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,068 logger INFO: model backbone.conv2.0.downsample.bn.weight                   ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,069 logger INFO: model backbone.conv2.0.downsample.bn.bias                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,070 logger INFO: model backbone.conv2.0.downsample.bn.running_mean             ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,071 logger INFO: model backbone.conv2.0.downsample.bn.running_var              ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,072 logger INFO: model backbone.conv2.1.conv1.conv.weight                      ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,073 logger INFO: model backbone.conv2.1.conv1.bn.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,074 logger INFO: model backbone.conv2.1.conv1.bn.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,075 logger INFO: model backbone.conv2.1.conv1.bn.running_mean                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,076 logger INFO: model backbone.conv2.1.conv1.bn.running_var                   ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,077 logger INFO: model backbone.conv2.1.conv2a.conv1.weight                    ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,078 logger INFO: model backbone.conv2.1.conv2a.conv2.weight                    ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,079 logger INFO: model backbone.conv2.1.conv2a.bn.weight                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,079 logger INFO: model backbone.conv2.1.conv2a.bn.bias                         ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,080 logger INFO: model backbone.conv2.1.conv2a.bn.running_mean                 ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,081 logger INFO: model backbone.conv2.1.conv2a.bn.running_var                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,082 logger INFO: model backbone.conv2.1.conv2b.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,083 logger INFO: model backbone.conv2.1.conv2b.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,084 logger INFO: model backbone.conv2.1.conv2b.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,085 logger INFO: model backbone.conv2.1.conv2b.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,086 logger INFO: model backbone.conv2.1.conv2b.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,087 logger INFO: model backbone.conv2.1.conv2b.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,087 logger INFO: model backbone.conv2.1.conv2b.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,088 logger INFO: model backbone.conv2.1.conv2b.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,089 logger INFO: model backbone.conv2.1.conv2b.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,090 logger INFO: model backbone.conv2.1.conv2b.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,092 logger INFO: model backbone.conv2.1.conv2b.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,094 logger INFO: model backbone.conv2.1.conv2b.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,095 logger INFO: model backbone.conv2.1.conv2c.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,096 logger INFO: model backbone.conv2.1.conv2c.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,099 logger INFO: model backbone.conv2.1.conv2c.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,101 logger INFO: model backbone.conv2.1.conv2c.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,102 logger INFO: model backbone.conv2.1.conv2c.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,102 logger INFO: model backbone.conv2.1.conv2c.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,103 logger INFO: model backbone.conv2.1.conv2c.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,104 logger INFO: model backbone.conv2.1.conv2c.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,105 logger INFO: model backbone.conv2.1.conv2c.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,105 logger INFO: model backbone.conv2.1.conv2c.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,106 logger INFO: model backbone.conv2.1.conv2c.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,107 logger INFO: model backbone.conv2.1.conv2c.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,109 logger INFO: model backbone.conv2.1.conv2c.2.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,110 logger INFO: model backbone.conv2.1.conv2c.2.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,111 logger INFO: model backbone.conv2.1.conv2c.2.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,112 logger INFO: model backbone.conv2.1.conv2c.2.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,113 logger INFO: model backbone.conv2.1.conv2c.2.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,114 logger INFO: model backbone.conv2.1.conv2c.2.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,115 logger INFO: model backbone.conv2.1.conv2d.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,116 logger INFO: model backbone.conv2.1.conv2d.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,116 logger INFO: model backbone.conv2.1.conv2d.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,117 logger INFO: model backbone.conv2.1.conv2d.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,118 logger INFO: model backbone.conv2.1.conv2d.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,119 logger INFO: model backbone.conv2.1.conv2d.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,120 logger INFO: model backbone.conv2.1.conv2d.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,121 logger INFO: model backbone.conv2.1.conv2d.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,122 logger INFO: model backbone.conv2.1.conv2d.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,123 logger INFO: model backbone.conv2.1.conv2d.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,124 logger INFO: model backbone.conv2.1.conv2d.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,125 logger INFO: model backbone.conv2.1.conv2d.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,125 logger INFO: model backbone.conv2.1.conv2d.2.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,126 logger INFO: model backbone.conv2.1.conv2d.2.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,128 logger INFO: model backbone.conv2.1.conv2d.2.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,129 logger INFO: model backbone.conv2.1.conv2d.2.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,129 logger INFO: model backbone.conv2.1.conv2d.2.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,130 logger INFO: model backbone.conv2.1.conv2d.2.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,131 logger INFO: model backbone.conv2.1.conv2d.3.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,132 logger INFO: model backbone.conv2.1.conv2d.3.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,133 logger INFO: model backbone.conv2.1.conv2d.3.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,133 logger INFO: model backbone.conv2.1.conv2d.3.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,135 logger INFO: model backbone.conv2.1.conv2d.3.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,136 logger INFO: model backbone.conv2.1.conv2d.3.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,137 logger INFO: model backbone.conv2.1.gate.fc1.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,138 logger INFO: model backbone.conv2.1.gate.fc1.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,138 logger INFO: model backbone.conv2.1.gate.fc2.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,139 logger INFO: model backbone.conv2.1.gate.fc2.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,140 logger INFO: model backbone.conv2.1.conv3.conv.weight                      ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,141 logger INFO: model backbone.conv2.1.conv3.bn.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,142 logger INFO: model backbone.conv2.1.conv3.bn.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,142 logger INFO: model backbone.conv2.1.conv3.bn.running_mean                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,143 logger INFO: model backbone.conv2.1.conv3.bn.running_var                   ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,145 logger INFO: model backbone.conv2.2.0.conv.weight                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,146 logger INFO: model backbone.conv2.2.0.bn.weight                            ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,147 logger INFO: model backbone.conv2.2.0.bn.bias                              ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,148 logger INFO: model backbone.conv2.2.0.bn.running_mean                      ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,149 logger INFO: model backbone.conv2.2.0.bn.running_var                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,152 logger INFO: model backbone.conv3.0.conv1.conv.weight                      ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,153 logger INFO: model backbone.conv3.0.conv1.bn.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,155 logger INFO: model backbone.conv3.0.conv1.bn.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,156 logger INFO: model backbone.conv3.0.conv1.bn.running_mean                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,157 logger INFO: model backbone.conv3.0.conv1.bn.running_var                   ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,158 logger INFO: model backbone.conv3.0.conv2a.conv1.weight                    ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,160 logger INFO: model backbone.conv3.0.conv2a.conv2.weight                    ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,162 logger INFO: model backbone.conv3.0.conv2a.bn.weight                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,163 logger INFO: model backbone.conv3.0.conv2a.bn.bias                         ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,164 logger INFO: model backbone.conv3.0.conv2a.bn.running_mean                 ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,165 logger INFO: model backbone.conv3.0.conv2a.bn.running_var                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,165 logger INFO: model backbone.conv3.0.conv2b.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,166 logger INFO: model backbone.conv3.0.conv2b.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,167 logger INFO: model backbone.conv3.0.conv2b.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,168 logger INFO: model backbone.conv3.0.conv2b.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,169 logger INFO: model backbone.conv3.0.conv2b.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,170 logger INFO: model backbone.conv3.0.conv2b.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,170 logger INFO: model backbone.conv3.0.conv2b.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,171 logger INFO: model backbone.conv3.0.conv2b.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,172 logger INFO: model backbone.conv3.0.conv2b.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,173 logger INFO: model backbone.conv3.0.conv2b.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,174 logger INFO: model backbone.conv3.0.conv2b.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,175 logger INFO: model backbone.conv3.0.conv2b.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,176 logger INFO: model backbone.conv3.0.conv2c.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,177 logger INFO: model backbone.conv3.0.conv2c.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,178 logger INFO: model backbone.conv3.0.conv2c.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,179 logger INFO: model backbone.conv3.0.conv2c.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,180 logger INFO: model backbone.conv3.0.conv2c.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,181 logger INFO: model backbone.conv3.0.conv2c.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,182 logger INFO: model backbone.conv3.0.conv2c.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,183 logger INFO: model backbone.conv3.0.conv2c.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,184 logger INFO: model backbone.conv3.0.conv2c.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,185 logger INFO: model backbone.conv3.0.conv2c.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,186 logger INFO: model backbone.conv3.0.conv2c.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,187 logger INFO: model backbone.conv3.0.conv2c.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,188 logger INFO: model backbone.conv3.0.conv2c.2.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,189 logger INFO: model backbone.conv3.0.conv2c.2.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,189 logger INFO: model backbone.conv3.0.conv2c.2.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,190 logger INFO: model backbone.conv3.0.conv2c.2.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,191 logger INFO: model backbone.conv3.0.conv2c.2.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,191 logger INFO: model backbone.conv3.0.conv2c.2.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,195 logger INFO: model backbone.conv3.0.conv2d.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,196 logger INFO: model backbone.conv3.0.conv2d.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,197 logger INFO: model backbone.conv3.0.conv2d.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,198 logger INFO: model backbone.conv3.0.conv2d.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,199 logger INFO: model backbone.conv3.0.conv2d.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,199 logger INFO: model backbone.conv3.0.conv2d.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,200 logger INFO: model backbone.conv3.0.conv2d.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,201 logger INFO: model backbone.conv3.0.conv2d.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,201 logger INFO: model backbone.conv3.0.conv2d.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,202 logger INFO: model backbone.conv3.0.conv2d.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,203 logger INFO: model backbone.conv3.0.conv2d.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,203 logger INFO: model backbone.conv3.0.conv2d.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,204 logger INFO: model backbone.conv3.0.conv2d.2.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,205 logger INFO: model backbone.conv3.0.conv2d.2.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,206 logger INFO: model backbone.conv3.0.conv2d.2.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,207 logger INFO: model backbone.conv3.0.conv2d.2.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,207 logger INFO: model backbone.conv3.0.conv2d.2.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,208 logger INFO: model backbone.conv3.0.conv2d.2.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,209 logger INFO: model backbone.conv3.0.conv2d.3.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,210 logger INFO: model backbone.conv3.0.conv2d.3.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,213 logger INFO: model backbone.conv3.0.conv2d.3.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,214 logger INFO: model backbone.conv3.0.conv2d.3.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,215 logger INFO: model backbone.conv3.0.conv2d.3.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,216 logger INFO: model backbone.conv3.0.conv2d.3.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,217 logger INFO: model backbone.conv3.0.gate.fc1.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,218 logger INFO: model backbone.conv3.0.gate.fc1.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,219 logger INFO: model backbone.conv3.0.gate.fc2.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,219 logger INFO: model backbone.conv3.0.gate.fc2.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,221 logger INFO: model backbone.conv3.0.conv3.conv.weight                      ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,225 logger INFO: model backbone.conv3.0.conv3.bn.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,226 logger INFO: model backbone.conv3.0.conv3.bn.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,226 logger INFO: model backbone.conv3.0.conv3.bn.running_mean                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,228 logger INFO: model backbone.conv3.0.conv3.bn.running_var                   ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,230 logger INFO: model backbone.conv3.0.downsample.conv.weight                 ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,231 logger INFO: model backbone.conv3.0.downsample.bn.weight                   ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,232 logger INFO: model backbone.conv3.0.downsample.bn.bias                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,232 logger INFO: model backbone.conv3.0.downsample.bn.running_mean             ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,234 logger INFO: model backbone.conv3.0.downsample.bn.running_var              ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,236 logger INFO: model backbone.conv3.1.conv1.conv.weight                      ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,236 logger INFO: model backbone.conv3.1.conv1.bn.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,237 logger INFO: model backbone.conv3.1.conv1.bn.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,239 logger INFO: model backbone.conv3.1.conv1.bn.running_mean                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,239 logger INFO: model backbone.conv3.1.conv1.bn.running_var                   ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,240 logger INFO: model backbone.conv3.1.conv2a.conv1.weight                    ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,242 logger INFO: model backbone.conv3.1.conv2a.conv2.weight                    ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,243 logger INFO: model backbone.conv3.1.conv2a.bn.weight                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,244 logger INFO: model backbone.conv3.1.conv2a.bn.bias                         ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,249 logger INFO: model backbone.conv3.1.conv2a.bn.running_mean                 ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,250 logger INFO: model backbone.conv3.1.conv2a.bn.running_var                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,250 logger INFO: model backbone.conv3.1.conv2b.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,255 logger INFO: model backbone.conv3.1.conv2b.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,256 logger INFO: model backbone.conv3.1.conv2b.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,257 logger INFO: model backbone.conv3.1.conv2b.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,258 logger INFO: model backbone.conv3.1.conv2b.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,259 logger INFO: model backbone.conv3.1.conv2b.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,261 logger INFO: model backbone.conv3.1.conv2b.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,262 logger INFO: model backbone.conv3.1.conv2b.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,263 logger INFO: model backbone.conv3.1.conv2b.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,263 logger INFO: model backbone.conv3.1.conv2b.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,264 logger INFO: model backbone.conv3.1.conv2b.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,265 logger INFO: model backbone.conv3.1.conv2b.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,266 logger INFO: model backbone.conv3.1.conv2c.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,267 logger INFO: model backbone.conv3.1.conv2c.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,268 logger INFO: model backbone.conv3.1.conv2c.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,269 logger INFO: model backbone.conv3.1.conv2c.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,270 logger INFO: model backbone.conv3.1.conv2c.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,270 logger INFO: model backbone.conv3.1.conv2c.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,271 logger INFO: model backbone.conv3.1.conv2c.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,272 logger INFO: model backbone.conv3.1.conv2c.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,273 logger INFO: model backbone.conv3.1.conv2c.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,274 logger INFO: model backbone.conv3.1.conv2c.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,275 logger INFO: model backbone.conv3.1.conv2c.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,275 logger INFO: model backbone.conv3.1.conv2c.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,276 logger INFO: model backbone.conv3.1.conv2c.2.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,278 logger INFO: model backbone.conv3.1.conv2c.2.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,279 logger INFO: model backbone.conv3.1.conv2c.2.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,279 logger INFO: model backbone.conv3.1.conv2c.2.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,280 logger INFO: model backbone.conv3.1.conv2c.2.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,281 logger INFO: model backbone.conv3.1.conv2c.2.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,282 logger INFO: model backbone.conv3.1.conv2d.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,282 logger INFO: model backbone.conv3.1.conv2d.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,283 logger INFO: model backbone.conv3.1.conv2d.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,284 logger INFO: model backbone.conv3.1.conv2d.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,284 logger INFO: model backbone.conv3.1.conv2d.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,285 logger INFO: model backbone.conv3.1.conv2d.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,286 logger INFO: model backbone.conv3.1.conv2d.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,287 logger INFO: model backbone.conv3.1.conv2d.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,287 logger INFO: model backbone.conv3.1.conv2d.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,288 logger INFO: model backbone.conv3.1.conv2d.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,289 logger INFO: model backbone.conv3.1.conv2d.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,290 logger INFO: model backbone.conv3.1.conv2d.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,290 logger INFO: model backbone.conv3.1.conv2d.2.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,291 logger INFO: model backbone.conv3.1.conv2d.2.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,292 logger INFO: model backbone.conv3.1.conv2d.2.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,293 logger INFO: model backbone.conv3.1.conv2d.2.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,294 logger INFO: model backbone.conv3.1.conv2d.2.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,294 logger INFO: model backbone.conv3.1.conv2d.2.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,295 logger INFO: model backbone.conv3.1.conv2d.3.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,296 logger INFO: model backbone.conv3.1.conv2d.3.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,297 logger INFO: model backbone.conv3.1.conv2d.3.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,297 logger INFO: model backbone.conv3.1.conv2d.3.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,298 logger INFO: model backbone.conv3.1.conv2d.3.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,299 logger INFO: model backbone.conv3.1.conv2d.3.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,300 logger INFO: model backbone.conv3.1.gate.fc1.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,300 logger INFO: model backbone.conv3.1.gate.fc1.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,301 logger INFO: model backbone.conv3.1.gate.fc2.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,302 logger INFO: model backbone.conv3.1.gate.fc2.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,303 logger INFO: model backbone.conv3.1.conv3.conv.weight                      ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,304 logger INFO: model backbone.conv3.1.conv3.bn.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,305 logger INFO: model backbone.conv3.1.conv3.bn.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,306 logger INFO: model backbone.conv3.1.conv3.bn.running_mean                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,306 logger INFO: model backbone.conv3.1.conv3.bn.running_var                   ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,308 logger INFO: model backbone.conv3.2.0.conv.weight                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,308 logger INFO: model backbone.conv3.2.0.bn.weight                            ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,309 logger INFO: model backbone.conv3.2.0.bn.bias                              ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,309 logger INFO: model backbone.conv3.2.0.bn.running_mean                      ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,311 logger INFO: model backbone.conv3.2.0.bn.running_var                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,312 logger INFO: model backbone.conv4.0.conv1.conv.weight                      ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,313 logger INFO: model backbone.conv4.0.conv1.bn.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,313 logger INFO: model backbone.conv4.0.conv1.bn.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,314 logger INFO: model backbone.conv4.0.conv1.bn.running_mean                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,315 logger INFO: model backbone.conv4.0.conv1.bn.running_var                   ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,317 logger INFO: model backbone.conv4.0.conv2a.conv1.weight                    ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,317 logger INFO: model backbone.conv4.0.conv2a.conv2.weight                    ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,318 logger INFO: model backbone.conv4.0.conv2a.bn.weight                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,319 logger INFO: model backbone.conv4.0.conv2a.bn.bias                         ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,320 logger INFO: model backbone.conv4.0.conv2a.bn.running_mean                 ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,321 logger INFO: model backbone.conv4.0.conv2a.bn.running_var                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,322 logger INFO: model backbone.conv4.0.conv2b.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,323 logger INFO: model backbone.conv4.0.conv2b.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,324 logger INFO: model backbone.conv4.0.conv2b.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,325 logger INFO: model backbone.conv4.0.conv2b.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,326 logger INFO: model backbone.conv4.0.conv2b.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,327 logger INFO: model backbone.conv4.0.conv2b.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,328 logger INFO: model backbone.conv4.0.conv2b.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,329 logger INFO: model backbone.conv4.0.conv2b.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,329 logger INFO: model backbone.conv4.0.conv2b.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,330 logger INFO: model backbone.conv4.0.conv2b.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,331 logger INFO: model backbone.conv4.0.conv2b.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,332 logger INFO: model backbone.conv4.0.conv2b.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,332 logger INFO: model backbone.conv4.0.conv2c.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,333 logger INFO: model backbone.conv4.0.conv2c.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,334 logger INFO: model backbone.conv4.0.conv2c.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,335 logger INFO: model backbone.conv4.0.conv2c.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,336 logger INFO: model backbone.conv4.0.conv2c.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,336 logger INFO: model backbone.conv4.0.conv2c.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,337 logger INFO: model backbone.conv4.0.conv2c.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,338 logger INFO: model backbone.conv4.0.conv2c.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,339 logger INFO: model backbone.conv4.0.conv2c.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,340 logger INFO: model backbone.conv4.0.conv2c.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,340 logger INFO: model backbone.conv4.0.conv2c.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,341 logger INFO: model backbone.conv4.0.conv2c.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,342 logger INFO: model backbone.conv4.0.conv2c.2.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,343 logger INFO: model backbone.conv4.0.conv2c.2.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,344 logger INFO: model backbone.conv4.0.conv2c.2.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,345 logger INFO: model backbone.conv4.0.conv2c.2.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,346 logger INFO: model backbone.conv4.0.conv2c.2.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,346 logger INFO: model backbone.conv4.0.conv2c.2.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,347 logger INFO: model backbone.conv4.0.conv2d.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,348 logger INFO: model backbone.conv4.0.conv2d.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,349 logger INFO: model backbone.conv4.0.conv2d.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,350 logger INFO: model backbone.conv4.0.conv2d.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,350 logger INFO: model backbone.conv4.0.conv2d.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,352 logger INFO: model backbone.conv4.0.conv2d.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,353 logger INFO: model backbone.conv4.0.conv2d.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,354 logger INFO: model backbone.conv4.0.conv2d.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,355 logger INFO: model backbone.conv4.0.conv2d.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,356 logger INFO: model backbone.conv4.0.conv2d.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,357 logger INFO: model backbone.conv4.0.conv2d.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,358 logger INFO: model backbone.conv4.0.conv2d.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,359 logger INFO: model backbone.conv4.0.conv2d.2.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,360 logger INFO: model backbone.conv4.0.conv2d.2.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,361 logger INFO: model backbone.conv4.0.conv2d.2.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,362 logger INFO: model backbone.conv4.0.conv2d.2.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,362 logger INFO: model backbone.conv4.0.conv2d.2.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,363 logger INFO: model backbone.conv4.0.conv2d.2.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,364 logger INFO: model backbone.conv4.0.conv2d.3.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,365 logger INFO: model backbone.conv4.0.conv2d.3.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,366 logger INFO: model backbone.conv4.0.conv2d.3.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,366 logger INFO: model backbone.conv4.0.conv2d.3.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,368 logger INFO: model backbone.conv4.0.conv2d.3.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,368 logger INFO: model backbone.conv4.0.conv2d.3.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,369 logger INFO: model backbone.conv4.0.gate.fc1.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,370 logger INFO: model backbone.conv4.0.gate.fc1.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,371 logger INFO: model backbone.conv4.0.gate.fc2.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,372 logger INFO: model backbone.conv4.0.gate.fc2.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,373 logger INFO: model backbone.conv4.0.conv3.conv.weight                      ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,374 logger INFO: model backbone.conv4.0.conv3.bn.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,374 logger INFO: model backbone.conv4.0.conv3.bn.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,375 logger INFO: model backbone.conv4.0.conv3.bn.running_mean                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,376 logger INFO: model backbone.conv4.0.conv3.bn.running_var                   ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,377 logger INFO: model backbone.conv4.0.downsample.conv.weight                 ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,378 logger INFO: model backbone.conv4.0.downsample.bn.weight                   ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,379 logger INFO: model backbone.conv4.0.downsample.bn.bias                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,379 logger INFO: model backbone.conv4.0.downsample.bn.running_mean             ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,380 logger INFO: model backbone.conv4.0.downsample.bn.running_var              ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,381 logger INFO: model backbone.conv4.1.conv1.conv.weight                      ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,382 logger INFO: model backbone.conv4.1.conv1.bn.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,383 logger INFO: model backbone.conv4.1.conv1.bn.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,383 logger INFO: model backbone.conv4.1.conv1.bn.running_mean                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,384 logger INFO: model backbone.conv4.1.conv1.bn.running_var                   ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,385 logger INFO: model backbone.conv4.1.conv2a.conv1.weight                    ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,386 logger INFO: model backbone.conv4.1.conv2a.conv2.weight                    ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,386 logger INFO: model backbone.conv4.1.conv2a.bn.weight                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,387 logger INFO: model backbone.conv4.1.conv2a.bn.bias                         ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,388 logger INFO: model backbone.conv4.1.conv2a.bn.running_mean                 ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,389 logger INFO: model backbone.conv4.1.conv2a.bn.running_var                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,390 logger INFO: model backbone.conv4.1.conv2b.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,390 logger INFO: model backbone.conv4.1.conv2b.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,391 logger INFO: model backbone.conv4.1.conv2b.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,392 logger INFO: model backbone.conv4.1.conv2b.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,392 logger INFO: model backbone.conv4.1.conv2b.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,393 logger INFO: model backbone.conv4.1.conv2b.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,393 logger INFO: model backbone.conv4.1.conv2b.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,394 logger INFO: model backbone.conv4.1.conv2b.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,395 logger INFO: model backbone.conv4.1.conv2b.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,395 logger INFO: model backbone.conv4.1.conv2b.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,396 logger INFO: model backbone.conv4.1.conv2b.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,396 logger INFO: model backbone.conv4.1.conv2b.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,397 logger INFO: model backbone.conv4.1.conv2c.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,397 logger INFO: model backbone.conv4.1.conv2c.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,400 logger INFO: model backbone.conv4.1.conv2c.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,402 logger INFO: model backbone.conv4.1.conv2c.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,402 logger INFO: model backbone.conv4.1.conv2c.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,403 logger INFO: model backbone.conv4.1.conv2c.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,404 logger INFO: model backbone.conv4.1.conv2c.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,405 logger INFO: model backbone.conv4.1.conv2c.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,406 logger INFO: model backbone.conv4.1.conv2c.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,407 logger INFO: model backbone.conv4.1.conv2c.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,408 logger INFO: model backbone.conv4.1.conv2c.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,409 logger INFO: model backbone.conv4.1.conv2c.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,410 logger INFO: model backbone.conv4.1.conv2c.2.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,411 logger INFO: model backbone.conv4.1.conv2c.2.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,412 logger INFO: model backbone.conv4.1.conv2c.2.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,413 logger INFO: model backbone.conv4.1.conv2c.2.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,414 logger INFO: model backbone.conv4.1.conv2c.2.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,415 logger INFO: model backbone.conv4.1.conv2c.2.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,416 logger INFO: model backbone.conv4.1.conv2d.0.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,417 logger INFO: model backbone.conv4.1.conv2d.0.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,418 logger INFO: model backbone.conv4.1.conv2d.0.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,419 logger INFO: model backbone.conv4.1.conv2d.0.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,420 logger INFO: model backbone.conv4.1.conv2d.0.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,421 logger INFO: model backbone.conv4.1.conv2d.0.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,421 logger INFO: model backbone.conv4.1.conv2d.1.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,422 logger INFO: model backbone.conv4.1.conv2d.1.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,423 logger INFO: model backbone.conv4.1.conv2d.1.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,424 logger INFO: model backbone.conv4.1.conv2d.1.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,425 logger INFO: model backbone.conv4.1.conv2d.1.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,426 logger INFO: model backbone.conv4.1.conv2d.1.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,427 logger INFO: model backbone.conv4.1.conv2d.2.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,428 logger INFO: model backbone.conv4.1.conv2d.2.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,429 logger INFO: model backbone.conv4.1.conv2d.2.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,430 logger INFO: model backbone.conv4.1.conv2d.2.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,431 logger INFO: model backbone.conv4.1.conv2d.2.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,433 logger INFO: model backbone.conv4.1.conv2d.2.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,434 logger INFO: model backbone.conv4.1.conv2d.3.conv1.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,435 logger INFO: model backbone.conv4.1.conv2d.3.conv2.weight                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,435 logger INFO: model backbone.conv4.1.conv2d.3.bn.weight                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,436 logger INFO: model backbone.conv4.1.conv2d.3.bn.bias                       ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,437 logger INFO: model backbone.conv4.1.conv2d.3.bn.running_mean               ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,438 logger INFO: model backbone.conv4.1.conv2d.3.bn.running_var                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,439 logger INFO: model backbone.conv4.1.gate.fc1.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,439 logger INFO: model backbone.conv4.1.gate.fc1.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,440 logger INFO: model backbone.conv4.1.gate.fc2.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,441 logger INFO: model backbone.conv4.1.gate.fc2.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,442 logger INFO: model backbone.conv4.1.conv3.conv.weight                      ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,444 logger INFO: model backbone.conv4.1.conv3.bn.weight                        ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,445 logger INFO: model backbone.conv4.1.conv3.bn.bias                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,446 logger INFO: model backbone.conv4.1.conv3.bn.running_mean                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,447 logger INFO: model backbone.conv4.1.conv3.bn.running_var                   ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,448 logger INFO: model backbone.conv5.conv.weight                              ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,449 logger INFO: model backbone.conv5.bn.weight                                ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,450 logger INFO: model backbone.conv5.bn.bias                                  ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,451 logger INFO: model backbone.conv5.bn.running_mean                          ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,452 logger INFO: model backbone.conv5.bn.running_var                           ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,455 logger INFO: model BNNeck.weight                                           ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,456 logger INFO: model BNNeck.bias                                             ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,460 logger INFO: model BNNeck.running_mean                                     ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,461 logger INFO: model BNNeck.running_var                                      ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,461 logger INFO: model BNNeck.num_batches_tracked                              ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,486 logger INFO: model id_fc.weight                                            ...... <span class="ansi-green-intense-fg">loaded</span>
2019-11-21 09:13:19,553 logger INFO: loss_0 is skipped
2019-11-21 09:13:19,560 logger INFO: 
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[26]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">manager</span><span class="o">.</span><span class="n">model</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[26]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Model(
  (backbone): OSNet(
    (conv1): ConvLayer(
      (conv): Conv2d(3, 64, kernel_size=(7, 7), stride=(2, 2), padding=(3, 3), bias=False)
      (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
    )
    (maxpool): MaxPool2d(kernel_size=3, stride=2, padding=1, dilation=1, ceil_mode=False)
    (conv2): Sequential(
      (0): OSBlock(
        (conv1): Conv1x1(
          (conv): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
        )
        (conv2a): LightConv3x3(
          (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
          (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
        )
        (conv2b): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (conv2c): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (2): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (conv2d): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (2): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (3): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (gate): ChannelGate(
          (global_avgpool): AdaptiveAvgPool2d(output_size=1)
          (fc1): Conv2d(64, 4, kernel_size=(1, 1), stride=(1, 1))
          (elu): ReLU(inplace)
          (fc2): Conv2d(4, 64, kernel_size=(1, 1), stride=(1, 1))
          (gate_activation): Sigmoid()
        )
        (conv3): Conv1x1Linear(
          (conv): Conv2d(64, 256, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(256, eps=1e-05, momentum=0.1, affine=True, activation=identity)
        )
        (downsample): Conv1x1Linear(
          (conv): Conv2d(64, 256, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(256, eps=1e-05, momentum=0.1, affine=True, activation=identity)
        )
      )
      (1): OSBlock(
        (conv1): Conv1x1(
          (conv): Conv2d(256, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
        )
        (conv2a): LightConv3x3(
          (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
          (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
        )
        (conv2b): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (conv2c): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (2): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (conv2d): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (2): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (3): LightConv3x3(
            (conv1): Conv2d(64, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(64, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=64, bias=False)
            (bn): InPlaceABN(64, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (gate): ChannelGate(
          (global_avgpool): AdaptiveAvgPool2d(output_size=1)
          (fc1): Conv2d(64, 4, kernel_size=(1, 1), stride=(1, 1))
          (elu): ReLU(inplace)
          (fc2): Conv2d(4, 64, kernel_size=(1, 1), stride=(1, 1))
          (gate_activation): Sigmoid()
        )
        (conv3): Conv1x1Linear(
          (conv): Conv2d(64, 256, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(256, eps=1e-05, momentum=0.1, affine=True, activation=identity)
        )
      )
      (2): Sequential(
        (0): Conv1x1(
          (conv): Conv2d(256, 256, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(256, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
        )
        (1): AvgPool2d(kernel_size=2, stride=2, padding=0)
      )
    )
    (conv3): Sequential(
      (0): OSBlock(
        (conv1): Conv1x1(
          (conv): Conv2d(256, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
        )
        (conv2a): LightConv3x3(
          (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
          (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
        )
        (conv2b): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (conv2c): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (2): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (conv2d): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (2): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (3): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (gate): ChannelGate(
          (global_avgpool): AdaptiveAvgPool2d(output_size=1)
          (fc1): Conv2d(96, 6, kernel_size=(1, 1), stride=(1, 1))
          (elu): ReLU(inplace)
          (fc2): Conv2d(6, 96, kernel_size=(1, 1), stride=(1, 1))
          (gate_activation): Sigmoid()
        )
        (conv3): Conv1x1Linear(
          (conv): Conv2d(96, 384, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(384, eps=1e-05, momentum=0.1, affine=True, activation=identity)
        )
        (downsample): Conv1x1Linear(
          (conv): Conv2d(256, 384, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(384, eps=1e-05, momentum=0.1, affine=True, activation=identity)
        )
      )
      (1): OSBlock(
        (conv1): Conv1x1(
          (conv): Conv2d(384, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
        )
        (conv2a): LightConv3x3(
          (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
          (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
        )
        (conv2b): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (conv2c): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (2): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (conv2d): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (2): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (3): LightConv3x3(
            (conv1): Conv2d(96, 96, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(96, 96, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=96, bias=False)
            (bn): InPlaceABN(96, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (gate): ChannelGate(
          (global_avgpool): AdaptiveAvgPool2d(output_size=1)
          (fc1): Conv2d(96, 6, kernel_size=(1, 1), stride=(1, 1))
          (elu): ReLU(inplace)
          (fc2): Conv2d(6, 96, kernel_size=(1, 1), stride=(1, 1))
          (gate_activation): Sigmoid()
        )
        (conv3): Conv1x1Linear(
          (conv): Conv2d(96, 384, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(384, eps=1e-05, momentum=0.1, affine=True, activation=identity)
        )
      )
      (2): Sequential(
        (0): Conv1x1(
          (conv): Conv2d(384, 384, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(384, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
        )
        (1): AvgPool2d(kernel_size=2, stride=2, padding=0)
      )
    )
    (conv4): Sequential(
      (0): OSBlock(
        (conv1): Conv1x1(
          (conv): Conv2d(384, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
        )
        (conv2a): LightConv3x3(
          (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
          (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
        )
        (conv2b): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (conv2c): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (2): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (conv2d): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (2): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (3): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (gate): ChannelGate(
          (global_avgpool): AdaptiveAvgPool2d(output_size=1)
          (fc1): Conv2d(128, 8, kernel_size=(1, 1), stride=(1, 1))
          (elu): ReLU(inplace)
          (fc2): Conv2d(8, 128, kernel_size=(1, 1), stride=(1, 1))
          (gate_activation): Sigmoid()
        )
        (conv3): Conv1x1Linear(
          (conv): Conv2d(128, 512, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(512, eps=1e-05, momentum=0.1, affine=True, activation=identity)
        )
        (downsample): Conv1x1Linear(
          (conv): Conv2d(384, 512, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(512, eps=1e-05, momentum=0.1, affine=True, activation=identity)
        )
      )
      (1): OSBlock(
        (conv1): Conv1x1(
          (conv): Conv2d(512, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
        )
        (conv2a): LightConv3x3(
          (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
          (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
        )
        (conv2b): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (conv2c): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (2): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (conv2d): Sequential(
          (0): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (1): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (2): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
          (3): LightConv3x3(
            (conv1): Conv2d(128, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
            (conv2): Conv2d(128, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), groups=128, bias=False)
            (bn): InPlaceABN(128, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
          )
        )
        (gate): ChannelGate(
          (global_avgpool): AdaptiveAvgPool2d(output_size=1)
          (fc1): Conv2d(128, 8, kernel_size=(1, 1), stride=(1, 1))
          (elu): ReLU(inplace)
          (fc2): Conv2d(8, 128, kernel_size=(1, 1), stride=(1, 1))
          (gate_activation): Sigmoid()
        )
        (conv3): Conv1x1Linear(
          (conv): Conv2d(128, 512, kernel_size=(1, 1), stride=(1, 1), bias=False)
          (bn): InPlaceABN(512, eps=1e-05, momentum=0.1, affine=True, activation=identity)
        )
      )
    )
    (conv5): Conv1x1(
      (conv): Conv2d(512, 512, kernel_size=(1, 1), stride=(1, 1), bias=False)
      (bn): InPlaceABN(512, eps=1e-05, momentum=0.1, affine=True, activation=leaky_relu[0.01])
    )
    (global_pool): AdaptiveAvgPool2d(output_size=1)
  )
  (gap): AdaptiveAvgPool2d(output_size=1)
  (BNNeck): BatchNorm1d(512, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
  (id_fc): Linear(in_features=512, out_features=5297, bias=False)
)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">deepfashion</span> <span class="o">=</span> <span class="n">get_img_data</span><span class="p">(</span><span class="n">cfg</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>loading annotations into memory...
Done (t=9.41s)
creating index...
index created!
2019-11-20 13:18:10,700 logger INFO: =&gt; DeepFashion2 is loaded
2019-11-20 13:18:10,701 logger INFO: Dataset statistics:
2019-11-20 13:18:10,702 logger INFO:   -------------------
2019-11-20 13:18:10,703 logger INFO:   subset   | # images
2019-11-20 13:18:10,704 logger INFO:   -------------------
2019-11-20 13:18:10,704 logger INFO:   val      |    32153
2019-11-20 13:18:10,705 logger INFO:   -------------------
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">dataset</span> <span class="o">=</span> <span class="n">build_DFKP_dataset</span><span class="p">(</span><span class="n">deepfashion</span><span class="o">.</span><span class="n">val_handle</span><span class="p">,</span> <span class="n">deepfashion</span><span class="o">.</span><span class="n">val_images</span><span class="p">,</span> <span class="n">src</span><span class="o">=</span><span class="n">deepfashion</span><span class="o">.</span><span class="n">val_dir</span><span class="p">,</span> <span class="n">split</span><span class="o">=</span><span class="s1">&#39;train&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">dataset</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[4]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>{&#39;input&#39;: array([[[-0.41176468, -0.41176468, -0.41960782, ..., -1.        ,
          -1.        , -1.        ],
         [-0.41176468, -0.40392154, -0.41176468, ..., -1.        ,
          -1.        , -1.        ],
         [-0.41176468, -0.3960784 , -0.40392154, ..., -1.        ,
          -1.        , -1.        ],
         ...,
         [ 0.05882359,  0.05882359,  0.06666672, ..., -1.        ,
          -1.        , -1.        ],
         [ 0.06666672,  0.06666672,  0.06666672, ..., -1.        ,
          -1.        , -1.        ],
         [ 0.07450986,  0.06666672,  0.07450986, ..., -1.        ,
          -1.        , -1.        ]],
 
        [[-0.3333333 , -0.3333333 , -0.34117645, ..., -1.        ,
          -1.        , -1.        ],
         [-0.3333333 , -0.32549018, -0.3333333 , ..., -1.        ,
          -1.        , -1.        ],
         [-0.3333333 , -0.31764704, -0.32549018, ..., -1.        ,
          -1.        , -1.        ],
         ...,
         [ 0.14509809,  0.14509809,  0.16078436, ..., -1.        ,
          -1.        , -1.        ],
         [ 0.16078436,  0.15294123,  0.16078436, ..., -1.        ,
          -1.        , -1.        ],
         [ 0.1686275 ,  0.16078436,  0.16078436, ..., -1.        ,
          -1.        , -1.        ]],
 
        [[-0.19999999, -0.19999999, -0.20784312, ..., -1.        ,
          -1.        , -1.        ],
         [-0.19215685, -0.18431371, -0.19215685, ..., -1.        ,
          -1.        , -1.        ],
         [-0.19215685, -0.17647058, -0.18431371, ..., -1.        ,
          -1.        , -1.        ],
         ...,
         [ 0.2313726 ,  0.2313726 ,  0.23921573, ..., -1.        ,
          -1.        , -1.        ],
         [ 0.23921573,  0.23921573,  0.23921573, ..., -1.        ,
          -1.        , -1.        ],
         [ 0.24705887,  0.23921573,  0.24705887, ..., -1.        ,
          -1.        , -1.        ]]], dtype=float32),
 &#39;hm&#39;: array([[[0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         ...,
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.]],
 
        [[0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         ...,
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.]],
 
        [[0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         ...,
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.]],
 
        ...,
 
        [[0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         ...,
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.]],
 
        [[0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         ...,
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.]],
 
        [[0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         ...,
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.]]], dtype=float32),
 &#39;wh&#39;: array([[24.20501 , 61.192467],
        [23.933052, 21.485355],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ],
        [ 0.      ,  0.      ]], dtype=float32),
 &#39;reg&#39;: array([[0.8630562 , 0.18279648],
        [0.36724472, 0.6012039 ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ],
        [0.        , 0.        ]], dtype=float32),
 &#39;reg_mask&#39;: array([1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,
        0, 0, 0, 0, 0, 0, 0, 0, 0, 0], dtype=uint8),
 &#39;ind&#39;: array([7230, 4669,    0,    0,    0,    0,    0,    0,    0,    0,    0,
           0,    0,    0,    0,    0,    0,    0,    0,    0,    0,    0,
           0,    0,    0,    0,    0,    0,    0,    0,    0,    0]),
 &#39;hm_hp&#39;: array([[[0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         ...,
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.]],
 
        [[0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         ...,
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.]],
 
        [[0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         ...,
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.]],
 
        ...,
 
        [[0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         ...,
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.]],
 
        [[0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         ...,
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.]],
 
        [[0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         ...,
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.],
         [0., 0., 0., ..., 0., 0., 0.]]], dtype=float32),
 &#39;hps&#39;: array([[  0.       ,   0.       ,   0.       , ...,   0.       ,
           6.1664047, -29.869501 ],
        [  0.       ,   0.       ,   0.       , ...,   0.       ,
           0.       ,   0.       ],
        [  0.       ,   0.       ,   0.       , ...,   0.       ,
           0.       ,   0.       ],
        ...,
        [  0.       ,   0.       ,   0.       , ...,   0.       ,
           0.       ,   0.       ],
        [  0.       ,   0.       ,   0.       , ...,   0.       ,
           0.       ,   0.       ],
        [  0.       ,   0.       ,   0.       , ...,   0.       ,
           0.       ,   0.       ]], dtype=float32),
 &#39;hp_offset&#39;: array([[0., 0.],
        [0., 0.],
        [0., 0.],
        ...,
        [0., 0.],
        [0., 0.],
        [0., 0.]], dtype=float32),
 &#39;hps_mask&#39;: array([[0, 0, 0, ..., 0, 1, 1],
        [0, 0, 0, ..., 0, 0, 0],
        [0, 0, 0, ..., 0, 0, 0],
        ...,
        [0, 0, 0, ..., 0, 0, 0],
        [0, 0, 0, ..., 0, 0, 0],
        [0, 0, 0, ..., 0, 0, 0]], dtype=uint8),
 &#39;hp_ind&#39;: array([0, 0, 0, ..., 0, 0, 0]),
 &#39;hp_mask&#39;: array([0, 0, 0, ..., 0, 0, 0])}</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">torch</span>
<span class="n">loader</span> <span class="o">=</span> <span class="n">torch</span><span class="o">.</span><span class="n">utils</span><span class="o">.</span><span class="n">data</span><span class="o">.</span><span class="n">DataLoader</span><span class="p">(</span>
    <span class="n">dataset</span><span class="p">,</span> 
    <span class="n">batch_size</span><span class="o">=</span><span class="mi">10</span><span class="p">,</span> <span class="n">shuffle</span><span class="o">=</span><span class="kc">False</span><span class="p">,</span> <span class="n">num_workers</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">pin_memory</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="n">batch</span> <span class="o">=</span> <span class="nb">next</span><span class="p">(</span><span class="nb">iter</span><span class="p">(</span><span class="n">loader</span><span class="p">))</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">batch</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[7]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>{&#39;input&#39;: tensor([[[[-1.0000, -1.0000, -1.0000,  ..., -0.6000, -0.5922, -0.5922],
           [-1.0000, -1.0000, -1.0000,  ..., -0.6000, -0.5922, -0.5843],
           [-1.0000, -1.0000, -1.0000,  ..., -0.6000, -0.5922, -0.5843],
           ...,
           [-1.0000, -1.0000, -1.0000,  ...,  0.0118,  0.0118,  0.0118],
           [-1.0000, -1.0000, -1.0000,  ...,  0.0196,  0.0196,  0.0196],
           [-1.0000, -1.0000, -1.0000,  ...,  0.0275,  0.0353,  0.0353]],
 
          [[-1.0000, -1.0000, -1.0000,  ..., -0.5451, -0.5373, -0.5294],
           [-1.0000, -1.0000, -1.0000,  ..., -0.5373, -0.5294, -0.5216],
           [-1.0000, -1.0000, -1.0000,  ..., -0.5373, -0.5294, -0.5216],
           ...,
           [-1.0000, -1.0000, -1.0000,  ...,  0.1529,  0.1529,  0.1529],
           [-1.0000, -1.0000, -1.0000,  ...,  0.1529,  0.1608,  0.1608],
           [-1.0000, -1.0000, -1.0000,  ...,  0.1686,  0.1686,  0.1765]],
 
          [[-1.0000, -1.0000, -1.0000,  ..., -0.4039, -0.3961, -0.3961],
           [-1.0000, -1.0000, -1.0000,  ..., -0.4039, -0.3961, -0.3882],
           [-1.0000, -1.0000, -1.0000,  ..., -0.4039, -0.3961, -0.3882],
           ...,
           [-1.0000, -1.0000, -1.0000,  ...,  0.2078,  0.2078,  0.2078],
           [-1.0000, -1.0000, -1.0000,  ...,  0.2078,  0.2157,  0.2157],
           [-1.0000, -1.0000, -1.0000,  ...,  0.2235,  0.2235,  0.2314]]],
 
 
         [[[-0.3412, -0.3333, -0.3098,  ..., -1.0000, -1.0000, -1.0000],
           [-0.3333, -0.3333, -0.3255,  ..., -1.0000, -1.0000, -1.0000],
           [-0.3255, -0.3333, -0.3333,  ..., -1.0000, -1.0000, -1.0000],
           ...,
           [ 0.0745,  0.0745,  0.0745,  ..., -1.0000, -1.0000, -1.0000],
           [ 0.0824,  0.0745,  0.0667,  ..., -1.0000, -1.0000, -1.0000],
           [ 0.0745,  0.0667,  0.0588,  ..., -1.0000, -1.0000, -1.0000]],
 
          [[-0.2863, -0.2784, -0.2549,  ..., -1.0000, -1.0000, -1.0000],
           [-0.2863, -0.2784, -0.2627,  ..., -1.0000, -1.0000, -1.0000],
           [-0.2706, -0.2784, -0.2784,  ..., -1.0000, -1.0000, -1.0000],
           ...,
           [ 0.1765,  0.1765,  0.1765,  ..., -1.0000, -1.0000, -1.0000],
           [ 0.1843,  0.1765,  0.1686,  ..., -1.0000, -1.0000, -1.0000],
           [ 0.1765,  0.1686,  0.1608,  ..., -1.0000, -1.0000, -1.0000]],
 
          [[-0.1765, -0.1608, -0.1373,  ..., -1.0000, -1.0000, -1.0000],
           [-0.1686, -0.1608, -0.1451,  ..., -1.0000, -1.0000, -1.0000],
           [-0.1529, -0.1608, -0.1608,  ..., -1.0000, -1.0000, -1.0000],
           ...,
           [ 0.2000,  0.1922,  0.1922,  ..., -1.0000, -1.0000, -1.0000],
           [ 0.2000,  0.1922,  0.1843,  ..., -1.0000, -1.0000, -1.0000],
           [ 0.1922,  0.1843,  0.1765,  ..., -1.0000, -1.0000, -1.0000]]],
 
 
         [[[-1.0000, -1.0000, -1.0000,  ...,  0.2784,  0.3255,  0.3176],
           [-1.0000, -1.0000, -1.0000,  ...,  0.2392,  0.3333,  0.3725],
           [-1.0000, -1.0000, -1.0000,  ...,  0.1843,  0.3020,  0.3647],
           ...,
           [-1.0000, -1.0000, -1.0000,  ..., -0.3098, -0.3647, -0.4275],
           [-1.0000, -1.0000, -1.0000,  ..., -0.3098, -0.3569, -0.4196],
           [-1.0000, -1.0000, -1.0000,  ..., -0.3098, -0.3490, -0.4196]],
 
          [[-1.0000, -1.0000, -1.0000,  ...,  0.6157,  0.6549,  0.6392],
           [-1.0000, -1.0000, -1.0000,  ...,  0.5765,  0.6627,  0.6941],
           [-1.0000, -1.0000, -1.0000,  ...,  0.5137,  0.6235,  0.6784],
           ...,
           [-1.0000, -1.0000, -1.0000,  ..., -0.1765, -0.2235, -0.2784],
           [-1.0000, -1.0000, -1.0000,  ..., -0.1765, -0.2078, -0.2706],
           [-1.0000, -1.0000, -1.0000,  ..., -0.1765, -0.2000, -0.2627]],
 
          [[-1.0000, -1.0000, -1.0000,  ...,  0.6549,  0.6941,  0.6784],
           [-1.0000, -1.0000, -1.0000,  ...,  0.6078,  0.7020,  0.7333],
           [-1.0000, -1.0000, -1.0000,  ...,  0.5529,  0.6627,  0.7176],
           ...,
           [-1.0000, -1.0000, -1.0000,  ..., -0.1216, -0.1686, -0.2314],
           [-1.0000, -1.0000, -1.0000,  ..., -0.1216, -0.1608, -0.2235],
           [-1.0000, -1.0000, -1.0000,  ..., -0.1294, -0.1608, -0.2314]]],
 
 
         ...,
 
 
         [[[-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           ...,
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000]],
 
          [[-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           ...,
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000]],
 
          [[-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           ...,
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000]]],
 
 
         [[[-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           ...,
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000]],
 
          [[-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           ...,
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000]],
 
          [[-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           ...,
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000],
           [-1.0000, -1.0000, -1.0000,  ..., -1.0000, -1.0000, -1.0000]]],
 
 
         [[[-0.6863, -0.6863, -0.6784,  ...,  0.9451,  0.9765,  0.9765],
           [-0.6784, -0.6784, -0.6863,  ...,  0.9451,  0.9686,  0.9765],
           [-0.6784, -0.6784, -0.6863,  ...,  0.9608,  0.9608,  0.9765],
           ...,
           [-0.7569, -0.7490, -0.7412,  ..., -0.7490, -0.7490, -0.7490],
           [-0.7490, -0.7412, -0.7412,  ..., -0.7569, -0.7569, -0.7569],
           [-0.7176, -0.7098, -0.7098,  ..., -0.7490, -0.7490, -0.7490]],
 
          [[-0.7569, -0.7569, -0.7490,  ...,  0.8353,  0.8902,  0.8824],
           [-0.7490, -0.7490, -0.7569,  ...,  0.8353,  0.8667,  0.8824],
           [-0.7490, -0.7490, -0.7569,  ...,  0.8431,  0.8588,  0.8824],
           ...,
           [-0.8196, -0.8118, -0.8039,  ..., -0.7804, -0.7804, -0.7804],
           [-0.8118, -0.8039, -0.8039,  ..., -0.7882, -0.7882, -0.7882],
           [-0.7961, -0.7882, -0.7804,  ..., -0.7961, -0.7961, -0.7961]],
 
          [[-0.8588, -0.8588, -0.8510,  ...,  0.7490,  0.8118,  0.8039],
           [-0.8510, -0.8510, -0.8588,  ...,  0.7569,  0.7961,  0.8039],
           [-0.8510, -0.8510, -0.8588,  ...,  0.7725,  0.7882,  0.8118],
           ...,
           [-0.8745, -0.8667, -0.8667,  ..., -0.8667, -0.8667, -0.8667],
           [-0.8667, -0.8588, -0.8588,  ..., -0.8745, -0.8745, -0.8745],
           [-0.8510, -0.8431, -0.8353,  ..., -0.8824, -0.8824, -0.8824]]]]),
 &#39;hm&#39;: tensor([[[[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          ...,
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]]],
 
 
         [[[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          ...,
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]]],
 
 
         [[[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          ...,
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]]],
 
 
         ...,
 
 
         [[[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          ...,
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]]],
 
 
         [[[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          ...,
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]]],
 
 
         [[[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          ...,
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]]]]),
 &#39;wh&#39;: tensor([[[ 30.4273,  76.9231],
          [ 30.0855,  27.0085],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000]],
 
         [[ 31.7131,  71.9013],
          [ 30.0728,  25.6986],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000]],
 
         [[ 41.8621,  63.4472],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000]],
 
         [[ 27.4826,  33.7695],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000]],
 
         [[ 88.6292, 127.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000]],
 
         [[ 78.9743,  73.7970],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000]],
 
         [[ 32.7034,  67.2611],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000]],
 
         [[ 96.5333, 127.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000]],
 
         [[ 53.0403,  52.7473],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000]],
 
         [[ 88.3782, 127.0000],
          [ 83.0662, 127.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000],
          [  0.0000,   0.0000]]]),
 &#39;reg&#39;: tensor([[[0.5873, 0.6539],
          [0.7069, 0.0385],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000]],
 
         [[0.8810, 0.9721],
          [0.4205, 0.1442],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000]],
 
         [[0.7343, 0.2900],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000]],
 
         [[0.2606, 0.8074],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000]],
 
         [[0.6854, 0.5000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000]],
 
         [[0.7719, 0.1015],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000]],
 
         [[0.2315, 0.5171],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000]],
 
         [[0.5172, 0.5000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000]],
 
         [[0.0037, 0.3620],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000]],
 
         [[0.8109, 0.5000],
          [0.5331, 0.5000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000],
          [0.0000, 0.0000]]]),
 &#39;reg_mask&#39;: tensor([[1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,
          0, 0, 0, 0, 0, 0, 0, 0],
         [1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,
          0, 0, 0, 0, 0, 0, 0, 0],
         [1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,
          0, 0, 0, 0, 0, 0, 0, 0],
         [1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,
          0, 0, 0, 0, 0, 0, 0, 0],
         [1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,
          0, 0, 0, 0, 0, 0, 0, 0],
         [1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,
          0, 0, 0, 0, 0, 0, 0, 0],
         [1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,
          0, 0, 0, 0, 0, 0, 0, 0],
         [1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,
          0, 0, 0, 0, 0, 0, 0, 0],
         [1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,
          0, 0, 0, 0, 0, 0, 0, 0],
         [1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,
          0, 0, 0, 0, 0, 0, 0, 0]], dtype=torch.uint8),
 &#39;ind&#39;: tensor([[ 9951,  6877,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0],
         [ 7965,  5147,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0],
         [11852,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0],
         [ 6195,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0],
         [ 8146,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0],
         [11581,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0],
         [ 9672,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0],
         [ 8136,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0],
         [10546,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0],
         [ 8146,  8105,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0,     0,     0,     0,     0,     0,     0,     0,     0,
              0,     0]]),
 &#39;hm_hp&#39;: tensor([[[[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          ...,
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]]],
 
 
         [[[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          ...,
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]]],
 
 
         [[[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          ...,
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]]],
 
 
         ...,
 
 
         [[[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          ...,
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]]],
 
 
         [[[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          ...,
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]]],
 
 
         [[[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          ...,
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]],
 
          [[0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           ...,
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.],
           [0., 0., 0.,  ..., 0., 0., 0.]]]]),
 &#39;hps&#39;: tensor([[[  0.0000,   0.0000,   0.0000,  ...,   0.0000,   7.2539, -37.1238],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          ...,
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000]],
 
         [[  0.0000,   0.0000,   0.0000,  ...,   0.0000,   6.0754, -34.7051],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          ...,
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000]],
 
         [[  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          ...,
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000]],
 
         ...,
 
         [[  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          ...,
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000]],
 
         [[  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          ...,
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000]],
 
         [[  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          ...,
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000],
          [  0.0000,   0.0000,   0.0000,  ...,   0.0000,   0.0000,   0.0000]]]),
 &#39;hp_offset&#39;: tensor([[[0., 0.],
          [0., 0.],
          [0., 0.],
          ...,
          [0., 0.],
          [0., 0.],
          [0., 0.]],
 
         [[0., 0.],
          [0., 0.],
          [0., 0.],
          ...,
          [0., 0.],
          [0., 0.],
          [0., 0.]],
 
         [[0., 0.],
          [0., 0.],
          [0., 0.],
          ...,
          [0., 0.],
          [0., 0.],
          [0., 0.]],
 
         ...,
 
         [[0., 0.],
          [0., 0.],
          [0., 0.],
          ...,
          [0., 0.],
          [0., 0.],
          [0., 0.]],
 
         [[0., 0.],
          [0., 0.],
          [0., 0.],
          ...,
          [0., 0.],
          [0., 0.],
          [0., 0.]],
 
         [[0., 0.],
          [0., 0.],
          [0., 0.],
          ...,
          [0., 0.],
          [0., 0.],
          [0., 0.]]]),
 &#39;hps_mask&#39;: tensor([[[0, 0, 0,  ..., 0, 1, 1],
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0],
          ...,
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0]],
 
         [[0, 0, 0,  ..., 0, 1, 1],
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0],
          ...,
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0]],
 
         [[0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0],
          ...,
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0]],
 
         ...,
 
         [[0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0],
          ...,
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0]],
 
         [[0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0],
          ...,
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0]],
 
         [[0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0],
          ...,
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0],
          [0, 0, 0,  ..., 0, 0, 0]]], dtype=torch.uint8),
 &#39;hp_ind&#39;: tensor([[0, 0, 0,  ..., 0, 0, 0],
         [0, 0, 0,  ..., 0, 0, 0],
         [0, 0, 0,  ..., 0, 0, 0],
         ...,
         [0, 0, 0,  ..., 0, 0, 0],
         [0, 0, 0,  ..., 0, 0, 0],
         [0, 0, 0,  ..., 0, 0, 0]]),
 &#39;hp_mask&#39;: tensor([[0, 0, 0,  ..., 0, 0, 0],
         [0, 0, 0,  ..., 0, 0, 0],
         [0, 0, 0,  ..., 0, 0, 0],
         ...,
         [0, 0, 0,  ..., 0, 0, 0],
         [0, 0, 0,  ..., 0, 0, 0],
         [0, 0, 0,  ..., 0, 0, 0]])}</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">pycocotools.coco</span> <span class="k">as</span> <span class="nn">coco</span>
<span class="kn">import</span> <span class="nn">os.path</span> <span class="k">as</span> <span class="nn">osp</span>
<span class="kn">from</span> <span class="nn">tools.logger</span> <span class="kn">import</span> <span class="n">setup_logger</span>
<span class="n">logger</span> <span class="o">=</span> <span class="n">setup_logger</span><span class="p">(</span><span class="s2">&quot;.&quot;</span><span class="p">)</span>

<span class="k">class</span> <span class="nc">DeepFashion2</span><span class="p">():</span>
    <span class="k">def</span> <span class="fm">__init__</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">cfg</span><span class="p">):</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">dataset_dir</span> <span class="o">=</span> <span class="n">cfg</span><span class="o">.</span><span class="n">DATASET</span><span class="o">.</span><span class="n">TRAIN_PATH</span>       
        <span class="bp">self</span><span class="o">.</span><span class="n">train_dir</span> <span class="o">=</span> <span class="n">osp</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">dataset_dir</span><span class="p">,</span> <span class="s2">&quot;train/image&quot;</span><span class="p">)</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">val_dir</span> <span class="o">=</span> <span class="n">osp</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">dataset_dir</span><span class="p">,</span> <span class="s2">&quot;validation/image&quot;</span><span class="p">)</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">train_anno</span> <span class="o">=</span> <span class="n">osp</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">dataset_dir</span><span class="p">,</span> <span class="s2">&quot;deepfashion2_train.json&quot;</span><span class="p">)</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">val_anno</span> <span class="o">=</span> <span class="n">osp</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">dataset_dir</span><span class="p">,</span> <span class="s2">&quot;deepfashion2_validation.json&quot;</span><span class="p">)</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">_check_before_run</span><span class="p">()</span>
        
<span class="c1">#         train_handle, train_images, train_num_samples = self._process_dir(self.train_anno)</span>
        <span class="n">val_handle</span><span class="p">,</span> <span class="n">val_images</span><span class="p">,</span> <span class="n">val_num_samples</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">_process_dir</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">val_anno</span><span class="p">)</span>
        
        <span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="s2">&quot;=&gt; DeepFashion2 is loaded&quot;</span><span class="p">)</span>
        <span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="s2">&quot;Dataset statistics:&quot;</span><span class="p">)</span>
        <span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="s2">&quot;  -------------------&quot;</span><span class="p">)</span>
        <span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="s2">&quot;  subset   | # images&quot;</span><span class="p">)</span>
        <span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="s2">&quot;  -------------------&quot;</span><span class="p">)</span>
<span class="c1">#         logger.info(&quot;  train    | {:8d}&quot;.format(train_num_samples))</span>
        <span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="s2">&quot;  val      | </span><span class="si">{:8d}</span><span class="s2">&quot;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">val_num_samples</span><span class="p">))</span>
        <span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="s2">&quot;  -------------------&quot;</span><span class="p">)</span>
        
<span class="c1">#         self.train_handle = train_handle</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">val_handle</span> <span class="o">=</span> <span class="n">val_handle</span>
<span class="c1">#         self.train_images = train_images</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">val_images</span> <span class="o">=</span> <span class="n">val_images</span>
        
    <span class="k">def</span> <span class="nf">_check_before_run</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
        <span class="sd">&quot;&quot;&quot;Check if all files are available before going deeper&quot;&quot;&quot;</span>
        <span class="k">if</span> <span class="ow">not</span> <span class="n">osp</span><span class="o">.</span><span class="n">exists</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">dataset_dir</span><span class="p">):</span>
            <span class="k">raise</span> <span class="ne">RuntimeError</span><span class="p">(</span><span class="s2">&quot;&#39;</span><span class="si">{}</span><span class="s2">&#39; is not available&quot;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">dataset_dir</span><span class="p">))</span>
        <span class="k">if</span> <span class="ow">not</span> <span class="n">osp</span><span class="o">.</span><span class="n">exists</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">val_dir</span><span class="p">):</span>
            <span class="k">raise</span> <span class="ne">RuntimeError</span><span class="p">(</span><span class="s2">&quot;&#39;</span><span class="si">{}</span><span class="s2">&#39; is not available&quot;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">val_dir</span><span class="p">))</span>
<span class="c1">#         if not osp.exists(self.train_dir):</span>
<span class="c1">#             raise RuntimeError(&quot;&#39;{}&#39; is not available&quot;.format(self.train_dir))</span>
        <span class="k">if</span> <span class="ow">not</span> <span class="n">osp</span><span class="o">.</span><span class="n">exists</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">val_anno</span><span class="p">):</span>
            <span class="k">raise</span> <span class="ne">RuntimeError</span><span class="p">(</span><span class="s2">&quot;&#39;</span><span class="si">{}</span><span class="s2">&#39; is not available&quot;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">val_anno</span><span class="p">))</span>
<span class="c1">#         if not osp.exists(self.train_anno):</span>
<span class="c1">#             raise RuntimeError(&quot;&#39;{}&#39; is not available&quot;.format(self.train_anno))</span>
    
    <span class="k">def</span> <span class="nf">_process_dir</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">path</span><span class="p">):</span>
        <span class="n">data_handle</span> <span class="o">=</span> <span class="n">coco</span><span class="o">.</span><span class="n">COCO</span><span class="p">(</span><span class="n">path</span><span class="p">)</span>
        <span class="n">image_ids</span> <span class="o">=</span> <span class="n">data_handle</span><span class="o">.</span><span class="n">getImgIds</span><span class="p">()</span>  
        <span class="n">images</span> <span class="o">=</span> <span class="p">[]</span>
        <span class="k">for</span> <span class="n">img_id</span> <span class="ow">in</span> <span class="n">image_ids</span><span class="p">:</span>
            <span class="n">idxs</span> <span class="o">=</span> <span class="n">data_handle</span><span class="o">.</span><span class="n">getAnnIds</span><span class="p">(</span><span class="n">imgIds</span><span class="o">=</span><span class="p">[</span><span class="n">img_id</span><span class="p">])</span>
            <span class="k">for</span> <span class="n">idx</span> <span class="ow">in</span> <span class="n">idxs</span><span class="p">:</span>
                <span class="n">images</span><span class="o">.</span><span class="n">append</span><span class="p">((</span><span class="n">img_id</span><span class="p">,</span> <span class="n">idx</span><span class="p">))</span>       
        <span class="n">num_samples</span> <span class="o">=</span> <span class="nb">len</span><span class="p">(</span><span class="n">images</span><span class="p">)</span>
        
        <span class="k">return</span> <span class="n">data_handle</span><span class="p">,</span> <span class="n">images</span><span class="p">,</span> <span class="n">num_samples</span>
        
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[46]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">class</span> <span class="nc">DeepFashion2KP</span><span class="p">(</span><span class="n">data</span><span class="o">.</span><span class="n">Dataset</span><span class="p">):</span>
    <span class="k">def</span> <span class="fm">__init__</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">data_handle</span><span class="p">,</span> <span class="n">data</span><span class="p">,</span> <span class="n">src</span><span class="p">,</span> <span class="n">split</span><span class="p">):</span>
        <span class="nb">super</span><span class="p">(</span><span class="n">DeepFashion2KP</span><span class="p">,</span> <span class="bp">self</span><span class="p">)</span><span class="o">.</span><span class="fm">__init__</span><span class="p">()</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">coco</span> <span class="o">=</span> <span class="n">data_handle</span>
        <span class="n">cats</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">coco</span><span class="o">.</span><span class="n">loadCats</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">coco</span><span class="o">.</span><span class="n">getCatIds</span><span class="p">())</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">num_classes</span> <span class="o">=</span> <span class="nb">len</span><span class="p">(</span><span class="n">cats</span><span class="p">)</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">num_joints</span> <span class="o">=</span> <span class="mi">294</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">max_object</span> <span class="o">=</span> <span class="mi">2</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">default_res</span> <span class="o">=</span> <span class="p">(</span><span class="mi">512</span><span class="p">,</span> <span class="mi">512</span><span class="p">)</span>    
        <span class="bp">self</span><span class="o">.</span><span class="n">images</span> <span class="o">=</span> <span class="n">data</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">src</span> <span class="o">=</span> <span class="n">src</span>
        <span class="bp">self</span><span class="o">.</span><span class="n">split</span> <span class="o">=</span> <span class="n">split</span>
        
    <span class="k">def</span> <span class="nf">_coco_box_to_bbox</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">box</span><span class="p">):</span>
        <span class="n">bbox</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([</span><span class="n">box</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="n">box</span><span class="p">[</span><span class="mi">1</span><span class="p">],</span> <span class="n">box</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">+</span> <span class="n">box</span><span class="p">[</span><span class="mi">2</span><span class="p">],</span> <span class="n">box</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">+</span> <span class="n">box</span><span class="p">[</span><span class="mi">3</span><span class="p">]],</span>
                        <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
        <span class="k">return</span> <span class="n">bbox</span>

    <span class="k">def</span> <span class="nf">_prerocessing</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">path</span><span class="p">):</span>
        <span class="n">img</span> <span class="o">=</span> <span class="n">cv2</span><span class="o">.</span><span class="n">imread</span><span class="p">(</span><span class="n">path</span><span class="p">)</span>
        <span class="n">height</span><span class="p">,</span> <span class="n">width</span> <span class="o">=</span> <span class="n">img</span><span class="o">.</span><span class="n">shape</span><span class="p">[:</span><span class="mi">2</span><span class="p">]</span>         
        <span class="n">long_side</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">max</span><span class="p">(</span><span class="n">img</span><span class="o">.</span><span class="n">shape</span><span class="p">[:</span><span class="mi">2</span><span class="p">])</span>
        <span class="n">canvas</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">([</span><span class="n">long_side</span><span class="p">,</span> <span class="n">long_side</span><span class="p">,</span> <span class="mi">3</span><span class="p">])</span>
        <span class="n">h_offset</span><span class="p">,</span> <span class="n">w_offset</span> <span class="o">=</span> <span class="nb">int</span><span class="p">((</span><span class="n">long_side</span><span class="o">-</span><span class="n">height</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span><span class="p">),</span> <span class="nb">int</span><span class="p">((</span><span class="n">long_side</span><span class="o">-</span><span class="n">width</span><span class="p">)</span><span class="o">/</span><span class="mi">2</span><span class="p">)</span>
        <span class="n">canvas</span><span class="p">[</span><span class="n">h_offset</span><span class="p">:(</span><span class="n">height</span><span class="o">+</span><span class="n">h_offset</span><span class="p">),</span> <span class="n">w_offset</span><span class="p">:(</span><span class="n">width</span><span class="o">+</span><span class="n">w_offset</span><span class="p">),</span> <span class="p">:]</span> <span class="o">=</span> <span class="n">img</span>
        <span class="n">img</span> <span class="o">=</span> <span class="n">canvas</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">uint8</span><span class="p">)</span>   
        <span class="n">scale</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">default_res</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">/</span> <span class="n">long_side</span>        
        <span class="n">img</span> <span class="o">=</span> <span class="n">cv2</span><span class="o">.</span><span class="n">resize</span><span class="p">(</span><span class="n">img</span><span class="p">,</span> <span class="bp">self</span><span class="o">.</span><span class="n">default_res</span><span class="p">)</span> 
        
        <span class="k">return</span> <span class="n">img</span><span class="p">,</span> <span class="n">w_offset</span><span class="p">,</span> <span class="n">h_offset</span><span class="p">,</span> <span class="n">scale</span>
    
    <span class="k">def</span> <span class="fm">__len__</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
        <span class="k">return</span> <span class="nb">len</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">images</span><span class="p">)</span>
        
    <span class="k">def</span> <span class="fm">__getitem__</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">index</span><span class="p">):</span>
        <span class="n">img_id</span><span class="p">,</span> <span class="n">ann_id</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">images</span><span class="p">[</span><span class="n">index</span><span class="p">]</span>
        <span class="n">fname</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">coco</span><span class="o">.</span><span class="n">loadImgs</span><span class="p">(</span><span class="n">ids</span><span class="o">=</span><span class="p">[</span><span class="n">img_id</span><span class="p">])[</span><span class="mi">0</span><span class="p">][</span><span class="s1">&#39;file_name&#39;</span><span class="p">]</span>
        <span class="n">img_path</span> <span class="o">=</span> <span class="n">osp</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">src</span><span class="p">,</span> <span class="n">fname</span><span class="p">)</span>
        <span class="n">anns</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">coco</span><span class="o">.</span><span class="n">loadAnns</span><span class="p">(</span><span class="n">ids</span><span class="o">=</span><span class="p">[</span><span class="n">ann_id</span><span class="p">])</span>
        <span class="n">num_objs</span> <span class="o">=</span> <span class="mi">1</span>
        

        <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">split</span> <span class="o">==</span> <span class="s1">&#39;train&#39;</span><span class="p">:</span>
            <span class="c1"># keep aspect ratio to resize to default resolution</span>
            <span class="n">img</span><span class="p">,</span> <span class="n">w_offset</span><span class="p">,</span> <span class="n">h_offset</span><span class="p">,</span> <span class="n">scale</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">_prerocessing</span><span class="p">(</span><span class="n">img_path</span><span class="p">)</span>
            <span class="n">height</span><span class="p">,</span> <span class="n">width</span> <span class="o">=</span> <span class="n">img</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="n">img</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span>
            <span class="n">c</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([</span><span class="n">img</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">/</span> <span class="mf">2.</span><span class="p">,</span> <span class="n">img</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">/</span> <span class="mf">2.</span><span class="p">],</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
            <span class="n">s</span> <span class="o">=</span> <span class="nb">max</span><span class="p">(</span><span class="n">img</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="n">img</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">1</span><span class="p">])</span> <span class="o">*</span> <span class="mf">1.0</span>
            <span class="n">sf</span> <span class="o">=</span> <span class="mf">0.4</span>
            <span class="n">cf</span> <span class="o">=</span> <span class="mf">0.1</span>
            <span class="n">c</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">=</span> <span class="n">c</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">+</span> <span class="n">s</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">clip</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">randn</span><span class="p">()</span><span class="o">*</span><span class="n">cf</span><span class="p">,</span> <span class="o">-</span><span class="mi">2</span><span class="o">*</span><span class="n">cf</span><span class="p">,</span> <span class="mi">2</span><span class="o">*</span><span class="n">cf</span><span class="p">)</span>
            <span class="n">c</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">=</span> <span class="n">c</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">+</span> <span class="n">s</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">clip</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">randn</span><span class="p">()</span><span class="o">*</span><span class="n">cf</span><span class="p">,</span> <span class="o">-</span><span class="mi">2</span><span class="o">*</span><span class="n">cf</span><span class="p">,</span> <span class="mi">2</span><span class="o">*</span><span class="n">cf</span><span class="p">)</span>
            <span class="n">s</span> <span class="o">=</span> <span class="n">s</span> <span class="o">*</span> <span class="n">np</span><span class="o">.</span><span class="n">clip</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">randn</span><span class="p">()</span><span class="o">*</span><span class="n">sf</span> <span class="o">+</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">1</span> <span class="o">-</span> <span class="n">sf</span><span class="p">,</span> <span class="mi">1</span> <span class="o">+</span> <span class="n">sf</span><span class="p">)</span>     

            <span class="n">trans_input</span> <span class="o">=</span> <span class="n">get_affine_transform</span><span class="p">(</span><span class="n">c</span><span class="p">,</span> <span class="n">s</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="bp">self</span><span class="o">.</span><span class="n">default_res</span><span class="p">)</span>
            <span class="n">inp</span> <span class="o">=</span> <span class="n">cv2</span><span class="o">.</span><span class="n">warpAffine</span><span class="p">(</span><span class="n">img</span><span class="p">,</span> <span class="n">trans_input</span><span class="p">,</span> <span class="bp">self</span><span class="o">.</span><span class="n">default_res</span><span class="p">,</span> <span class="n">flags</span><span class="o">=</span><span class="n">cv2</span><span class="o">.</span><span class="n">INTER_LINEAR</span><span class="p">)</span>
            <span class="n">img</span> <span class="o">=</span> <span class="n">inp</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
            <span class="c1"># [-1,1]</span>
            <span class="n">inp</span> <span class="o">=</span> <span class="p">(</span><span class="n">inp</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span> <span class="o">/</span> <span class="mf">255.</span><span class="p">)</span>
            <span class="n">inp</span> <span class="o">=</span> <span class="p">(</span><span class="n">inp</span> <span class="o">-</span> <span class="mf">0.5</span><span class="p">)</span> <span class="o">/</span> <span class="mf">0.5</span>
            <span class="c1"># HWC =&gt; CHW</span>
            <span class="n">inp</span> <span class="o">=</span> <span class="n">inp</span><span class="o">.</span><span class="n">transpose</span><span class="p">(</span><span class="mi">2</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="mi">1</span><span class="p">)</span>

            <span class="n">output_res</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">default_res</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">//</span> <span class="mi">4</span>
            <span class="n">num_joints</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">num_joints</span>
            <span class="n">num_classes</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">num_classes</span>
            <span class="n">trans_output</span> <span class="o">=</span> <span class="n">get_affine_transform</span><span class="p">(</span><span class="n">c</span><span class="p">,</span> <span class="n">s</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="p">[</span><span class="n">output_res</span><span class="p">,</span> <span class="n">output_res</span><span class="p">])</span>
            
            <span class="c1"># center, object heatmap</span>
            <span class="n">hm</span>             <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="n">num_classes</span><span class="p">,</span> <span class="n">output_res</span><span class="p">,</span> <span class="n">output_res</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
            <span class="c1"># size</span>
            <span class="n">wh</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="n">num_objs</span><span class="p">,</span> <span class="mi">2</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
            <span class="c1"># offset</span>
            <span class="n">reg</span>            <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="n">num_objs</span><span class="p">,</span> <span class="mi">2</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
            <span class="n">reg_mask</span>       <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="n">num_objs</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">uint8</span><span class="p">)</span>
            
            <span class="n">ind</span>            <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="n">num_objs</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">int64</span><span class="p">)</span>
            
            <span class="c1"># human pose heatmap</span>
            <span class="n">hm_hp</span>          <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="n">num_joints</span> <span class="p">,</span> <span class="n">output_res</span><span class="p">,</span> <span class="n">output_res</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>    
            <span class="c1"># humna pose offset</span>
            <span class="n">hp_offset</span>      <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="n">num_objs</span> <span class="o">*</span> <span class="n">num_joints</span><span class="p">,</span> <span class="mi">2</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
            <span class="c1"># human pose location relative to center</span>
            <span class="n">kps</span>            <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="n">num_objs</span><span class="p">,</span> <span class="n">num_joints</span> <span class="o">*</span> <span class="mi">2</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
            <span class="n">kps_mask</span>       <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="n">num_objs</span><span class="p">,</span> <span class="n">num_joints</span> <span class="o">*</span> <span class="mi">2</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">uint8</span><span class="p">)</span>
            
            <span class="n">hp_ind</span>         <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="n">num_objs</span> <span class="o">*</span> <span class="n">num_joints</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">int64</span><span class="p">)</span>
            <span class="n">hp_mask</span>        <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">zeros</span><span class="p">((</span><span class="n">num_objs</span> <span class="o">*</span> <span class="n">num_joints</span><span class="p">),</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">int64</span><span class="p">)</span>            
            
            
            <span class="n">draw_gaussian</span> <span class="o">=</span> <span class="n">draw_umich_gaussian</span>

            <span class="n">gt_det</span> <span class="o">=</span> <span class="p">[]</span>
            <span class="k">for</span> <span class="n">k</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">num_objs</span><span class="p">):</span>
                <span class="n">ann</span> <span class="o">=</span> <span class="n">anns</span><span class="p">[</span><span class="n">k</span><span class="p">]</span>
                <span class="n">bbox</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">_coco_box_to_bbox</span><span class="p">(</span><span class="n">ann</span><span class="p">[</span><span class="s1">&#39;bbox&#39;</span><span class="p">])</span>
                <span class="n">bbox</span><span class="p">[[</span><span class="mi">0</span><span class="p">,</span> <span class="mi">2</span><span class="p">]]</span> <span class="o">+=</span> <span class="n">w_offset</span>
                <span class="n">bbox</span><span class="p">[[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">3</span><span class="p">]]</span> <span class="o">+=</span> <span class="n">h_offset</span>
                <span class="n">bbox</span> <span class="o">*=</span> <span class="n">scale</span>

                <span class="n">cls_id</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">ann</span><span class="p">[</span><span class="s1">&#39;category_id&#39;</span><span class="p">])</span> <span class="o">-</span> <span class="mi">1</span>
                <span class="n">pts</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span><span class="n">ann</span><span class="p">[</span><span class="s1">&#39;keypoints&#39;</span><span class="p">],</span> <span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span><span class="o">.</span><span class="n">reshape</span><span class="p">(</span><span class="n">num_joints</span><span class="p">,</span> <span class="mi">3</span><span class="p">)</span>
                <span class="n">pts</span><span class="p">[:,</span><span class="mi">0</span><span class="p">]</span> <span class="o">+=</span> <span class="n">w_offset</span>
                <span class="n">pts</span><span class="p">[:,</span><span class="mi">1</span><span class="p">]</span> <span class="o">+=</span> <span class="n">h_offset</span>
                <span class="n">pts</span><span class="p">[:,:</span><span class="mi">2</span><span class="p">]</span> <span class="o">*=</span> <span class="n">scale</span>

                <span class="n">bbox</span><span class="p">[:</span><span class="mi">2</span><span class="p">]</span> <span class="o">=</span> <span class="n">affine_transform</span><span class="p">(</span><span class="n">bbox</span><span class="p">[:</span><span class="mi">2</span><span class="p">],</span> <span class="n">trans_output</span><span class="p">)</span>
                <span class="n">bbox</span><span class="p">[</span><span class="mi">2</span><span class="p">:]</span> <span class="o">=</span> <span class="n">affine_transform</span><span class="p">(</span><span class="n">bbox</span><span class="p">[</span><span class="mi">2</span><span class="p">:],</span> <span class="n">trans_output</span><span class="p">)</span>
                <span class="n">bbox</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">clip</span><span class="p">(</span><span class="n">bbox</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="n">output_res</span> <span class="o">-</span> <span class="mi">1</span><span class="p">)</span>
                <span class="n">h</span><span class="p">,</span> <span class="n">w</span> <span class="o">=</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">3</span><span class="p">]</span> <span class="o">-</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">1</span><span class="p">],</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span> <span class="o">-</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
                
                <span class="k">if</span> <span class="n">h</span> <span class="o">&gt;</span> <span class="mi">0</span> <span class="ow">and</span> <span class="n">w</span> <span class="o">&gt;</span> <span class="mi">0</span><span class="p">:</span>
                    <span class="n">radius</span> <span class="o">=</span> <span class="n">gaussian_radius</span><span class="p">((</span><span class="n">math</span><span class="o">.</span><span class="n">ceil</span><span class="p">(</span><span class="n">h</span><span class="p">),</span> <span class="n">math</span><span class="o">.</span><span class="n">ceil</span><span class="p">(</span><span class="n">w</span><span class="p">)))</span>
                    <span class="n">radius</span> <span class="o">=</span> <span class="nb">max</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="nb">int</span><span class="p">(</span><span class="n">radius</span><span class="p">))</span>
                    <span class="n">ct</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([(</span><span class="n">bbox</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">+</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">2</span><span class="p">])</span> <span class="o">/</span> <span class="mi">2</span><span class="p">,</span> <span class="p">(</span><span class="n">bbox</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">+</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">3</span><span class="p">])</span> <span class="o">/</span> <span class="mi">2</span><span class="p">],</span> <span class="n">dtype</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span>
                    <span class="n">ct_int</span> <span class="o">=</span> <span class="n">ct</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">int32</span><span class="p">)</span>
                    <span class="n">wh</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="mf">1.</span> <span class="o">*</span> <span class="n">w</span><span class="p">,</span> <span class="mf">1.</span> <span class="o">*</span> <span class="n">h</span>
                    <span class="n">ind</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="n">ct_int</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">*</span> <span class="n">output_res</span> <span class="o">+</span> <span class="n">ct_int</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
                    <span class="n">reg</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="n">ct</span> <span class="o">-</span> <span class="n">ct_int</span>
                    <span class="n">reg_mask</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="mi">1</span>
                    <span class="n">num_kpts</span> <span class="o">=</span> <span class="n">pts</span><span class="p">[:,</span> <span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>
                    <span class="k">if</span> <span class="n">num_kpts</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
                        <span class="n">hm</span><span class="p">[</span><span class="n">cls_id</span><span class="p">,</span> <span class="n">ct_int</span><span class="p">[</span><span class="mi">1</span><span class="p">],</span> <span class="n">ct_int</span><span class="p">[</span><span class="mi">0</span><span class="p">]]</span> <span class="o">=</span> <span class="mf">0.9999</span>
                        <span class="n">reg_mask</span><span class="p">[</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="mi">0</span>

                    <span class="n">hp_radius</span> <span class="o">=</span> <span class="n">gaussian_radius</span><span class="p">((</span><span class="n">math</span><span class="o">.</span><span class="n">ceil</span><span class="p">(</span><span class="n">h</span><span class="p">),</span> <span class="n">math</span><span class="o">.</span><span class="n">ceil</span><span class="p">(</span><span class="n">w</span><span class="p">)))</span>
                    <span class="n">hp_radius</span> <span class="o">=</span> <span class="nb">max</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="nb">int</span><span class="p">(</span><span class="n">hp_radius</span><span class="p">))</span> 
                    <span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="n">num_joints</span><span class="p">):</span>
                        <span class="k">if</span> <span class="n">pts</span><span class="p">[</span><span class="n">j</span><span class="p">,</span> <span class="mi">2</span><span class="p">]</span> <span class="o">&gt;</span> <span class="mi">0</span><span class="p">:</span>
                            <span class="n">pts</span><span class="p">[</span><span class="n">j</span><span class="p">,</span> <span class="p">:</span><span class="mi">2</span><span class="p">]</span> <span class="o">=</span> <span class="n">affine_transform</span><span class="p">(</span><span class="n">pts</span><span class="p">[</span><span class="n">j</span><span class="p">,</span> <span class="p">:</span><span class="mi">2</span><span class="p">],</span> <span class="n">trans_output</span><span class="p">)</span>
                            <span class="k">if</span> <span class="n">pts</span><span class="p">[</span><span class="n">j</span><span class="p">,</span> <span class="mi">0</span><span class="p">]</span> <span class="o">&gt;=</span> <span class="mi">0</span> <span class="ow">and</span> <span class="n">pts</span><span class="p">[</span><span class="n">j</span><span class="p">,</span> <span class="mi">0</span><span class="p">]</span> <span class="o">&lt;</span> <span class="n">output_res</span> <span class="ow">and</span> <span class="n">pts</span><span class="p">[</span><span class="n">j</span><span class="p">,</span> <span class="mi">1</span><span class="p">]</span> <span class="o">&gt;=</span> <span class="mi">0</span> <span class="ow">and</span> <span class="n">pts</span><span class="p">[</span><span class="n">j</span><span class="p">,</span> <span class="mi">1</span><span class="p">]</span> <span class="o">&lt;</span> <span class="n">output_res</span><span class="p">:</span>
                                <span class="n">kps</span><span class="p">[</span><span class="n">k</span><span class="p">,</span> <span class="n">j</span> <span class="o">*</span> <span class="mi">2</span><span class="p">:</span> <span class="n">j</span> <span class="o">*</span> <span class="mi">2</span> <span class="o">+</span> <span class="mi">2</span><span class="p">]</span> <span class="o">=</span> <span class="n">pts</span><span class="p">[</span><span class="n">j</span><span class="p">,</span> <span class="p">:</span><span class="mi">2</span><span class="p">]</span> <span class="o">-</span> <span class="n">ct_int</span>
                                <span class="n">kps_mask</span><span class="p">[</span><span class="n">k</span><span class="p">,</span> <span class="n">j</span> <span class="o">*</span> <span class="mi">2</span><span class="p">:</span> <span class="n">j</span> <span class="o">*</span> <span class="mi">2</span> <span class="o">+</span> <span class="mi">2</span><span class="p">]</span> <span class="o">=</span> <span class="mi">1</span>
                                <span class="n">pt_int</span> <span class="o">=</span> <span class="n">pts</span><span class="p">[</span><span class="n">j</span><span class="p">,</span> <span class="p">:</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">int32</span><span class="p">)</span>
                                <span class="n">hp_offset</span><span class="p">[</span><span class="n">k</span> <span class="o">*</span> <span class="n">num_joints</span> <span class="o">+</span> <span class="n">j</span><span class="p">]</span> <span class="o">=</span> <span class="n">pts</span><span class="p">[</span><span class="n">j</span><span class="p">,</span> <span class="p">:</span><span class="mi">2</span><span class="p">]</span> <span class="o">-</span> <span class="n">pt_int</span>
                                <span class="n">hp_ind</span><span class="p">[</span><span class="n">k</span> <span class="o">*</span> <span class="n">num_joints</span> <span class="o">+</span> <span class="n">j</span><span class="p">]</span> <span class="o">=</span> <span class="n">pt_int</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">*</span> <span class="n">output_res</span> <span class="o">+</span> <span class="n">pt_int</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
                                <span class="n">hp_mask</span><span class="p">[</span><span class="n">k</span> <span class="o">*</span> <span class="n">num_joints</span> <span class="o">+</span> <span class="n">j</span><span class="p">]</span> <span class="o">=</span> <span class="mi">1</span>
                                <span class="n">draw_gaussian</span><span class="p">(</span><span class="n">hm_hp</span><span class="p">[</span><span class="n">j</span><span class="p">],</span> <span class="n">pt_int</span><span class="p">,</span> <span class="n">hp_radius</span><span class="p">)</span>
                    <span class="n">draw_gaussian</span><span class="p">(</span><span class="n">hm</span><span class="p">[</span><span class="n">cls_id</span><span class="p">],</span> <span class="n">ct_int</span><span class="p">,</span> <span class="n">radius</span><span class="p">)</span>
                    
            
            <span class="n">ret</span> <span class="o">=</span> <span class="p">{</span>   <span class="s1">&#39;input&#39;</span><span class="p">:</span> <span class="n">inp</span><span class="p">,</span>         <span class="s1">&#39;img&#39;</span><span class="p">:</span> <span class="n">img</span><span class="p">,</span>       <span class="s1">&#39;bbox&#39;</span><span class="p">:</span> <span class="n">bbox</span><span class="p">,</span>     <span class="s1">&#39;pts&#39;</span><span class="p">:</span><span class="n">pts</span><span class="p">,</span> <span class="s1">&#39;cls&#39;</span><span class="p">:</span><span class="n">cls_id</span><span class="p">,</span>
                         <span class="s1">&#39;hm&#39;</span><span class="p">:</span> <span class="n">hm</span><span class="p">,</span>           <span class="s1">&#39;wh&#39;</span><span class="p">:</span> <span class="n">wh</span><span class="p">,</span>         <span class="s1">&#39;reg&#39;</span><span class="p">:</span> <span class="n">reg</span><span class="p">,</span>
                   <span class="s1">&#39;reg_mask&#39;</span><span class="p">:</span> <span class="n">reg_mask</span><span class="p">,</span>    <span class="s1">&#39;ind&#39;</span><span class="p">:</span> <span class="n">ind</span><span class="p">,</span>
                      <span class="s1">&#39;hm_hp&#39;</span><span class="p">:</span> <span class="n">hm_hp</span><span class="p">,</span>       <span class="s1">&#39;hps&#39;</span><span class="p">:</span> <span class="n">kps</span><span class="p">,</span>  <span class="s1">&#39;hp_offset&#39;</span><span class="p">:</span> <span class="n">hp_offset</span><span class="p">,</span>
                   <span class="s1">&#39;hps_mask&#39;</span><span class="p">:</span> <span class="n">kps_mask</span><span class="p">,</span> <span class="s1">&#39;hp_ind&#39;</span><span class="p">:</span> <span class="n">hp_ind</span><span class="p">,</span> <span class="s1">&#39;hp_mask&#39;</span><span class="p">:</span> <span class="n">hp_mask</span><span class="p">}</span>
        <span class="k">else</span><span class="p">:</span>
            <span class="n">img</span> <span class="o">=</span> <span class="n">cv2</span><span class="o">.</span><span class="n">imread</span><span class="p">(</span><span class="n">img_path</span><span class="p">)</span>
            <span class="c1"># [-1,1]</span>
            <span class="n">inp</span> <span class="o">=</span> <span class="p">(</span><span class="n">inp</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">float32</span><span class="p">)</span> <span class="o">/</span> <span class="mf">255.</span><span class="p">)</span>
            <span class="n">inp</span> <span class="o">=</span> <span class="p">(</span><span class="n">inp</span> <span class="o">-</span> <span class="mf">0.5</span><span class="p">)</span> <span class="o">/</span> <span class="mf">0.5</span>
            <span class="c1"># HWC =&gt; CHW</span>
            <span class="n">inp</span> <span class="o">=</span> <span class="n">inp</span><span class="o">.</span><span class="n">transpose</span><span class="p">(</span><span class="mi">2</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="mi">1</span><span class="p">)</span>

        <span class="k">return</span> <span class="n">ret</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">deepfashion</span> <span class="o">=</span> <span class="n">DeepFashion2</span><span class="p">(</span><span class="n">cfg</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_text output_error">
<pre>
<span class="ansi-red-fg">---------------------------------------------------------------------------</span>
<span class="ansi-red-fg">KeyError</span>                                  Traceback (most recent call last)
<span class="ansi-green-fg">&lt;ipython-input-3-21ff75c0410c&gt;</span> in <span class="ansi-cyan-fg">&lt;module&gt;</span>
<span class="ansi-green-fg">----&gt; 1</span><span class="ansi-red-fg"> </span>deepfashion <span class="ansi-blue-fg">=</span> data_manager<span class="ansi-blue-fg">.</span>init_img_dataset<span class="ansi-blue-fg">(</span>cfg<span class="ansi-blue-fg">)</span>

<span class="ansi-green-fg">/media/allen/mass/deep-learning-works/data/data_manager.py</span> in <span class="ansi-cyan-fg">init_img_dataset</span><span class="ansi-blue-fg">(cfg)</span>
<span class="ansi-green-intense-fg ansi-bold">   1547</span>     name <span class="ansi-blue-fg">=</span> cfg<span class="ansi-blue-fg">.</span>DATASET<span class="ansi-blue-fg">.</span>NAME
<span class="ansi-green-intense-fg ansi-bold">   1548</span>     <span class="ansi-green-fg">if</span> name <span class="ansi-green-fg">not</span> <span class="ansi-green-fg">in</span> __img_factory<span class="ansi-blue-fg">.</span>keys<span class="ansi-blue-fg">(</span><span class="ansi-blue-fg">)</span><span class="ansi-blue-fg">:</span>
<span class="ansi-green-fg">-&gt; 1549</span><span class="ansi-red-fg">         </span><span class="ansi-green-fg">raise</span> KeyError<span class="ansi-blue-fg">(</span><span class="ansi-blue-fg">&#34;Invalid dataset, got &#39;{}&#39;, but expected to be one of {}&#34;</span><span class="ansi-blue-fg">.</span>format<span class="ansi-blue-fg">(</span>name<span class="ansi-blue-fg">,</span> __img_factory<span class="ansi-blue-fg">.</span>keys<span class="ansi-blue-fg">(</span><span class="ansi-blue-fg">)</span><span class="ansi-blue-fg">)</span><span class="ansi-blue-fg">)</span>
<span class="ansi-green-intense-fg ansi-bold">   1550</span>     dataset <span class="ansi-blue-fg">=</span> __img_factory<span class="ansi-blue-fg">[</span>name<span class="ansi-blue-fg">]</span><span class="ansi-blue-fg">(</span>cfg<span class="ansi-blue-fg">)</span>
<span class="ansi-green-intense-fg ansi-bold">   1551</span>     <span class="ansi-green-fg">return</span> dataset

<span class="ansi-red-fg">KeyError</span>: &#34;Invalid dataset, got &#39;deepfashion&#39;, but expected to be one of dict_keys([&#39;imagenet&#39;, &#39;market1501&#39;, &#39;market1501_partial&#39;, &#39;cuhk03&#39;, &#39;cuhk02&#39;, &#39;cuhk01&#39;, &#39;dukemtmcreid&#39;, &#39;msmt17&#39;, &#39;msmt17_total&#39;, &#39;par&#39;, &#39;sogo&#39;, &#39;deepfastion&#39;])&#34;</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[47]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">dataset</span> <span class="o">=</span> <span class="n">DeepFashion2KP</span><span class="p">(</span><span class="n">deepfashion</span><span class="o">.</span><span class="n">val_handle</span><span class="p">,</span> <span class="n">deepfashion</span><span class="o">.</span><span class="n">val_images</span><span class="p">,</span> <span class="n">src</span><span class="o">=</span><span class="n">deepfashion</span><span class="o">.</span><span class="n">val_dir</span><span class="p">,</span> <span class="n">split</span><span class="o">=</span><span class="s1">&#39;train&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[50]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">batch</span><span class="o">.</span><span class="n">keys</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[50]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>dict_keys([&#39;input&#39;, &#39;img&#39;, &#39;bbox&#39;, &#39;pts&#39;, &#39;cls&#39;, &#39;hm&#39;, &#39;wh&#39;, &#39;reg&#39;, &#39;reg_mask&#39;, &#39;ind&#39;, &#39;hm_hp&#39;, &#39;hps&#39;, &#39;hp_offset&#39;, &#39;hps_mask&#39;, &#39;hp_ind&#39;, &#39;hp_mask&#39;])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[17]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">batch</span><span class="p">[</span><span class="s1">&#39;hm&#39;</span><span class="p">][</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">numpy</span><span class="p">()</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[17]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(13, 128, 128)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[69]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">batch</span><span class="p">[</span><span class="s1">&#39;hm_hp&#39;</span><span class="p">][</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">sum</span><span class="p">(</span><span class="n">dim</span><span class="o">=</span><span class="mi">0</span><span class="p">)</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[69]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>torch.Size([128, 128])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[74]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">_hm</span> <span class="o">=</span> <span class="p">(</span><span class="n">batch</span><span class="p">[</span><span class="s1">&#39;hm_hp&#39;</span><span class="p">][</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">sum</span><span class="p">(</span><span class="n">dim</span><span class="o">=</span><span class="mi">0</span><span class="p">)</span><span class="o">.</span><span class="n">numpy</span><span class="p">()</span> <span class="o">*</span> <span class="mi">255</span><span class="p">)</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">uint8</span><span class="p">)</span>
<span class="n">to_pil</span><span class="p">(</span><span class="n">_hm</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[74]:</div>




<div class="output_png output_subarea output_execute_result">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[75]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">img</span> <span class="o">=</span> <span class="n">batch</span><span class="p">[</span><span class="s1">&#39;img&#39;</span><span class="p">][</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">numpy</span><span class="p">()</span>
<span class="n">scale_img</span> <span class="o">=</span> <span class="n">cv2</span><span class="o">.</span><span class="n">resize</span><span class="p">(</span><span class="n">img</span><span class="p">,</span> <span class="p">(</span><span class="mi">128</span><span class="p">,</span><span class="mi">128</span><span class="p">))</span>
<span class="n">bbox</span> <span class="o">=</span> <span class="p">[</span><span class="nb">int</span><span class="p">(</span><span class="n">i</span><span class="p">)</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">map</span><span class="p">(</span><span class="nb">int</span><span class="p">,</span> <span class="n">batch</span><span class="p">[</span><span class="s1">&#39;bbox&#39;</span><span class="p">][</span><span class="mi">7</span><span class="p">]</span><span class="o">.</span><span class="n">numpy</span><span class="p">())]</span>
<span class="n">temp</span> <span class="o">=</span> <span class="n">cv2</span><span class="o">.</span><span class="n">rectangle</span><span class="p">(</span><span class="n">scale_img</span><span class="p">,</span> <span class="p">(</span><span class="n">bbox</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">1</span><span class="p">]),</span> <span class="p">(</span><span class="n">bbox</span><span class="p">[</span><span class="mi">2</span><span class="p">],</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">3</span><span class="p">]),</span> <span class="p">(</span><span class="mi">255</span><span class="p">,</span><span class="mi">255</span><span class="p">,</span><span class="mi">255</span><span class="p">),</span> <span class="mi">1</span><span class="p">)</span>
<span class="n">to_pil</span><span class="p">(</span><span class="n">temp</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[75]:</div>




<div class="output_png output_subarea output_execute_result">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAIAAAACACAIAAABMXPacAABiD0lEQVR4nOz9Z6xnW3YfiK21djjhH2+sXK9eDh3Yzdwim6JESqIomiMqQvbA8IwFWPPBXwQbhj1jYATYMAYG7PHYHsmGxmk0kscciTIlSpRESszNbnYOL79Xuermfzpph7WWP9x61a8DB7J0NfYHLvzr1v2fu885++zf3muvfAD+gP6A/oD+gP6A/oD+gP5/QviHfujTSRlJrMFr15+p65ExhEiIgIAIIKCKCACgSmhUVVUAFUUBkYiYsyFU1SQchlyNy5yTJLCgSdnUxd2791+99YKxBgGJCM6vBgr6pBOiih/uE6KIIKIqIAECqiqen4UIAB9uDE++4zd//fBxhfN/8OT8J6TfckA//L9+9ws9+dNv/eZvfOH3fu9famj/5cj+D/77/15EzjLcuLJ/4/mXfeENGUQkRAJEhQwKhEikqsBAhKIZQQiNMBtjWKSwLsa4Cf3ibHXpxv5qvcBoL+9u3T941MZhsVz+4R/4USKq6/p8KBBRVQHg/KeIPHlCVSL6YPTPf1dEoPO7f3Du+Zjgtw0SfgcuT47IdzZQRSL64Ns37/7NBoQfOvK0JfwH//7/9IIBGM9qtGY8HV2/fBmcIyREBEQFYGZLhgjhg8cmAwCAoAAKTwfL2KyojJDBG4KsedBZ7dep39+58vnPfOaVV1/w3osIIuD59T944KcD/cFXQERjzDkGiGjMt3T3m0gAIuL5IiIk+G6EiACKSOcAfxgA/G6nfAtCHzqiCvrBKvh2kP+1yVaTqt6ab21vIxgy9GQsRJCIDKkonbMHFgAAFQVBEEBRMOcAAKlojrnLqS8crM7WjnzXrEuogUanh4u9P7R9Pqzf9tjn92Lm80dV1afwPIXk6Yg/nbDfXAQfwPBt13yK69ODHz7lX4EQUUXO0aCLhsBu7+3NtrYQgIiMGhAgMorCymitAAM9uSURoSiCYQECi+pQlVBUJSZFLC2H6dbuwdkpkFrjVO1qfXzpxiU7mTJzWZbnD/NhJvO0H09H7XykPph6CgDGGBXFD/GE79rsHCCRDABERvWbs/47G5+znQ9Q+fDxJ0Qf+iYo5/MBABS/pdm/PtF8a8saY4whQ2SQDCIpqHggJ+iAnIAT8ECUn/BKgvNZJqoiopwTQk55iLlXVLJms9k46w4ODqwzN2/eJOvOVwARfedkpG+lp8fPoXrK8T/c+PxPTxv/1/z+rzPx/5shMsbA+VxQUOXzD9GTWYEfPIaK4AeLUUERETABMpGxxiozIYClYQiGjLEmhLC/v/9bv/XbO7u7MYRvMo0PpvlT+s4+nY+vqn54o/7w9vukSx9c5+lZ5wfP6ekK+7Yb/X63/q7NLny4v5MsnQt655xX5fyBFTEj0PmeaYiZAQkBUFhUjTGqioZBDAAgWOCcEpf1dAhBUeuqDl2P3j//3HNlUVhrc87/Mr15yvqffv0uI3W+HH4fTvBtV/j/fyLSJ2I209NDZMhYMgiAAChiESwoqXxIRCHUSoGNZdGswKzBV0WQqCCGLLnyi1/5WkgdkVq0RVH0fX/O+p/e+ylr/tZ9Fc7FX/NEUJTzD6Kef54cecKXv3n8wyvgQ9dEBEHMCEoKiiAIRgE/YPznqxw/JN585zoghaefi94CgIQAiAyiBUIkYxwiqX6zH09F9W/n3R9ILCJPGhBRUTgySARF6XPT3bh2oxjV4oxzrizLpmmeivzfds3vuuS/86bwrXvDvwSXQEbDQIwGgBRIkDISIzCCGgLz3UXY/8bIKiISgYIBED0fenO+wj8YFFWVc7ajqh/I1CAqoOcyOIuIqrZtiwSSEnMqi3q+s7W3v2+QzrdMAJhOp6rStn1ZlufjeN6JJ+Lsh+jJ+MKTSX3e4KlI+l05zHeFCkElx6ZZrdd9d3S6c2XfVEXhfDka07kyoOeTDeBDm8233eLplVXhwhUBe37Fc71XEQBRRD9Yzef9UAQ87xsJZRQV+Lt/9xc//tILr370JVViTipSFj5xMsZU1Wi9Xm+aja/L0XiCCqUhQlRQMpQCl1WVVdabtXXeO2uNNYAGAc+fEBBQAZ4Oy7cqUN86wOcnnNsn5MnJT0lyzs16mZq1IeWmC4vj47iZX70UFPKw1bbtdDrr+85XlfdFUXg0BhA/tLucmzLOf8p31d0uAABzvrue20wMAJ6bX0CYPxA2EODJoxqQSP7Lv/3FX/mV3/yzf/yPGnCihjXEONTTUb9ZgpaASs4fHJ9d29uyxgOKMYLn4KoaS10YvvHu200Y+n5QQEUznc1efuba9njLASGCaAZEACWgpxMBP6QlPEVFvwOVJwyTjObh5PHDunRVYbgbMIem7Uqjdrkcl9No2uXJYQrrvusrVyNiXVV9irb0l67cQOsQnvBhBVUVpARqQe3FAwAAdP4woqTnq/aJBeuDB0ZEJMTMvKburbeW/+f/5P/0v/3r//NiOhYFAMgimzgUUAOBYkhiFdym6T7+0i04B/RD8jiSIuSPv/KiGiqI2pAXXfzGW+/93utfHVXjH/ro91ZKT8cXPpBEfz/68OI455DnbCqrLI9OpA9AuG7WBRABRBUjvF4ujlcHYP2tZ6+PqnJWlha9qjJLWdqo6fT4kbXeuiLGWFVl1w+KNJ1VRYGA5r+mM//qAAA8WfGEBPqENZ5rloj4hCMgqup77xz9L/7af/if/C//2vaVy6xowOQsqjKuR916bUUBFRSNqtVhPB7jE0CfGHlUlcCMygkIKCiojgtfuHLnkx+/8+juV95757c+/9kf+94f8PgBO/59xvr3I1XNOccYw5C6TVM5s2kbw2KsRdWbl6+8ffddW/n9rcvz3XFZl6xWRISSMQYNkoGRKwtykjjHDpkteh7agSUMy7Kst3ev/n7i7786APZcxycAgIz6RNJCBQME58INCiLknHP86//R//o/+g///ZsvP4NqsjAiM0dNQ10Uy64nBBHD3IXQXN6piqJGUusskvmAW5ybgUlREVEoq4olcs587PpLN64++89/91d/9XP/bFptf8/LnxhXpXnChBW+lTF/CAw8X6kiKipRYhrC5uxsdXJqWYstPx4XY5reu3uv60NKOp1fvvrc3qieee9FIGdFg6awAJAzs3Qo2Gf2jkwC54r12dIoVKWdjOqQBOjiN2H69lmG50Lxh2zl50eICu//+n/6H7/y0ktkrEVDikTImtrQReEgeRDOFBnz4fHR3t416xwLExEAAgHQuSHlfINVAEUxpEQKiBowPj550HLb2nDKy2/cfWOxWazXjah8e5e/1WYpoiySYuy7drlcni2ON+uzIW+G3Bvjlcwy9eNLe9s3rm7duvZ7b7zexM4ZqyBZknXiKyKDCqLAaByry1AEIXQuixRVRd5ZZyVDNwwM39GZf30A4Juq0BO1k4gUFOCJ4qVZSQFYVERLT9aAqoI6YxUgMSfhuw8eZNA2DEkCGIgJtrevAYBzjohA1QACCyk8NTAgIioRqmonshz49Gx9d743KasanR63B4xxOp2s1xv8Nno6VwBURERSTDHlvm02q7PYdzkEVBm42zRt3+fsEGtfzMZuVKqh0XhCRATZExvMFrO3MqrM9qze2prP57vvvvPeb/3W76A16kxCZUJblIywansVunAV+8ke8IH93RCgihIaBkBUBDKYUQERhTV5dIAWUBCtYuYUORdlWbehRENoDPkQYlFVReXPr8zMyhyXPYASEZUlefcEfJIY1wJrojRS/Oity289OO4HjJQ7l996/97+91x2zn3Xfp9rJKKQc44xhTB07Sb2XU5pWK9O7p9O94po7OrgUUAejaaz6VaKucjgjWEVEjLGESEqccLISThkiU3TP7zz7t7+fMixqmpAYOaUOQxxd29f/w1Yh6yKIBIBEpJmQSJAUFWDSMaoKikBKFkrCgUbQFQiS4YhpCCawqiYneGpgyhsuOuHvtvf2fHOSY5d2wnh+u37x196a+5dPzFXXnyu3t/DnRmpQWdym4vSBh9QYL0Ik7685vd8UT5y67cfPejDcM5mABX1m2L4E76vylmYOXFoh01sKQHlFPMmm2nhxbmqLPe2UG1Kucvh8EFbl35oGra9gcI6pyrOem9L650rTEXV2/cfDmV55dZLJLRZrHLqrSVbjcpRhVQSElw0BhbRIJ3rX/IB68ffx+ShhEpESCCaATBzjpzBMigOQ55PJqdNv1yvn33meUQ6W5+1x4u6rg5ff6de93prUoyK5Xv3vvw7v/uJn/qjWFWuqqyW6zM6XWw2JwuqR1W5B36GJht01pqjk6Nr+5e/676nqqIiqjlzjjH2Q9JEkCWFoqYMxbQa95sWQihGpTXoSjfEvi79yBTOO2vKc26LAGRVNOQEcdOtjs5MThUhgcymU+ZZyrkZlqphe2fygWZ6oQCAebKzCKj9wP197pB/erNzBkV0rhGzChAhAWTmQXLXbAwVYRgyD1HTemins9l6uXr//vs3dy4tm9X8+m6/M+qv7tqy3PHljWcvneZY2ZEujo7P2hTBA4Q+XL68B5DQDt5WV8Z762F9cnT87PUb8PttfQqZmTlzSJRZJKY+USKALO2mA7XGDiGycj2yhk3rpNyd1NtzU9bn+52qoqrPmlUE9O7jxx/7yGu/++UvTsbeEca+O12tbVnWozqmJ8aYbzOZXAAACqqAAIrGGPjAJvMdk46ZPzDefOAKFhhirOrR40eLmlwK6ejooHdgnAtxOH18PKqrVbeRgorru7W3s6JebrownWbFCtzpe0erlr70+rsPHt95+ebVn/pjP12PC8PRkJosGPH5y9ePhoMnHugPvDLnlgdQVQURFRHmnEKEJMpk2ImkmHWMVHg73d33bqSSUtqsV/3RvQfXZ+PVuw+wri2hsYYQjXOD8Uom5eSLilGn29NiXJhETLkcIboYgx6dLGbz/TgM/5J29f8vAEAGRCEyoCDIaPCJM++puxXRkOUYEQHJqqoCElEech4iJC6ZgKPLLGT4uJm6+vT4aLM4LtLI1dMKi6wUGjZ9ZE6bo1NvHUoeQfUPfuMfhdWmWTbHJ3b052y/6vfn82ri+jhwCCOpxvWYQAUIgEXPlQcEBBXJApIIkwpnBmYjEHHglSmk7dlmUzIc3z9g5nZzMi5rwRI1FaNq07elDoOoMUYBQt8X6LtUvHP3rY9/9Lk3v3K/3PbDonVV7UejqSv61XrVL3Yv7Q1piG13dnxw0QCcM5cnlnT8QNHBDy/8D1gQqcp5AwUdeAiSjIAxpgth3WbWYOvi0qXLibGYbs/tJHc5mpwMMqeTs6YoCj+dBdYo8tU33gpx+ekf+cHTVb775Xu0aQpUMUMCtJaIfCbZubw75EBgJFOGts0Fad6qmaRQZcHMkHPOzJxSEmFjKOe0tT0tIrzz7hvz+bYaospQ6X0x3eRu68rW/s6+w6JzARBzzi6PTYS3v/bmS68+DyUtFqfPTLYfv/2mcyMuDBNuTed1vc1Kw9C9+e43lt36ogGgc5u+WGv1myrnt1h9P2QuPm/MANCmbkhhc7rSDKdnp1/53Ft9XP/5/+6/tT5ZQNL9a9fOdD1zde6VSZD7a5evDszgyr4bvvDFL335S2//+Z/9ye3x5G739rt61PTD9v6MrFlvemQty7IP8fc+93tXLu/cf/vxb//zr0bsluUAafj+Wy/92E/8+M1XnhOQlFOMkZkRgGVApBRj05zaXnd3t6pqVNYT56kunKCViFvzLTtxaMopWGssAObMX/zS1/Zv7l2/cWU9dJlpZ3uvsi71vOk2xph1ziWQc7OHB0fvvXewWocLBsCYJ4Mrwgjmybgr0LkLUsRakg/cTOcmL2vtMAyBuWnD0cGi3fTvvPdWuxo2i7O46HcnW8Bosy6gaVersOTr15+Jm27t2zAuXJT/6uf/fj90P/dn//R0NrKb4Rkqv9qv2ZtuSGXsgVxo5bO/86X/x9/5zw3SIi3GC+/cfNCwKdbjUfXW2dEX3vwbL3/8uT/5x/74bDZNPAAyQxJUUa3qifNoyW5tl1G4MN4VhZq0Dutw3NAQkMuz08e78+2OI2d+cPdhynz95tUU+6Hl0lZ7W/viiAzVYQsF26aFwq1W4Y0vv8F9rrG8YADOLWVPhJ8n5nUlJABUVWcdS1Z4EjuFoIhACMK5T2m5XEBIi7P+/lHz/hvvXZluc2hDVTlbcQzxOE2n0/Fl14aNgxocDRl+6b/8hdXjk//2X/gz02mZu5Ym43pnu89ZEIqyykPYNN3f+/l//mu//bmQ1zHJdGR78pvNAYnqrOprXZ4stp6ZzFz1jd/97PWXn9/dnaskECbAxCmnLoe0PFtyqtjby/NikOCKerHupKpOhs3cXBETv3r79v6lK/ffvl2jf+3ljzpLztDZ6sFzLz1zenrWg2zNR9N6AmjY27Nev/yN95qeO0+9uXAxVOF8fPEDX8S5m16VjTU5x6c+qSfmUgARSSk1/aofmvXx4eHJSaJBQB+cvH909JDqclIWNZjtckpQ1VXRDptUFUnSP/xbvyDk/p2/8t8jyGLZQtId48yOt9MwgLlW2bL6f/78/+sX/smvgBFXcujFLIZHPu5SdmA7HQR5vr8LpvjsV7/6A5/8eLz3AEFm43HOApKMJiIaTaoCEAFi0nfff5C9FNV0EWXIkYQe3j26duvK2w/uvv/Fz3/s+VdqUyZSZ71zo3Xz5qsffYFDo23cbLrcJ1GMBg8WzYOTh6rOYVnpBVukraoCPjX9PyUlApFMBCLKzB82CeScc87dSXt2sAAmIXN6vDHDiHwawbyESd/0hSQ2abNYxb60ZTJ7lz7/u2/aof+3/vLPkTHz+USM+PlWLpgK2RQaVisy11Yn4Z/8wr9IkEuCGHjsqgd4VjElG0NlJwk5mjub02vTSV3ah7cfXH725tt37n7k1VeUKAyqSsJ52TTOuuPDR+xLXkcq3AtXb17a2yYTU+pKGB+dHtzYnlngYuxm04ktvSsIRFPoLIGvx5KGCCzklOzp4uytd97N3NZ+HD3Hki8YALFGRawiKapBEYEn7m7DnMkQkpAogjz1ScUYYwxNuzpYLTWBpmybodqCkyYeHJxWt2406wejyy/UVLgyA6lzvlsMmJuf+OM/4YNMditUshERuO0j6aBna0UdOPzDX/qNpcSZ0eNNl9hLvWYCBbmPebdZNvPd5zZhk44X7zfP/vT3726Grk9NP9ST+89evQzAqkDRtPcXAp04F6yK0unh8sd+8lo99beu/Jhh3y6apjkpdq6AmOXDR+3piS1svT3anj7T9cNkOnOFne0qsFksD9aR3ztcrFZdMakC9BXU9sJDE5949vCJy4WQRMUYUhUiUpZvC04WkZxz2/YHh/n+O6uJr5nd4ix87OZ1OTw5SsdXvCwWq506jK5tWYXVar3ZrA+P737qxz/hwTlfRRiUfOW9briyha+25jQe7ven0+Xf/zv/VUhdyjlTyNx7Lmtw2krlavWrQeO6wmK+VaayPhUY0+liDYIxvr83m7AkFgUVqAqhNGRarIPZhGduXS62po/bNWEoTTXZnW7t1qBC1q763pcjZ0y/SUfNQWy7fr1pNAuwBScxGLGnjw6kmnQs42IrBu7TxY4/WKMIRKoqBCgACISkCueBDoAIKh+OGAQAIur67uT08avPXTt+/JgjXKaZY7vQ9MU7bzzT/PDD9x7cnD3TDdPpaF7Z6gu/+6WPfu9Hciz3dq8YIxHjYr2K0tlkna9KR04pB339i++vj1eDXYN3k61qcXQSwMz3p+mkGXlX9iPqxrrlp9X2eGbSYX8395o8EamWfTcUI8/K6tDNxxbKruk9oRV64ZXne07ZFSKaMIdhRWILJ242fvkHfthE7jbrg+PDt998syx8WZTkUJQ5JU8TGGR9cgz7l5yvCfwwnAF3Fw4AMIAgAMC37i9IhMxsrTmXPgEAEZlzzvn09Kw7bidu0nWDlC5u6/7N/erh6PD+8dn9k4+++AqaeP/OnYrq3/rV3/7oa69Cbq2WGjeBsZqMa0x1VcRR9uTa5XJrf/q5u1/4zOffSsLWgBojg87N7Ob29t52cenqZAFWz9aPH65XZ23Fud/fur+KfQV++ciODbr50eHZzWcukaoAGuNcrkeFi37Y35lfuXKz7QdrUbEYlWVpjAzUyrJN2gxSsqnGs2uzrVvPvRTWy0W7IYuL1dlicbY+aYYBFNgPAwvjuFAipYtmQfqhEKDzlXA++pasaLZPLROIADAgZI5NaL5y+/1UkYZYPjNK93qzhStazneu3n98T89W3c39Mc7/b3/7bz54Y/Gzf/yHXnhptHvjand2Onn2+c+/cbtaHJdG4uxyXZabIAVUxXT+O1/8/O37DzpSjEi+zRu4NZ1uG37x6pVo0w30w47Z2q/fejQ8dkvXmAZxduYG09uhOIt60CxvwLaxzqpRMnHUoOp2Lvbm21T4NiQldJosFsoAGOf1/LTbJMMZUheDChfG1uNZQWgg1Zz7kB6a4ct37/Q93hh1Us2b0NXspzS+YACEAAAtIouIfnsiw9NEifOvRcwdyGrZhPcPX/re1/ov3n/YmzfePZk/M/3CG19+eO90ItX/7j/9Gzgbjc/crSv1D958dXNv894bS5z1O7MdtvTcy7e++Ju/OXW+Tpbnrt+UPqzsfDg4W2x6S1bKMXL0+wDzurj1TFHi2roanXVmtizjrVH1zpfeGpjh8s6mXZd9tsYFTKudFAL7uiBPiMRQbTWRRtV4d96EQS1FApu167rCF2SQhfmJdU+UckYXwHR5UEmGpAuhRHz1uVsvP//Sm199q1muGlMk59ER64WvACQCUFED+CGPjzIzGXwSh/s0PA3VCm4W7b1HZ+/FL1ePV+MXrj/jZiBmdOXW9dmzX/76l1+8eW1+Ze+HP/IjP/VTP/LorXuHh8uvvH/7MDZXd6Y/vrVTTYrvefnFh2/cLbv0lfff2BpfurW/TW5vebRyGZwUPtl2PLSc9q/v++0SnJ8U006zY9wSN/Oufe7Wl84W9o179dYIXNGdLrNwayaLq+urz02Tiiuo1HHwjfN2vj1f52ysrRmIVUja0AuogAqhVSSBTOdB2ywsGZXRjMbbu3tXDs9OyrL8I3/8RyThr37hc4/OzlJlG3PBewCdh6Odhx8BACKc28rPTRSqogiKSM6yastR+7g4OxtKrB6AmU2PVs382nyHdBt2rs73uCznpvi3/8RPfPLHXm15VY14d89f3inuvXH7yvblX/rFf/TGN96od3fspZ3d565f2b9BwMtu+dY3FoGguuyCM5Py0iiYUkdXi2t+dlWwigNqkmx96SssnLV09VQnu9uV8Svtl/vW7Uw6gwdHGxJrLCkIi6ZJiUVZ+ioLV2ThdDMvqso4AyAGgQgUkjADZHXA4nKqicbGoVJtyg6tjsbBmqOhXWrzye999fnre2ND5xzjAskCMxlCgyKK9EHwyBOrhHyQFgJybioFaYbh4aOHO1vjgC5SnD/Mp9fC1bpq3xjqa/EjN155+Prt7izWV+IC0mw+u3Rl9+rN7a/ruyNfbe/v/PLf/PubP/KHX/70D5DRK+Pxcai7eHj/a1+dZrd4tMp5fKx3RlX6xLXnbQnfePfQnDyc71wezXA+ur6E2MemtFhdLqx199++U4y2+9bMhrSKZ2c3ZpARPRDAoINTe3m+N7AaZ3vO1WjEIeUQxvNJSL3mrCKxH9R78cYAkeLJcnl5e6/RQLYYcouoTBSVHApIfOb5Z/eu5stXL18sAPThVAhQQjCgdJ4DAU82Z0BVEEFV5ty2fb9OTguaRqMc8vtehtHwzI294uqNl3/i4y/F0rmXbigKdxAFmqhbW9f/5J//U4u0vHJz/6Xve/Xuu+/91q/8xqJbjbZ3B4qtFmd8oh1v4XhKhkNLFq4+u1cX+OLNycsffc7WWyVsm7wZO81dz31artpHD1d1ed1k2L8yiTWXqGzbXISoQuogU0V+vjVuuFWyYiiPysZJGLlVHs69r9DH5vFJXDeVdaTQDX1hbLZQghqnAyclIAWjOMIigiZnyq0t8v5iAbD61AOAKAKIJMqkKJqZ+Txo5pw4MyuslqdHj+5kJW6HNAxUXJ/X9eb+A7fdmRiEV+z5tz77lZ/58R+T906H/YF24qId7h6fDllG62Hryt4Oze7eOfqG/dwzN147OTnMRWUnWYdssWjbDCSu9G7PqzFHDx+tTxdnbfGx/ens5lR94YuCU97emkHHcS2llY3v01aZh2g2ElaxLYQUTUX1qGLrI4sV2qu3Rr7sUne4PmUAg2jRrNcNExRb0yEnQrKTuoJiHYc5QJKOCVABWZyauBmKaclZZ6aq4ILDQy3oufiJ5+GHT1QCVNXsrQFEUVARIEzCYUjtweYQAhV0bbT76I3bfUzNsKhuTF977Xv3vb1eP/Pzn/3a7/3q577/oy9Oc7R5u+DYDcP+ZHS0gubh2oOy1fne+PUvv77+RltfGp3Es2136bAO625opZmXRV074wkGnpU7O8/ulmeH28/uB5sn9c6IcPSM+sXWzvLx7fcPOWPV2xwGLGZzV04Lx1XOosZgNR5vYgSHAlK4yiVBNMYSSBYxCrx1dX+WWBVRfDacgBkHy1pX9UlqGUgRrCMVZS8GrQEowZQXHR5qPxSB/STkgjmTwczZklVAPTdFIGSR3Oc37j5anvKusW29SUVpXFkxzBxcHvOl8ZjEfeoHf+hzv/I7ue93v+c5s0iV0jrK0bBcxeHy9Rv9yalC9NlrX37jvds/cutTb735u3ceP2hWKwEtq5qYuEkj44oi1ld30fEr33N9e3/XiBvV1aDXuxwf3Hnw3I++9PZbx//l3/1lFJ6UzltqiiQWRozFkLuJ3dqanA0dGwTjHy0OJ2W5in3OaVoUlopTbgfUjEhkvJ6HQlFW9oAMGFgMWQFQzqhkDGbVqHIWVlHjBQOAqKp8nniOSE+czgrGGEJK8qQggYKqSLtcfePB+9tUuy4PPrE3mMGzdzhuQ94Urqzhhz/y0V/7hX928Pa93clkmyaaeVg0eZFL74pNMuUoGoptlEgrjr/wi7+0wmHZnNiIaDkzJjGSqN8Ms0sFM/lSX3vthimIZMjYjNGKmsu71xHcz732k7/4j3+9mOypdjk2L21v0ZB7Dz3yzHg1yqSeTG2N5HAWQgKxSClqYXkXi0HyQBIkZ1APxAJGxTsXJJMlYhBVg2QAR/VoxSml3Gla0wUbgyyiKqiIGGNEnqR5isqTCg2E54naIsLMi8XRfGw1xOZWSWjk6/fryiVZXN6ZXdq9EmN/1HfNvcYAvvG5r356/2a4UXf9BmJO1raL5v5b98Zb48mWNRZe/b4Xq9sP20Xz5sN7yKagmCiyFAPCaRrev/Ogri/XJZW+TH1s22RteOPt4c2vf+VP/fT3mZEPuTP57tVbl772/lFZhJkDnNtkUJRqg5e3rvZBAP1WMZqm1MYhkEkESa2A9txOTBVFmNmoTqwxbNfKpFAVxaLZqEU2wOebX+Zus2RjjJIBY/8N+AOQyCCpsBAqEgmCMBo1GROIBTAApCyxi8vN6WtXtw4Lsz3b3tw5FD+lsdv72Eev6Ki/dzBUaZMOzVD81Pd9/4/8wPe89qkfofm41SQiOXexWS8enb768kerrQk4YwCFdHV09nf/0T/70v3blWLfFYHTeCSraN97a/HK/qx7tjY6EOWcB8356M7Rlz57+yd+6iMug2OTIU4nuztlx7Qpd5ypTaJkenX1aDzfPgybgXLotc/A1TiHcO7HJwVNpolNYykrTbB0AfoCuhy3FGJmQTODYoAIkpNKBEGjbMCKkCDJhXvEvoOUxRiCfG6EIABS5fPIe1W/Nb9Uljv11qU3T4ZTgn4g+6vvfm5MqcS9LU9xvROv/9W/+j+kUazcOAFUGc4Oz/YvXf2d17/che7ms8/O6j1XV2dHx2987fOf+uFP/6Ef+bH/49/6RQCtVWyO3OWA5n4+O0s3t9penc+cLCpl/dE/vPuHfvTPOd9BMgCGhQGCcFMafGHnyq7ZiQmzETszkZgJ0LgOAUubgQVF8En+eyZVJKtgRaL2a+PaIVhna+fbvi+s25tuDbE7a1aF832KAGzJJQMZ+OJzxJ7mdZ6HMasoEDKLgScBucaICOccu25jyeMIy4KtYdpJi9NB7x595I986td/9SuXtnfDCets7/gEfvszr9+86q4+d2M8n6U0vP3mG//in//6n/7zP33t1g0EA95l1MvXrl7a/4mU5OqlS7u+PoAhtaGazkNud9dZw3DnrUe7s2dhBKCCzMjlSX/IHVHW6bbb2d3201nsltYOxWj8/DO3PLselSq7s7O9zm1CEXERUCBlECUxSjaDAW1APdFMTaK0Qel5MJasiKt9agaDAKo1ladhQcaDYkleAhTO9zqcR4RcID3JX3wa+60g5273c7novLqPQs4c23YzHVXlpNAJrGDz7OT6p/dfOYLu/uL96RW6zOnkzfcWb93JZ2e/9Ru//NU3PnNw+KhP/ee+8eX51d2/8lf/8vWXbvYxpiyiSkisGo13o/G1Szt/9o/94T1vt50vsUJrXJ2r3fHn3r49NL0hJAvOINszU843fbXp3L2TcP/Rpl3Lv/fv/rsf+/iLz7767PzqPlsRlNKWW+V2E7oMoIiopFFVNQN7xLkpRugc0iTT4u3bJStKKhFGxhjhJnSBtOd0sl52/TCdbycAMNaQGam9Xm9dne1eOAAWEED0idWTDKoKx3PzjzAYA6zCAinlMAyj8YjKcnW0iBi3r8yvzviH6LVfffsr+b2zI1upK/Pj5e7u+OGq230/NVfv3NPwt3/+5/+dP/pzn/vnn33t+16ZXbuqTR6abjQbkSNvraRMFf6Vv/pvf/Xtz3+N71BNuqY09nPe+Zmf/Ys/+xc//Xtf+yXnTS9Zk7e91K69c/Ion2o4ni1PVlXp/8LP/eSdw5NSIRNh14/dTAANFimzc1mR2JgkYsgEyU0fq2IEJOhcVdUJwWYxJttkpn7Wxa7yZki8yM1Km0jnVQBoKbEGP8dUq/VSXDQA+kGapwiAIn2Qj/hBXQdCz5kXXfdgdXx1ZCIPseBLV3f36+26G/7i9/239t99Dtv0hd/9wtdfvzPbuNJWtkvDUf78L31N929DwlXTbt6+lx4v9j723POvvFzXdbNeTXenEpHIMOdqOvrf/43/+D/4a//p737ht17c3pqbappHf/Ev/ez+8zf+2W/+Qg6KyWLuSdE7uHl1S7VLaThZ3t/Ks5OD+5d2byzPhr5femPne7tnuQ8EBk0pCE1vnZUKQSETQF2wAomeYhhd3TozXKLzAwNldplyTm1P0xEbSgqkcLmaVky3+2UEeO/0gKLE/oKtoXh8cgYfpBgiEpKoMoCiPrEFKWLX9e+8d/uzv/u5/9n/5H90sbf/N0G/fucrqkjGVGDW9x9ef/b6gUbKKoRGAdUwUVIm0WjyJS0osHFWCAqlJg69JTVmx0xyzHuTWSX0cLNxk+JgfbBeLf4v/5v/w9/72z9/gb218EEotAKoskGThQmf5ihjEk4xnp4tUxQA+B//9f+V861SKMc7muP1ne3Hy8yPTr7+5Xe+/LX39/L8U/vPq3Prw9X2TXr36OSlWy+/MBlDMTOVqUs3qaTa3vrxn/m5gOidEWU0pmmGg8MHq/YMAz5+eAC7dVzpg9e/nmkYzVY/9qlX77x9cLqOVBTGOe9LLIrJGL/nxVd+77e/KMZM9/ZnV68dnJxs11s/9Kk/3CNX6JBFnZvduHqWQzZoAVGQgBJLJrBJ2KIJigTkClfa9WZVuNIYg4J71XxfyjwCERGVy6NZBM7FrAsL4n8TURFPMrZUhPVJTrWSQRUEQBZNIT48ub8MpwAgeTg8ON65sSu96R91j+83m56GB/d37OT5neuCY7TFCMv60pYb9bMCj986evF7bWjCyFRgp0PAzf1DyFiNvCiIhM/85q+v1t2ZNotuc/Dw8bXtHV3iW1/48qW98YbXz+9ug4HLV2aTeVoPoev72A7A43bdyiCf+EM/WBX1ehNoPDpZnM1nWwCApFG5NK7PCQ2JkgIyKQIVYkZlteSBERKCUWyHUDtxDgF0sHDGKauzm2ZWGEMWkigDuxxTPzTLFDu56ExhK6qGUPU89uSbFTDOizEZY1Ieus2yW2xKdgAQ3l4f990XvvrZ3b3p6sHZzepy6aFL65FN9uFKL3EyWuxdizG3Rbk3nze6eXDvweUrz8pg2aEvSoHhM7/+q888/2K5U33pK5+NHMGT6Vto2+nYSh1LxZf3C67joEOCllXQoqtSabwpitT3immd+eHx8vhzn/nYKx+5ce2FXuP+1nY5nwCAU1LAwJnAFIoIlFUZwQMV1kHMJdICGYEyp15kUpbroW9DdAaJsGCcF3Wyahnaow0xVFfn1mJKLVDO+cJNEedZL8z4wVb84RoazKwZzk437dmQGgUA36cXL+9fn/rD5rGZeO0hpHbRpJ1Z9lN6fHgMe/XZ/YMSxn53a280uTP1PizPuLlWbZWO1qdHO1d2FssHi6+e5kmfSamYpExDCiNbl9ZUtjg8OhzVbmdcjXFKWZFHQwrDIM3AIQXJG2PHKYe+i0npq1/9yuqke/7VW/vb2wtJAEDn4U3G7JbTaVEd9ss+94ooWeZbk9Xh6XRSb0KPMamIsYiehi6ocfFcAxCsyQliynG8VQpK5hwzb9YZBvL/BnzC+MQFBmDUAIjmRAQCJhkLkCDT2cntddstHqwAIE/sfpua+/n5K/u6DXmY503vUnvvoH33cFNq9e6dkxdeuHVwcLpJB1vPv7zjyOKsXbRmL4znZR9NlPMU4Y1qxzwu7VhCRAc4T0UxMVpObDuelbZCx+Ha3vWDe90mD8SUbY7rFDZGR5zW6urCoEGDD0/uXGq396qxLQkAGEmRtqgqxHQ5t6ErUBBsxny4Oi3LYtkFsC4Cduv19e09aBPE1Fhj7chnEZDHaWGDveonwYJjVMinm2OJCSPrhesB54A+VccAQESUAAEM4JDT6XB2dHYynsG9ZgUAX/36PW4eLqHAO1kkrzufmrOdyzsHpychhpt+/tuwmfejaqfenm9/7Y3Xx7uzF67chAJWbZip2F2Ty94QcxjQFrZyqoColioyqOoQ4CMf/8jxw7vKfV3K2eahsybCkGkbEzI7tJCgd9PSeONKt3/p8s7OzuHx4eTyeGf3CgBcNVunadVr32LSoJiY7XkpP+0hDhyECJSNkdl8VFb+8ckxok6LkUQAhR6ZSS+pFc495IHFAS5XZ23qGZgvulaBPc92fsL3EUWUVQAQgZFRJLXH7Ru/dUxTKvoKAB7dO9nds03Kr47mfmYer4f+eLxpoI71TEdmEIIC1qWdTy/rvtvdP16f3H7w/rPf//J0a7LmVZ6q92hSsqRx4PnuuFeOkAoqjSsEEhGMt6bkbjy+c9uSuLHf2ZuEvmsQMBJMTYwpcnVyFuauItSz0zNrinpkl5uzvc0EpvDcbKfs4bBrBoikVFjLEETUoQmSldBoJkED6J1DQhzVDvTmzpXS+Y30j9aLQdJjbfoc1sge0DUhpEAEQfniA7M+nJEqAIIKCFnYGYPCIQ6PDt//2sOHB/dPZr0AQAECZ93cT86WmzGUp8tVlULft2NjIOuDavNJd5PH9H7/aA1HO/P59e+5Dgcunh4e8WJnp4Si7vpcRD2vgmnQAoCilKUDoAxalBQkzC7tzkaTg3sPpBhWTVthWUlenWxaadu8rnEyqSYeq6KA7b1rdTWzRdRkmrPV/jUYeLM3Gq9jP8RMRAmUwBRoXC6MKQYZDJBkJIOVKXMAa7wxGIZUgiFQibEkCiDO2DGgE3iQN8rBJiifplBcJADypFwNAAhkA4CEyoBkNrmTsHr97fdOlife19ZlAHBawBkPdTzDHG6vtA3o3dwbAehBLPrvf/6VHTNpt12p8P6DA7q9oi1/87m9YaspvB86jhgNaxjipWvXkyFIOKMyWYEkAGO0HgtnyLv56LVLV7vm9GzxWEXXpxsD2TiDriylFCx6HawYbWDIS6Jy4jRoAwDIbGzaqatNDFFYCBnMvt0u2GsBJ/1JpuyM77Hblfo2JCZJKvfC4ypayRpV2ZotcBWZa6Od1aYtNjEzIebA/UWrAd9qjnYCgpARxCKACHO3kUfvnM5SASAFMACk3LjdqXIquCs7UOcHYAlCrowhvTy6vhZbbJdTbzah/+RHX96vxuLTSh6W6FIechfJSmmrsz4Wk30RQ5iUBmNrAR37oq78eDwmJlGJ6ur55XK2k5PsPauzorz34H4CcWQ3zfLx0b11v25Oj8cVjkM9VMN4XABACp11Y0+2AAJjekwmK5KSB0Z2ZDKn1qTKmJazCDMwoKhKKxGAAMgmScDRm1W36fuOIQySlUmw1HzRecJPww5VNYkQAaoaIlElhcOz7vNvvFGaLMgtZwCQNISing4ShcLIhX4YW8vGbVoxMV2tIhUhdlmHcv+5eTy5fzptEHN9mZRzjjxAdBaOj0/9/k0uPBEhQ1EXXUIqHSqXBieTcXO2qYva2KEfGuuMsYUrR4enK8FiNpkKihC8Mtu69+DdxSJ1muNyjX0fogeA0K/LqnJoR8bFEIiSKJzyhmAFIOc52RZ0qmYNQyJgYQRBApHzVHi2ZDaUVjnavOZVBwFIKakMyvHCWdC5ECIiCqoWFYCyEmAfY4rp7XuPeOjGpEPITY4AYDM0Rwc76qd7OwcUgaDeDIsybZeTvUs3cbb9aNO+sjMyO6ji5xO7pJPJdhEhGzbrZZOcj8SCaWe+o5CssWhKJSidF81GeDQZFbYYbK+kocsgBqBQcMI9p2QNIWgKPaFFddNiC7dymxtdbVKQ7AUA+j7UMQGCEayMEcmRtJfgkASEARBwwjAtyjthnRENYRYVyRYcgApA4lzk3GuSjNK1GBAErUop7C7aI0NPMuMRVBIonzuCWUFZ+nZ440tfxgEbEWtmKh4ABknYxFbBprA9AIGz5ThNnI3N5Ut7z+6UN8fF89NLkAqdPBz8+lK9G0MxnOWw6CAotVkWmml7Mr1SmcIYAQdM3hi3NZ7uXtou5mMUEmFfGMHMRGBdn4dVG4mM905yn+Ngi3rTNUmJHMauJcg+B+YAAOu+b4fOAVo0UXOAlBAKUmRRAUJ0AEDQCoslh6hJDTlVZ9AoAAMbzZIkcW77NaU+mDCQJmZGyXjRLMgaI5pV5YOCtCoihkgSrzbt0f2jPGgzgpY5JgCA6Cka20O4scEJefB4PDWFVIXZxM0yFjcqNS21oehA+7rwJ6enK6MKIrGduKosuSr3L9/4BBQFuCLmzntjVZK0RNOiqOrRuPAVGseMUWU0Gvmiiiqi0flClfthQOc4c99uOhxU2UjuHY8TLkIGgNz1TWxGo3HEwJBBVIGJSJBV2SgVaKa+SKEDkzGrGqcsqCoxnfOingOQtVJCH4x6pSxZ2GJKuTAXHJhFIvzEJYl0XpsYAIYQEuaj9erxwdmlapL6dpk37BgAcgjkipjiu4vuuB+u+WLGuc76KZrrsv/yO4+bw2atG511aWXDMj94725ebeR4U2hZ0PyZ/R/8yIs/6oxBYIhKSklSl7ucpO9jilSWU+NLsn5I2ZPJ/XDy+FBiovP61QrC4oo6cc5xsEFPT1cPF2c4aLRI2QLAWWiGZokcIA+QE6qigGTOEsgIQSZJ1patQlBUNVlZVIyAkgoJoHgEVpa2o8yDpi5FB0Ss3ljli94DBPJ5liQLCCariGgZc2J47wtvmCa0/dneZHz3pOmGFgC8Lajlms0KihR0dXh8g5yryDP6LrbavNO242i3Cleks763J4Bb76xfe+l5tzW7dOX6M7ufGDgg95Li4MgYw1EkI1pkxZy0MIWCKinHwYlLIqfLs0vbO1VVi0hKeeTHoKYZVogkA3frJq9xWtNZOhwVlwEghJWEqjtbG1uUlZsiDEG6lMlwQ1BkZ7zrYsMGUIwSOUgKkDFYUSLKmROAJTUcNPdDHmryIlFzW3hrLlwRO39/y3myPBk6f59LypxifnD7HvdDX3hjR3PHfUwAsA7d3I0zkyt4GPoeqRS4oY636gyRRuF4cSL1NoGjgsJcPrpzeTDllrtZ789LP4kx24kr/CgXA0eJLFkQiEzohIALu1kcTXe2c0qatO+7gbNy5jSwL4RFRLx37dAOQ6egq2YFPBgaookiRTssACAt6WzWWx42Fldt2hbrvZ+OSmdKCwwh1eSa2CWArBCRSkFWDICqgqpP3h3CAiFZUWsMZkzMZF0BxuWLXgFE+E1TBACLgDISPj46fOvdd3xZRLJdSqUilxUAVJPRctNb47xDL8qID73dFRjFvIdWEul8dK3cgQPBLU2+uTwu3PMvVPemJY3mk60chm4YQpkTh9iBGgrK5A1t+mXTOmuaZuVHZUpps1jHTaMW0SgSsCYGQQNJQ5AgGfrQ9BFRpqK60pwClp4BIAQNy56rMK8mQ4zVfKswysBdG3xJk6rkjM5UFWeANAijgKIXsJYocCIEr9R2AaOkLEESSUpiCmsDSXT/ZuKCPih5CufxCjnnhwePu6FPmV0l/fHjyXh7gRUAOCSoyk3DSdxYqBRY1uZKNe+1+VpYvwZ742mh0irOqZHtnZ3q6q2te2azDCkNy3g6phnXwEQKGfwYlK2wxki2SDkfna1sNQlMq9Vysz5JiZnBWDIbmlkTYxyNRiENm24tifvQM0TANJlNkm/GIYCMAaDBDQxVsVxeqyZbZdGGDZoqs2oxidgGyZuUa3C7VBhbNTA0qR0EMgoNiVACqbJISJRVs6JBsIGjKpVZsrUXbo5WOM+LV02YRFQy5xS6w7uPlptNmDjhTQ/pvdVmq9oHgMmQtSz5EpuhZa5TkqJrsagF6FThd5v1T96YUebT2cqcpSu4d83sH/dtL6v1KsYjXe6tZ/MbhRmTHBvpQkoZ2ViXhKB0jPnRyd2zth46jqk16DgiOt+BUT0bVQWHnoM2q6ELqzzkkWhyxox9Nb50vHlYnb+YhLDrl0NZhe6knM+OE6ykq8DV6qFJxah+nBaXt/c8UZ+Hfh1nbrxVlm2MnQ2aI+bzogYwQEabAdQErC14MIUZ4YW7JM89X+dZGhkFDQWWddd//stviDpcDWA5Rm+w2gwPACApU0w0xIEMonWlpXZz7+jo2gvP1CcdBpPm483MujhsZiTz0Sanz3/jK1FFh2ZWjJcP84+/eDPwmUZryRgFA14DQBYmyQaGGJ2QVQQwgXPK6opi3S5yKEgpMy0XTWo6yYGQ2Go9mVy9du3k4N7YV+dKjVOKxizaZrqqdwvvDS3BMPkmrCekq74pwSwPjzMITIsl8LpvXd841HFZjYpyiCE3PcYEoizACtGIcwQp+HKkF54f8LS6MIAigIoK89np2etvv9Nq2nbmrNcUWW2XKQIAFxasK3p2TC1IMFkd3A39s30L6wiXymvgr3b27dTOR9Nx2nrjd29/4zPvrxGxjGZkP/lDr4FRRROZldIQQlnUBkzGLgxpSGk0HrEwEWZmQld5w7ETYWY8eLyuJpPEIKqWSGvvyVbVOGcdjab9Zh2oA4ChC8ZQw2nZdfW6pPkoIihmwXSN6ofDej7aqbM1pbu9OuitoBEnYpnDOkFWZYEuOk4iHBkEKAv5UamcEbKBC3ZJPknSAwAENAJGAJPcee+9xXrRcJu9hIyJ+6qOxs0AYNltgqUBZJLEDJ2tcYXDsDV63Kx3y/FUGJ+Z3vFhqpOqHqge3nzvK8V1G2/64rK9tVf+4Pe+wAIpVlnDJq/ZsRhJmHKRGQYN7ajwYqnNLSM6NRAS5lw5I6k1JCF2UWIEKaoKCmuM3Z1uX7p05fIzzySghAIATCTdAAibFJqQMlNGZW6NZqsSUBdds0jdMnQsopIFhkTSIg6A5KucUdgm4YQiBpPAxG2nAakcDcYGvPAMGZEsGZQdS7ai0Qwxff7rX+OMMzHMto+9Jdc1MJgeAJRzc7ipa9ooblWzg0Uzu7x/aeGWzeFHJvMHjkczo12mxnUbexzfTW+vXvnBKx/b2o6r8NzWDVtd5qwhrg0WNhkw1MXgvO0TbDhWHgeXUxuJSMTknJAwqxmGXJE4O84ZLTlyZCFP0EBVj7bnqR/2r1+rRjWcRABgjwxQpo56p6WakI3xirKb9RAGUGqx6zQNMZVKneYJkiowQIZIBmPuQSBTqTh4UdNk61i0qMgbTI4uWAqiLMkiACfWjGBTSqvl+vVvvF1QBdnO7KT21m+VUJegDgAa5ADDZjhrrMGy3JVq+jiihOqZq8T86os1NoqrEUkLiOsvnvh68qWv326+8t7ug3X9yWeUctYIBqyKNdlyqAkhy2rZ5kG3prt90wtwkggUo4/RBEIowQ+jKntjnLUgBaGCYl2DtYQ4Go+tMfuXd01FAKDcgviMLjjTQFZCYCkEJ2XddG1klpSBbSJSr+g4nxf/ZonEm9im3LMJwIyd8ipNqsr6VHq1kjT2KhdcNZEyqHAizpEDM4nko6OjdtlZzpeu7x9vTlSQGVKMNQEAKFMfMUORYrOJm2lhLtXjZXf2qGvaPT9/YauDjgl7MjbScbBxnJ6F6tlcb3//y5sZGJA+D21oNYZeNkgpS+o1YU5b83Ec2sIaB2A1Q+4AdUixT13UIUfJSVQZLYhXtKb0lbO+quvxaAyIl6+8XEwvA8DYzxgw5WCRVWIUdmQcQxsHKRwgXB9vn9y+oympAGQSVFVFURHTbaKJKjFGaBHYErCNAyZ1xIBgCrlwaygpoACAdbYklEHS/TuPTIBq1/nKDNx75zGhRaAcAYAYs3A7QCA+CYs3Nw/vNsc8ojrT3W5Rb815RJuh63N9cvfxZjyao3uV/amD8PGrM3VLzTEEU2AiEUviPLmSE3cnx5CUnItdFxvBNOVhDmzHhSdEcT1lRh4EUzSsBsl5Ai3LIoOiJUMUTASTASAPmzRED1bSkCjVZWW7obT+ZGgCBEC9f//h9Us7R7fv5C6ZCFngvGge5xhiDCmRosYEOWlJGeX87XaiNokTuODILCJBQKvkQF3IMfXDm2+8bmsPWuqa/FCt110CDsJtTgAgqr4GVUkhSoxc+c7q0rBtu+eeu1wuysWjwZMNctYdbODtd7ebvJiU5cduucJHZkiyPDwgTYcnj5cHKQR7dHIUupNL+7vUcj9IVg/oGLMpu+OwPBmWGYohA0pyRgUZCWtfz2ZbZKiuS2dsu9oo62HfSVUCABS+mCRGaZJLOnr81p3rtqoNDQiCCprN2CflZy5dsSqVohnEJXDMPgyUe0aOOYr6zDgwGCkrKApRToE4mXThUhDik3IpRCy4OVm8d+/dY2n61B/ERVtHO3Wm9K4uxSAA1PXovHCi9wYNmaoOxkJdJUiza2POJ1PDhrGJdrnOr87GZ2X75VHe+p5nYtflTd8P7WQ06ZrBWZRwH2koq+3TA7HjqrKKgmoJXKeW23Vb5hIzQtIylpq0DwmSjLHMXfSmyAyTuuahq0s3xLYTxq0ZAHTWCU/FkZrgarr00q2VhJX2ATAzcI6eVC342hMpZq6zHbFzvZpNKKN4QBFZcRyEEbEgZ9SJAFrNFOm7F3P/1wBAEc4/rDL0w5318t2HZ6M0KYLp1l1dVJDFACmLsgBACIOIiDAZcIQugg9YicUE490r7cj3hkFzafFdDf94tfid3Fx68epQCuSoAI/Wy1SO3n50ugb02WuGrDmnPvS6pAiGC8Ys9vDkFHMepTr1oacmFUG8D4R+NPbkpM+FLUQ0C7d9EyAtQ5NTZmsAwJXVOFQSqap3rKuYOvS0aZOTDJKyYlDTO2k0BGJGubSzvzvf5SFllphzSolUxw7GBZKGwjJKEM6CTqTidNH+AABABCJF4sThM2/cVnXjrgc0psCiZUmY+xBiNufsz6tHdGBtgBykyDjypSw3H/2ej98oeihG46JyExlfxRc/eWVVltVo5wd/8PubJqYCG4G+H5bLBRodQFw111TwOl/b2bacBWiAINytT1emAQtFD3HdMLJCj2u7LIwd2Tp5gnIchjQqqqOjA1dWQeC0WQVJjgEALt24ev257ReeuTV/9lpNhR0KB1XBZgSFI2THvUVG8VJgpqjp3snD95eP2tyrqGMSVI3JSAZLpXEC6Bi8OIwKfMEiEDypmgiABDGELob33n0nOzoYujxKQ9sxeEcFhNzkYTKaAoBBHzkiSIwME5dr2t3ZHVF1wF1nxgCxKixoObLF9deuPbsfu5AcoRPHXdVJM526zcOTrb0pJclbGsPZweODrZs7moVdoexaooex0Q3jqLTLfmJqjRhRx1hMygmWRdY4nxVp6OvprFmuk+TFJhzHRiGzEgAI1c0ujY03KiIhAGDOI499G3cmFdX1ctE2Bgk0Z2Zg5QSCimlI0bIdEAtLiI0il36cM6kVBGNzzmlI3F8sAHT+zoDzSpT90Snfflg1qSomsOmmTCO0KsgKRe3ICQBwwMQYdHBVaSrvJi6HVjbduukrqgu1BFQVY+2Z01CV6ROffGW97pEFhpxC6PqhcoZyXyoqj4dkXTUXmSRrE6Qk/O7r747RjB2Z3Ddnp5V1MQ1CmFaxqCam9EPoC0f90AlpJD3tmsN2GSx6NIwIAKy0QDqJoQLrx7UtfBdawTiqypvzq+PBXZ1uoZByBGVLTkF5iCEGJSDjcj73jpCxjhCNAUEYUszCrMgXXa7myWtdACCm9PbxI+E4GY3Qj+Iac8CNps5zb6Mdky8ZADiTdd6VLqrWVeE489AdrM8edKuOSAcL6AfkRVyuLNF2uR76biBTO2s20vLQA3iyBQnznHXNi2KL6mEYmNXmJBvveVRZN8E85cP+KPloSrCF1JOtBECImNhWk4B8Fhedz6epS6gpZ0xFZgIA0eCzyaxkzDIEyJaFepWNxqhaluMuDMionJRzCKzikA2Ck9RTDh7UQlAuERwaFuiQFRGTgR4GMBdcquA8SIAkC0d+7ytvPdjA4HMJPRDxOsDZughZA7tlkjYDANtgNVPvqIAqxEr4gFuIpazO1kehlVVoqIiGg/38r71bF3ut5A46IFynlGiZcoPlFGWcnWmTW717UvYSXXR8VLc2rWU829pOaB3rot4fbzWg0zwaWp4UBafELFU5CiGXRbnq12xYMQOiojKk87h678wsap3xcLMpAI/jMiVpB1pjeOfg7dvH7541qzKzsIlkEknIfUoSG3BiwCSRdTDojDWFjUhZK/FWnICqz47iResBhhOknELuu+HR1w80oo/0ySsvO4RyPgpG1Ubnsx/5TT8AABJFFTICOSMWqS36TRKMIcIXv/ju7ePV+nH31u2zYellSgNKCMkTZpY+amyNZywhUexmzg3DJmrOSG0bG3AbSKumKdg0ol1Zb4ZGa/aaAoiFwnuvACIyHY0gBGetQWehyAlBAHsKRs/fZ76rxuV1sz49L7u26dqAEpU52pih59hym0AZVEQ0s/QBeHAGVRQUrGJlnSe0qsTZCKeQc9/l7izmldiLtgXFNEQOg/Cjs8XdR8e82EzG1dcf3iYQkTxylvvIDIoQUQGABKyxnvLcFgUYHPLEVpG57fO9+2ej42lnxt37d6aX9NM3n5llg2hM5XXIMmTbx5kvOQQOgtl0Gd3u9goGKJViuWpbWxbs3GJchuSD5WJnOvdl8rIzHznniqJwzlVVGdIQCbJ1PUBb8NINgRQ4n1f8Wg7N6arFqlQWy1QNxdHjTZts33aMGAQGMANwl0LOGbOWClYDKjNiy1ENAWhpDaToECAniYlFBoGml6G7aFuQEGaUiPzmg/sn3JMZmmH1Vjxox8WhNMPEsy3IliGzsRYAMLEMsTYuj+u1S02VBx4gC0DOwvfSe2eP3zrYrQ7FdLd2TmxwBTkLizycSAdTlwmwqHw5Z/Xv3n/Eo7IvJXnx2XXrBGyavsEQL2+MO+1VrEYwZIzLRMSSvfeiwAY7iRHUAHkRn1KdxaYn2RNrh7EYgx9X5fjs7BGH472rJbuVKSEhB0DJdhgGo+TRSAoQBAUJQUAygjpD3hgiBuAQLaKxpunTadc3IRi86Ex5AKMx913z+jtvNzHqFtpg5kmm0c3ZeHAetMTkcywSAUBQUYNmVFQACN1kCnMDJkTvzUA86eud+WyivvKjdeQhCmDOvLZBSxq3TcpMUXtEBM5EcQY4HK5zNjkvq3oUfWx8A5CU4myyVYAZqBurIxPHo3EMvXPl0LMaGniImoeUNVsjJVqbiM7LbjJjMfeQ2aNNZbEZVcEaVGK1gUyEXGpEQJfQD7GWBGwyFwxMaEAsii3IAJpEBoWCxHUfhhgM9FuTqaGLVsRQNYO0zfDG579hCL1SXgxu0K5dc1IEo4xEVgxK8SSJAz0FL3vZ745nf+ln/jS0KUMFbjLZ2+kUN3nBvi12t2oItc6sVH3XrZfKYsxW4UpMqYGiXzYHtFVBwhFNVykfmCGXWTFX1WRQPNMO5sBoFZx3taZRAEHFftNkyRFjKHRwGQlQQES6FCLnzAwAKJAxF46VO3TGlIWwWkEU5BARUsA+5JwpxdRpzB2GQNxKXnEAZwv0LhdZGEQBMZAAgjGmKAtVILpwYxyqqp6erjZHm8y5iWGZ0kqYCzD16Hiz2RCY3VmDuck9AMzr6WQ0KidVV6IN5p/8099pjCmmflxPoU07r+wkb8tqqtTVZWWKTTmljO7x6UG3PIXY5yY5Y5NJxyeHo1JSgVAVMzIea2hzTbUmAEhN7tSgTc6rUyzEb7UpFNY6QEHcJO5idtmUYElBQBVBDbEIAFhAl2ns7bJvg5JhBDQDi/VKkCyZjFSjYxjYcJDc0sCSxugqS6DBEaIzikAAQBgNiqr3hbVWACJfdI7YoBH7+LW332k2nFnBhiFCxo6wAkRIitqnhbO9I1YAGDbDFlVumYe5WqHl+ixRKDjuTyfXXtq7NNsuLl1yXA99ZJHRbLvtlv0m5zZZN2gsDYntZ16N+Pk4eqOcQoTEu4ka0FgKpzAXF61PRWFtEKNYxVybTZfmVWENSasJmRCBKUAoBADJA1O2SAUAuCExbKjc69ADkyVQdQqao7CQj5oVFYQiQTQxsTWOJaaYoDTjsq7RDCloRiBuJCkYHBhtcupVUxcu+CU+1CF2LHfffmd7VhQF1NOyM50UkCBhaUyBxaiIzEImAQFAMXIWnJXSxCRMeVCHlbN+bz597bVXrl55Znppp57Ny2rqK49+1ARYdMIzKxM3SNrYiNPZcWih5gAmJvW2KF2VJaN3vaayKHWAypdIuXY4tqXPsF1M0qYDRlsVgwxGpWCw3WDOqxmd1xpEFEUAGECMq876LlkGLxEYBCogydozC6IY05vMIpaxNs5qVtJBxZnCsnrCylg0TtUAek1KLkfoex42baty0XtAGMJJ0+aDxdXtanvLte1QTrQPYkrXSWROHGVIA2vyRQUARGJLN3ikjKnPm00coozG5fd970ev7V3rBXuBLiQyjgq/7pdR0+nZEoZQ23qS3dga6EKX+yuFcYVNkJAgc2KPiCDIztrVpinBFKy9aCyLxoI6W6HLUboQsNLgpFeB0ijyOds5jy9254nmzpXFtAlRjcQcBmbhCKk3AAjACBGYOUlOkiIPHQijSOXrUqm0NkHOOYIVUQxDlNT3tBo4hNy3y4P6wjPli9hvTk922LvZlnjHHSBuqsZ3EhFdaScpDLY0OSfJAgBWjZY4VFKGCask0zmH3/exl0ZjTBB7FjRERCnLCAvhRnnVNyfbOzcXrVyZzsV0OcSHXZrNKwuRScQJeuSuwAATPyozwryunTfJVMWM2JfOE/dgbUrAOdVGp00KVKgIa/LijUFLbmbrT7z8EQCo0VrJpbcAJsbBWJM4WcvaB2sJhNFINeRSFDlbX3QxmMxTSN4bcJQMCGvSLosQJKVBSsot43KATGfdBRvjbKvp4NHdlz66997m9tDMj3E9PZ3ayxJTKFpha5wbdf1QYdUWCgBQpQGXilWHLqWEGZ+5NL35you8U68aoJkJm6HMsu1sw1mD9JvKicfhbFTPl5Jrn5qq3e/NZlRDSFvFfCHJBTU950ka+mxxSkTB6diY2pCaRNaFJpOrvKJ0crJs903RTiC6Wjcp2c7HYu/y/rXp1t5kCwBmRbXqmoCZSAeiImUghmjFmDJuFl6Bp5NYxJgKW8Q4lJYCQG/VWUdZMGUl37NEGWxMlVSD9COxp5uzo+MTvPBM+eUyd5GqcmvbIRblWO1Jteg2m/0DsZVJJOtmM9mbprY/T2htNmEkpbZ9b1Maurp0f+ynPl2MHOZ+AtwtpGB0aNFUFDpiTTEQaKEuwIaruNuPllFsUdatiAWf45TYgQxFCcZMHHbH6xvPXs1iCEl8DgL71U573OmsB6oGgDffuvu2TTqx405e+ciru1Vt7aSMaTKdEhgAePXFVz7z9S9XVJgoqMTIrQRhrQ16MiSZh85GjDm3mIwno+QJAMBarxkMuj6KkAJh9tT2TC0sV+uTzbI1+PhsdbEAULt66MpNOeqnNe1upb3ny4+/vHPzIzuvPbt/dX+6Oyr2JiNAZsqFAwCwZbluB4l5aMPQdbduXbOVwIwaTeIQxm4NG57ZOKpygn7dtqdnlTetK4qJ2xfEoTjZrN2o6FiDJSnsADFIl9Km3TTeusg9GFK2aoshtt45Y0zkNnUdoghk8Oasw/ub+ObRo9N23YC+c/T40emi68K/+Be/CQCXZjsvP/uyV1eK9WCBDIIlazOCqrViCg4OAVDJUR9iHHhsbWELgewLk5IioGdAFlZlC1iYhOjn20Mikgv2Sdp+0VXkvdORWJ5ol3JVzT+io/jaZnOcpMHj4wWETfC2GwYA2L+2f9Yum9Wm1PGV/Ws/+iOfnpQNdUGThQipXNVGbGgslYsQEAhFR6IYQNukRU2j0aQ9mG/iEp3rhJi3i1pCYukVaEj91pWtoIy2jgilwLgqBm6l7Kl3WvBkYtvlmdzpD3gt5ebX/t4v/+TP/YnNKq83Z/fuPS6hBABkfWb/yrt33gDkGFK2YhUxQaBkWTlHn1JQI5yMsYUxpAjMha+EUh8iYcmcMCWLch403tphfHnXdOOYtSovunKucJCEnTF2knZpNDWWOTdjK7rjdWW3Cz/TmdtbPWxPzpYAsDw8K+aeaUKOX7x1C03S8VboG5skKY4N9nE8qorHaR1Ege3jdv3Stb2UdUzbFZTLYWnyZAEVljJ2IsB5AKFJb+Ok8ne/9vAjH32usE6xNeSzGVFZrDfLLOXUU3IiDNTKadVkRG+m9PLV199+T3DerDen3cmLz9wAAAF59/03LatR2ItpIdqmiM6K0U6GgnOJVZLoHOXEaBFLBhBD0qsZW8oyEHBLEZQgsS9R7EQRqormz7/8+WvfeO/NuxcJQJTTuiAeCGkigzhy3pKWkQpniPvEO0VdC42CGdclAHz/87Pl2e7gb5v5/JPf80rpHRq3TGm7zTiv1qEvq7lmkiY501crhUYe9amiqvLUZgk9FNN5W8ge2LvrYTYLziKEuaZjtrNiXCbDQ99fHU17g4ao8PXpyaq0XsrCWR8Exrt72y5RvWGtPZXqc2qHybh83PfHqzMAYBnef+/O177+qPRhXMZ6f3dWFFZx6JYg6KBipmBMycLEfc7bMnKVUyhIMIcUQBhj1mBNSbZsNmlcakgQPbTDcNHWaLAARkO0qpmYyhEnRPC+mg+5nbmtcaVtc4KgbtcWYABg/8b1ajSkxd7Oi5fieDOd754uThViU0RvOxgwEZ7mTW8Hzf5ss5JyDNlMUKc1rzKfxLRvDaYu1+PL1bhfLI13krqKxrGnemtSloi99pIkwPZ8nhMMUWrgcuQReVL7T33q+75xp77/9Tfep860S702vra1vTo9url1OTQKAO/fvrvrq1vPbd85uffw+HB1++6lajoBe+XFq4QeBAhzyFIoqMGYcu2JLGUUEvTG9Go6RkCvgiICDlfa5zalnnGk6IcLBiAO4yKhYExukMzeUhXr3sNEnatJULS2Ng1aJ1ouAMC6YrrVgd++ceUSq8iqk9PWcDG+MvHiuxi1iwOlWERquV1nKOOOVNWE8kjWm84pO+sm4iIPpgkjLWDQkjTC6ODukbu1ExLUlYtjXzE7h91mPXIeQFClJJeazaiuP/H88z/8iU//6t/9pTOMMAC4HkxXy7geWwD4x//s1z720q0bM/Pc7Nlu/9rDxerh0fGj49O3v/Do1jOvXd65ZHAxgtJEVqOzorSOxCAKKCdFKrES55NE4azEQVlKKLh0IbZD04aLBqBIhC6xZc121ttU9nYII2MUSGxihIJojsXK2VSOAeC5S1tD3FIwnF01KlMjUGF71s2EwoCzab1ZNcZUKJSbKClJrbFz5bwuQzNtoRhfDlkrq46WbrQnHPs+NgGrSTXU8BH1MFhFy8lnFetdf7goXe2sqUztrT88Oqo6/upb90L3havX5ofHh7we3lg9HG9NttwspwYAQu5Rg0PrgXAEN6v59f3t00171A9EDnMLaIS4JxAVBwTOIGAesiEOygU54ShEtak4s6Tskx0YyFfAiuai64Y6yckPQlxGX2AZaDgpeZyHcjzyUiJypuAEHLj9ag4A853ZapCQoOhNn4TQJEvskwVJBribknEAzTh0fV+18mAiM6qKTVFY2TSSet+PyUQoZDNBG4Y8NKIZPWzWJQ4yzftkNqZHNpPteQIFNIUrjWQNLKjGFYcnxw4GpXx4utya78yc2dBuiMxJr+3tAsDx6aHI9boaQwIyjnOLBHu7U7eaDcOJUOxklCUHjVVtXYHeWeGMBpmUUYNElGyIKGfP4E2puZQyr2K/7hPoRUdFNJOlApm+yHW/rEPJkK3NvmhC0OQ4WsmkaHxpvQYAKOZVURaaNY3gKC7WcX1wdji/tO9IEmzqQrNp19Iym7sHD9cGTVfP6pT79aOW1rwOeYOBjzerhL6RIVjtmRnN2dHBlck4o3uMzCVmzirQMPegA0tU6DJv2s6Ts0p+bAsPKeY3v/H+V7/0ugO/7yfbO8WNK3sAMJ7sXn3meT8dcyFqsbSTwtYGbbKR0BE70Y7S+auskkcNoTecQVijcMRBMaOVnJgTQwqSAkCEYeTw5mRc40X7hCEVKqBWWQrkAXSypdZBdgJ9kcQJGRJvC/EEJQB453OI0MBygAz0yBwWy/0dN8vB1pYCLfyKUrvdbRwO/Qyq8ZjyEOdReICd6Y4JhTFa7hadXa/VD2hG1o0DQYx2ZIuBQUc5V6NqXKLTk3YynvfS+yIXNkkX+2VcbYJ3xYOz1Ru33/P51GJol0dbY7x6ZSY2A8ClrStmtDXd2kUkBDFOyYFTKiUDiwAwbYxEWwSAUGJhyXe5jFisQaQkQzlaLogUmE0mz2yakYw42kbYXfxLfIIxhtDmzH3JprDUK6ipCuacsnPGqB+aoZzYQAgAnOpVf1LPWWSti1TmPtyMq3haavbi1px41FIKGGzX8HhnUtYFeH04LE5S2tmaToEEhjQYqU0Rppl7ARmG4Afn1GdMijEHrWYFAAsZV9jTtqvH29uujtCgSxHa1z//6PD0xPliNC8aCeV8x/oZomxvjwHgU5/63tXZ0k1HzhaMeeCcJQvZs9wlIsg2DkYh1JHrybglcJhTSCRqDDALMZgsbFyQpKLMyjpS7rqm+eLXvjZceL0gj2gVUHhUWqNF4ixkkhib2VvDKBppZKsQg7oMAMAwm87C6tA3OtuUzFvpauGMyUMA1nbNG8gFFM0AXQkMajXv1b7motx042yGgjsn12SW2qHPR9aTs+40HNzavpTYYokCaU41iKQkIyhrxpZ1jiUDdTGebY7fufvW8th0MbHpq/Xk2RefuVzPxpFAURIDwMsvPHd8dBK6hnyhAU2WJNj0AwAJGlXYKqdNbAtbELjINKTegykQrXGBNYWMmQNm62yOPStHOV6u5O/8X//pumlCfHzBABD0HHU0rgPzmWJtwXnUDM6OQKJYcOSAk7MZIQJAWcS5p2XY6spHebpaoHl2AwjACQenWy6ueiN91aTFLsWt8X6hlBfdaqDC12GAUiAKrdex2YZxpRwJetuecHoWwXllrp1HRVBIzGxMvzypjTFqQsxHx4u7jx61fSbU7WvTZqfdc1cnO/Pkc0fNWHfaTQIAFNjd2jsV6foNAFboosTYx7JDFGFN0ixGru4dkfNFILZVaIcubUZUZTTJggPjjISh4RxU5fRR95/97V/55Pe9Fvrl537j6IIBQHW+dl2KSlp4ACpCSobEWhMEJSN6EOdYPSYAAHHjB0Or62DKzeFQzsZbxYSGVVuP5yfdGXZUFJBsf3B8Wnb1C7w+1ZE1bg2b61u7pheqmx0cN9uauxiqqMnBcdy7fIUvuTGCh5r7Mk1rtjZlmsyn4cESJ5ZJOKTRCzsQs9xZKUU9Ts9c3rKFiSFkb4ydjmMe37wKAJv1ajzbKqeV72yIG7bQ99JDB+QVVzxYq0WSMMFLMsiAevDW3X/0974yjB9yO0EMuF3vmRlMpNqrbySP9eSXf/kzr3zk2g99wqfwibe/8qXmQu2hFrXMtOxhU7kbHhhi8ohocGma2hc1kEeTVAnQGwMAiYcWNzBpKRd7V9EyxhTLKcZlLvq4DKduuhuXLUhwIwvDXkkPu/FzcHS2niRb8r6OOA7iY2V3eumwiGfrh1vb12Z5RCp+WrOD2kaT0FoymnkI9az04Fewmnr4xLOXXtjSo4N16YtY85RqtSJ5GKhSKnMaAOBsvShGdVEWzEKm6Po+dJFBW46WFGK2hFyMI2dSun/n8T/9hc9sEm2aqvDmIzdeHu9uHZ2cLs6OHz4++9LRZhhg5OCVS9dENPjNi89cfXDv/gUCQFjYDpHKkQUQQUSuDGmAylUa2IPLwkqoAN45AIBMnmo3Gu3sTI0FQFYdDQpSP+QBXVGmNsKKXYStSbWZqYERd4ud6dbY1oTUdgC5JqlFNtc3tuxGG2Pa3d45NKQhNVk660EyE2DTrgTElRUDEaGRPGxOGdvxDWOuBDvPVSHTytSFq4sCHUBmAFh36wcP7orI1as3BFwWw5GjZDDIIUnKbLCKhWe6/e7d//c/+OXNYG597FLX0x/62Eu33/zqnTtvfeq153/2z/zon/mTn/6Zv/inIIWyLH/pn/766aEZhrC6aE2Ysh0yTSRtu8y2qBVNAvHOejEFFcwaQNkiWkiSAWBU5ldvXrl5ea4UnVaVKzysPYwXZ7Nc5j710OSuU1LrAp7AIsB2XN63U7bCowh1XeRccKhqF4LnO+8t5277SuH62OUKxHA1KoVMK4LGL1aNFM44rwIFFpWpL125XIym+/W1bbu1pfVkXKHRaVWNy8IWns/LCgLHoT07euysq0aTEIKyBGZLoEPMliOnWOBX79//xd/5tbUHKvm1j93cmVdf/72v/PRf+Euzl174z/7Wz//yP/jnsQ2vf+HrL1y7+bM/9wNXP7L9S//gHywfPQz5os3RWgig926Suk0eRMUEw64UcEqkCQSRnAgZSeepHFJWasZ7l6bz0aPTo4eP2x2y65gKGzsOI79dd/Clk6PLOwXEWC2K1p42AaqCDHNha8hpRYoItpPGrkWW050Zwaw2ozNnHCGHMB5PsougbrNsuKarJhntJAOSnYxcWdzYhF7B5kGRcOpnZVGSISZjkABAh8gA7VkY2p6JVv2q54xCoYtOiuhDIebh0b2vfeP2n/sTfyKa8SRrMvGP/ckf+LX/4lfefeurr33frU/85f/Ov/iNz/7NX/yH47X96T/1o2j993//9x2Nb/3jf/JPlyfNxQJAJueZio1r1n7kaTy2flQxOE55SNE5VxCBQGaKwACAllETZBiBKaxDa5IvD1NooDGcQyunEkYCE3EyBWNZOEFZxCZPMIX1sFyGibFms3EIhZajsra+BjcfCBMPKW3GU9/3rccig7AVV4+sn86298FLzCE0baG0O6ln9bgez2q3VWppRIhMUMnnVRcSq+YQ+tPTo4ODg2XsltrhkH1nF31vwNw+WP76r3/++3/glZF3ddGbMtPY2lo/9dM/9tnX3+g3Cbn9Iz/6SYMljLdl13FZYEGXbo3/xM/8zIUrYlSk0g9iczbOB0aGZCBYYWusr6ucc5KgCCnmc19cyJ216snknDfLlWaWkJwB9FkChWjvxDaX2BppSIDx+HCB1pKN9/p20J5xrdpWpILlOmTjPLLV4DYYrdpJrvaqvdSqA3+0elSWsS6sQxPazaR241G5d/UylgWgn02n09KXkEeOlfscWEPMIQBABsk5hjiI5kW7CSHQMLClk81BGMUH7935vc+8/qkf+eHRJNfFCPNgRHLSkuze1cl0Z/4P/8GvDszHby2l7z75Q68mT7EZmrOmid3to8hw0S7JDEzqjLo2C9hIYj0RGjYMgqpIQkaE67I8f4PT2NaI3CSDdlwOk/0qhW5dATfJXNJqGTap5GuFC7Oy3pzFnAvCalJb1KYdj6xB3x0mnOzg3FSnj4/mthhVNrkQS8snXTWboh1Vk1T59uw0g421Dcvj22+8+fpLN18uMJ9MzoyXyJLTYCNAk23B+9eezYghc9QMABwkDiszdoGhWa7yMDCLJBam9YPhK198/Qc+9SNlWVYpdGGtpthgTLmUAQzBz/zRT//f//P/4h/+0988PV7DHK9d2sVlW1W6GsZ1Ljf3fg/0gsPTrfF2CMEBAzDZElhyViDSnA1ZJHTkI0cFtcYAgCoBsrE0cMxDIM8b5o6Rsj9MoTesB5uVUJH9MRmt7NmyeXH6DDRSFX1Rlk6MFRyG/P9p7Uxao4jiIP5/e3dPd2bLQhIQBBGXSCCIeFBEc/HixYN69sv5CQJeFBWMIAgGNUYxkITJMpLMZHp7/XYPfgGFqXNBHX63gqJ+e+Ublsy1SlWJTECOO1GW9Vrj+hAzDqhVyTMu+kTP7Xz7Ph75L3o3w94mM9iUGBiNPDjPu0nT5Pt7WohkLhUz3RQAmupcG9mmtKir2hgHqPIhWHuUjz5vf11bvwP9th3VLzY2CWZrq9fnF/pVqRIaSyU9Clcurexs7dXO3bx7S0qZxbqSgAQyNgwGRxEh011q08rpiBPvFSbBOiKQDUAQRA4DBYQCsoVhkbDB47+n8yQKyFFvYgJZh4+LCZAAQxt7o2JmFUls5KkBp7TDgENbcFpIW4kkAW3KmseRcD2d7W4fJJ0EUwQMdFNgleCULfR6eXXK47iWuLaKJ0kkUJOfhiYPqFeaWhUoNpJipkpJI0FTrNUkoi1d6mGhj4fm4X3IJ6fpTMc2JD+vrbWy0aVystI/t34IRDo8U7X6+O7TwbDyGo523wgOBjFv1OKFvgowGkyWu7OhKjZfbc7fW+exqxULRFYNKoztt0RxPlUAEcXYBIFjbTxJGfINDqCNpYworQRhCRYOqAwqBA8Aj549n2b+P+jx0yf/5W/Keqm7ONCuUtaOcib4yf7x3v6JzkWji/Hh2exi+7DgKdIYSKEYEFU7aWytfhWXr91YebA6z4mJ+OsP719uvL16e3lp+SJXUT0uCaNpK55uF/EHlty3MvfwXdYAAAAASUVORK5CYII=
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[279]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">output</span> <span class="o">=</span> <span class="n">torch</span><span class="o">.</span><span class="n">rand</span><span class="p">(</span><span class="mi">2</span><span class="p">,</span><span class="mi">588</span><span class="p">,</span><span class="mi">128</span><span class="p">,</span><span class="mi">128</span><span class="p">)</span>
<span class="n">ind</span> <span class="o">=</span> <span class="n">batch</span><span class="p">[</span><span class="s1">&#39;ind&#39;</span><span class="p">]</span>
<span class="n">mask</span> <span class="o">=</span> <span class="n">batch</span><span class="p">[</span><span class="s1">&#39;hps_mask&#39;</span><span class="p">]</span>
<span class="n">target</span> <span class="o">=</span> <span class="n">batch</span><span class="p">[</span><span class="s1">&#39;hps&#39;</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[287]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">mask</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[287]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>torch.Size([2, 1, 588])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[280]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pred</span> <span class="o">=</span> <span class="n">_tranpose_and_gather_feat</span><span class="p">(</span><span class="n">output</span><span class="p">,</span> <span class="n">ind</span><span class="p">)</span>
<span class="n">mask</span> <span class="o">=</span> <span class="n">mask</span><span class="o">.</span><span class="n">float</span><span class="p">()</span>
<span class="c1"># loss = F.l1_loss(pred * mask, target * mask, reduction=&#39;elementwise_mean&#39;)</span>
<span class="n">loss</span> <span class="o">=</span> <span class="n">torch</span><span class="o">.</span><span class="n">nn</span><span class="o">.</span><span class="n">functional</span><span class="o">.</span><span class="n">l1_loss</span><span class="p">(</span><span class="n">pred</span> <span class="o">*</span> <span class="n">mask</span><span class="p">,</span> <span class="n">target</span> <span class="o">*</span> <span class="n">mask</span><span class="p">,</span> <span class="n">size_average</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>/home/allen/.pyenv/versions/3.6.8/envs/py368/lib/python3.6/site-packages/torch/nn/_reduction.py:46: UserWarning: size_average and reduce args will be deprecated, please use reduction=&#39;sum&#39; instead.
  warnings.warn(warning.format(ret))
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[212]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">_tranpose_and_gather_feat</span><span class="p">(</span><span class="n">batch</span><span class="p">[</span><span class="s1">&#39;hm&#39;</span><span class="p">],</span> <span class="n">batch</span><span class="p">[</span><span class="s1">&#39;ind&#39;</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[212]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>tensor([[[0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 0., 1.]],

        [[0., 0., 0., 0., 1., 0., 0., 0., 0., 0., 0., 0., 0.]]])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[255]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">feat</span> <span class="o">=</span> <span class="n">torch</span><span class="o">.</span><span class="n">zeros</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">4</span><span class="p">,</span><span class="mi">4</span><span class="p">)</span>
<span class="c1"># feat[0,0,0,0] = 1</span>
<span class="n">feat</span><span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">0</span><span class="p">]</span> <span class="o">=</span> <span class="mi">1</span>
<span class="n">feat</span><span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">0</span><span class="p">]</span> <span class="o">=</span> <span class="mi">1</span>
<span class="n">ind</span> <span class="o">=</span> <span class="p">(</span><span class="n">torch</span><span class="o">.</span><span class="n">ones</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">)</span> <span class="o">*</span> <span class="mi">4</span><span class="p">)</span><span class="o">.</span><span class="n">long</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[256]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">feat</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[256]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>tensor([[[[0., 0., 0., 0.],
          [1., 0., 0., 0.],
          [0., 0., 0., 0.],
          [0., 0., 0., 0.]],

         [[0., 0., 0., 0.],
          [1., 0., 0., 0.],
          [0., 0., 0., 0.],
          [0., 0., 0., 0.]]]])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[257]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">feat</span> <span class="o">=</span> <span class="n">feat</span><span class="o">.</span><span class="n">permute</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">1</span><span class="p">)</span><span class="o">.</span><span class="n">contiguous</span><span class="p">()</span>
<span class="n">feat</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[257]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>tensor([[[[0., 0.],
          [0., 0.],
          [0., 0.],
          [0., 0.]],

         [[1., 1.],
          [0., 0.],
          [0., 0.],
          [0., 0.]],

         [[0., 0.],
          [0., 0.],
          [0., 0.],
          [0., 0.]],

         [[0., 0.],
          [0., 0.],
          [0., 0.],
          [0., 0.]]]])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[258]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">feat</span> <span class="o">=</span> <span class="n">feat</span><span class="o">.</span><span class="n">view</span><span class="p">(</span><span class="n">feat</span><span class="o">.</span><span class="n">size</span><span class="p">(</span><span class="mi">0</span><span class="p">),</span> <span class="o">-</span><span class="mi">1</span><span class="p">,</span> <span class="n">feat</span><span class="o">.</span><span class="n">size</span><span class="p">(</span><span class="mi">3</span><span class="p">))</span>
<span class="n">feat</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[258]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>tensor([[[0., 0.],
         [0., 0.],
         [0., 0.],
         [0., 0.],
         [1., 1.],
         [0., 0.],
         [0., 0.],
         [0., 0.],
         [0., 0.],
         [0., 0.],
         [0., 0.],
         [0., 0.],
         [0., 0.],
         [0., 0.],
         [0., 0.],
         [0., 0.]]])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[259]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">dim</span>  <span class="o">=</span> <span class="n">feat</span><span class="o">.</span><span class="n">size</span><span class="p">(</span><span class="mi">2</span><span class="p">)</span>
<span class="n">ind</span>  <span class="o">=</span> <span class="n">ind</span><span class="o">.</span><span class="n">unsqueeze</span><span class="p">(</span><span class="mi">2</span><span class="p">)</span><span class="o">.</span><span class="n">expand</span><span class="p">(</span><span class="n">ind</span><span class="o">.</span><span class="n">size</span><span class="p">(</span><span class="mi">0</span><span class="p">),</span> <span class="n">ind</span><span class="o">.</span><span class="n">size</span><span class="p">(</span><span class="mi">1</span><span class="p">),</span> <span class="n">dim</span><span class="p">)</span>
<span class="n">ind</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[259]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>tensor([[[4, 4]]])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[262]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">ind</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[262]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>torch.Size([1, 1, 2])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[260]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">feat</span> <span class="o">=</span> <span class="n">feat</span><span class="o">.</span><span class="n">gather</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="n">ind</span><span class="p">)</span>
<span class="n">feat</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[260]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>tensor([[[1., 1.]]])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[211]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">_gather_feat</span><span class="p">(</span><span class="n">feat</span><span class="p">,</span> <span class="n">ind</span><span class="p">,</span> <span class="n">mask</span><span class="o">=</span><span class="kc">None</span><span class="p">):</span>
    <span class="n">dim</span>  <span class="o">=</span> <span class="n">feat</span><span class="o">.</span><span class="n">size</span><span class="p">(</span><span class="mi">2</span><span class="p">)</span>
    <span class="n">ind</span>  <span class="o">=</span> <span class="n">ind</span><span class="o">.</span><span class="n">unsqueeze</span><span class="p">(</span><span class="mi">2</span><span class="p">)</span><span class="o">.</span><span class="n">expand</span><span class="p">(</span><span class="n">ind</span><span class="o">.</span><span class="n">size</span><span class="p">(</span><span class="mi">0</span><span class="p">),</span> <span class="n">ind</span><span class="o">.</span><span class="n">size</span><span class="p">(</span><span class="mi">1</span><span class="p">),</span> <span class="n">dim</span><span class="p">)</span>
    <span class="n">feat</span> <span class="o">=</span> <span class="n">feat</span><span class="o">.</span><span class="n">gather</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="n">ind</span><span class="p">)</span>
    <span class="k">if</span> <span class="n">mask</span> <span class="ow">is</span> <span class="ow">not</span> <span class="kc">None</span><span class="p">:</span>
        <span class="n">mask</span> <span class="o">=</span> <span class="n">mask</span><span class="o">.</span><span class="n">unsqueeze</span><span class="p">(</span><span class="mi">2</span><span class="p">)</span><span class="o">.</span><span class="n">expand_as</span><span class="p">(</span><span class="n">feat</span><span class="p">)</span>
        <span class="n">feat</span> <span class="o">=</span> <span class="n">feat</span><span class="p">[</span><span class="n">mask</span><span class="p">]</span>
        <span class="n">feat</span> <span class="o">=</span> <span class="n">feat</span><span class="o">.</span><span class="n">view</span><span class="p">(</span><span class="o">-</span><span class="mi">1</span><span class="p">,</span> <span class="n">dim</span><span class="p">)</span>
    <span class="k">return</span> <span class="n">feat</span>

<span class="k">def</span> <span class="nf">_tranpose_and_gather_feat</span><span class="p">(</span><span class="n">feat</span><span class="p">,</span> <span class="n">ind</span><span class="p">):</span>
    <span class="n">feat</span> <span class="o">=</span> <span class="n">feat</span><span class="o">.</span><span class="n">permute</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">1</span><span class="p">)</span><span class="o">.</span><span class="n">contiguous</span><span class="p">()</span>
    <span class="n">feat</span> <span class="o">=</span> <span class="n">feat</span><span class="o">.</span><span class="n">view</span><span class="p">(</span><span class="n">feat</span><span class="o">.</span><span class="n">size</span><span class="p">(</span><span class="mi">0</span><span class="p">),</span> <span class="o">-</span><span class="mi">1</span><span class="p">,</span> <span class="n">feat</span><span class="o">.</span><span class="n">size</span><span class="p">(</span><span class="mi">3</span><span class="p">))</span>
    <span class="n">feat</span> <span class="o">=</span> <span class="n">_gather_feat</span><span class="p">(</span><span class="n">feat</span><span class="p">,</span> <span class="n">ind</span><span class="p">)</span>
    <span class="k">return</span> <span class="n">feat</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[105]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">_hm</span> <span class="o">=</span> <span class="p">(</span><span class="n">hm</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">*</span> <span class="mi">255</span><span class="p">)</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">uint8</span><span class="p">)</span>
<span class="n">to_pil</span><span class="p">(</span><span class="n">_hm</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[105]:</div>




<div class="output_png output_subarea output_execute_result">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAIAAAACACAIAAABMXPacAAAA10lEQVR4nO3WMWrEMBQEUEdS506t76FrGHxQH0SHcOdW3TaLZXKCgEm8LGTf6wcGBvE1DAAAAAAAAAAAAAAAAAAAAAAAAAA/+np3gX8ihJBSijH23o/jOM/zYtAANwghjOM4TVPOubW27/vj8bi4QXp1uU+QUpqmaVmWUkqtdV3Xbduez+eVbHh1uU8QY8w5l1LmeS6l5JxjjBezXsANeu+ttVrrMAy11tZa7/1i1g24wV9ugAHu8etfEAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAADAe3wDlr5I4V6pDcUAAAAASUVORK5CYII=
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[106]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">scale_img</span> <span class="o">=</span> <span class="n">cv2</span><span class="o">.</span><span class="n">resize</span><span class="p">(</span><span class="n">inp</span><span class="p">,</span> <span class="p">(</span><span class="n">output_w</span><span class="p">,</span> <span class="n">output_h</span><span class="p">))</span>
<span class="n">temp</span> <span class="o">=</span> <span class="n">cv2</span><span class="o">.</span><span class="n">rectangle</span><span class="p">(</span><span class="n">scale_img</span><span class="p">,</span> <span class="p">(</span><span class="n">bbox</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">1</span><span class="p">]),</span> <span class="p">(</span><span class="n">bbox</span><span class="p">[</span><span class="mi">2</span><span class="p">],</span> <span class="n">bbox</span><span class="p">[</span><span class="mi">3</span><span class="p">]),</span> <span class="p">(</span><span class="mi">255</span><span class="p">,</span><span class="mi">255</span><span class="p">,</span><span class="mi">255</span><span class="p">),</span> <span class="mi">1</span><span class="p">)</span>
<span class="n">to_pil</span><span class="p">(</span><span class="n">temp</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[106]:</div>




<div class="output_png output_subarea output_execute_result">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[149]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">os</span>
<span class="kn">import</span> <span class="nn">os.path</span> <span class="k">as</span> <span class="nn">osp</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[156]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">branch</span> <span class="ow">in</span> <span class="n">os</span><span class="o">.</span><span class="n">listdir</span><span class="p">(</span><span class="s1">&#39;/media/allen/mass/recording/&#39;</span><span class="p">):</span>    
    <span class="k">if</span> <span class="n">osp</span><span class="o">.</span><span class="n">exists</span><span class="p">(</span><span class="s1">&#39;/media/allen/mass/office_color/</span><span class="si">{}</span><span class="s1">.csv&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">branch</span><span class="p">)):</span>
        <span class="k">continue</span>
    
        
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>20000
0
10000
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[210]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">pycocotools.coco</span> <span class="kn">import</span> <span class="n">COCO</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">coco</span> <span class="o">=</span> <span class="n">COCO</span><span class="p">(</span><span class="s2">&quot;/media/allen/mass/DeepFashion/deepfashion2_train.json&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    </div>
  </div>
</body>

 


</html>
