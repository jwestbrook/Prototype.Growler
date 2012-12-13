Prototype.Growler
=================

Mirrored from http://code.google.com/p/kproto/


__Overview__

Growler is a Prototype JavaScript Framework based class that displays unobtrusive notices on a page. It works like the OS X Growl. It supports themes by using CSS styling. Also options can be passed to modify how long the notice is displayed or whether it remains displayed until the user closes it.

Growler also supports observing two events: notice:created and notice:destroyed. These can be passed in as options to the notice or attached to the returned notice object.

__Usage__

Include the `growler.js` on your page after `prototype.js`. I use the ProtoPacked which is included in the download. Otherwise, scriptaculous effects must be included before the Growler class.

```html
<script src="prototype.js" type="text/javascript" charset="utf-8"></script>
<script src="Growler.js" type="text/javascript" charset="utf-8"></script>
```

__Examples__

Examples can be found here. [Growler Examples](http://examples.kevinandre.com/growler1.0.0/index.html)

__Options__
<table>
	<tr>
		<td>Notice Options</td>
		<td>Default</td>
		<td>Description</td>
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
	<tr>
		<td>Growler Options</td>
		<td>Default</td>
		<td>Description</td>
	</tr>
	<tr>
		<td>location</td>
		<td>tr (top right)</td>
		<td>The location of the growler notices. This can be tr(top-right), br(bottom-right), tl(top-left), bl(bottom-left), tc(top-center), bc(bottom-center)</td>
	</tr>
	<tr>
		<td>width</td>
		<td>250px</td>
		<td>The width of the growler notices by default depends on the width of the growler container.</td>
	</tr>
</table>

__Compatibility__
Growler has been tested with Safari 3+, Firefox 3+, IE6+, Google Chrome and Opera.