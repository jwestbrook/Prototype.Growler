Prototype.Growler
=================

Mirrored from http://code.google.com/p/kproto/


__Overview__

Growler is a [Prototype JavaScript Framework](http://www.prototypejs.org) based class that displays unobtrusive notices on a page. It works like the OSX Growl. It supports themes by using CSS styling. Also options can be passed to modify how long the notice is displayed or whether it remains displayed until the user closes it.

Growler also supports observing two events: `notice:created` and `notice:destroyed`. These can be passed in as options to the notice or attached to the returned notice object.

__Usage__

Include the `growler.js` on your page after [`prototype.js`](http://prototypejs.org/download) and [`scriptaculous.js`](http://script.aculo.us/downloads). Also make sure to link or import the CSS file for the default styling and themes. Please feel free to write your own styling for `div.Growler-notice`, `div.Growler-notice-head`, and `div.Growler-notice-exit`.

```html
<script src="prototype.js" type="text/javascript" charset="utf-8"></script>
<script src="scriptaculous.js" type="text/javascript" charset="utf-8"></script>
<script src="Growler.js" type="text/javascript" charset="utf-8"></script>
<link rel="stylesheet" type="text/css" href="Growler.css" />
<!--    OR    -->
<style type="text/css">
@import url('Growler.css');
</style>
```

__Examples__

```javascript
//Create an instance of the Growler Class
var grwl = new Growler();

//Make a default notification happen
grwl.growl("Notification");

//Notice with header
grwl.growl("...with header", {header: "Growler Notice"});

//Notice that stays longer
grwl.growl("Long lasting notice (20s)", {life: 20});

//Sticky notice that stays till dismissed
grwl.growl("Sticky notice", {sticky: true});

//Candybar Theme
grwl.growl("Candy is good", {header: "Candybar Theme", className: "candybar", sticky: true});

//Plain Theme
grwl.growl("Visit <a>kProto</a> for more Prototype classes.", {className: "plain"});

//MacOSX Theme
grwl.growl("The funnest iPod ever. Millions of songs. Thousands of movies. Hundreds of games. <a target='_blank' href='http://www.apple.com/ipodtouch/whatsnew.html'>Learn more</a>", {header: "iPod Touch", className: "macosx", sticky: true});

//AtWork Theme
grwl.growl("This is a test to see how well the theme handles text that is long. It should stretch height-wise.", {header: "At Work Theme", className: "atwork"});

//Important Notice
grwl.info("Something good happended", {life: 10});

//Warning Notice
grwl.warn("Take heed", {life: 10});

//Critical notice
grwl.error("Something bad happened", {life: 10});

//Event handling
grwl.growl("Notice w/Events", {
	created: function(){
		$("noticeevents").innerHTML += "<div>Notice created...</div>";
	}, 
	destroyed: function(){
		$("noticeevents").innerHTML += "<div>...Notice destroyed</div>";
	}
});
```



Real world example can be found here. http://jsfiddle.net/jwestbrook/RehFw/

__Options__
<table>
	<tr>
		<th>Notice Options</th>
		<th>Default</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>header</td>
		<td></td>
		<td>The title that is displayed for the notice.</td>
	</tr>
	<tr>
		<td>speedin</td>
		<td>0.3</td>
		<td>The speed in seconds in which the notice is shown.</td>
	</tr>
	<tr>
		<td>speedout</td>
		<td>0.5</td>
		<td>The speed in seconds in which the notice is hidden.</td>
	</tr>
	<tr>
		<td>life</td>
		<td>5</td>
		<td>The number of seconds in which the notice remains visible.</td>
	</tr>
	<tr>
		<td>sticky</td>
		<td>false</td>
		<td>Determines if the notice should always remain visible until closed by the user.</td>
	</tr>
	<tr>
		<td>className</td>
		<td></td>
		<td>An optional CSS class to apply to notice.</td>
	</tr>
	<tr>
		<td>created</td>
		<td></td>
		<td>event that is triggered when the notice is created and displayed</td>
	</tr>
	<tr>
		<td>destroyed</td>
		<td></td>
		<td>event that is triggered when the notice is hidden and destroyed</td>
	</tr>
</table>
<table>
	<tr>
		<th>Growler Options</th>
		<th>Default</th>
		<th>Description</th>
	</tr>
	<tr>
		<td valign="top">location</td>
		<td valign="top">tr (top right)</td>
		<td>The location of the growler notices. This can be 
			<ul>
				<li>tr(top-right)</li>
				<li>br(bottom-right)</li>
				<li>tl(top-left)</li>
				<li>bl(bottom-left)</li>
				<li>tc(top-center)</li>
				<li>bc(bottom-center)</li>
			</ul>
		</td>
	</tr>
	<tr>
		<td>width</td>
		<td>250px</td>
		<td>The width of the growler notices by default depends on the width of the growler container.</td>
	</tr>
</table>

__Compatibility__

Growler has been tested with all modern browsers that PrototypeJS and Script.aculo.us support.