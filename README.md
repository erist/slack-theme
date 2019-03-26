<h1>How to apply slack-theme</h1>

File Path<br>
  OSX: /Applications/Slack.app/Contents/Resources/app.asar.unpacked/src/static

1. Open ssb-interop.js
2. Add below codes at the last

<pre><code>
document.addEventListener('DOMContentLoaded', function() {
  let tt__customCss = ``;
  $.ajax({
      url: 'https://raw.githubusercontent.com/erist/slack-theme/master/black.css', // css file url
      success: function(css) {
          $('<style></style>').appendTo('head').html(css + tt__customCss);
      }   
  });
});
</code></pre>
