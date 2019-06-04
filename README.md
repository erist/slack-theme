<h1>How to apply slack-theme</h1>

File Path<br>
  OSX: /Applications/Slack.app/Contents/Resources/app.asar.unpacked/src/static

1. Open ssb-interop.js
2. Add below codes at the last

<pre><code>
document.addEventListener('DOMContentLoaded', function() {
  $.ajax({
      url: 'https://raw.githubusercontent.com/erist/slack-theme/master/black.css', // css file url
      success: function(css) {
          $('<style></style>').appendTo('head').html(css);
  		}
	});
});
</code></pre>

Sidebar<br>
  Preferences > Sidebar > Custom Theme
  
1. Input below Color codes:
<pre><code>
#363636,#444A47,#D39B46,#FEFEFE,#434745,#FEFEFE,#99D04A,#DB6668
</code></pre>
