# resizeColumns jQuery Plugin

Based off of the simple, working code provided at http://bz.var.ru/comp/web/resizable.html by "bz" (I don't speak Russian.)

## Demo & Examples

Someday soon!

## Example Usage

### HTML

``` html
<table id="gpas" border="1">
	<thead>
		<tr>
			<th>Name</th>
			<th>Age</th>
			<th>GPA</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Nano</td>
			<td>25</td>
			<td>5.0 baby</td>
		</tr>
		<tr>
			<td>Enia</td>
			<td>25</td>
			<td>1.0 boohoo</td>
		</tr>
	</tbody>
</table>
<span id="column_array_output"></span>
```

### jQuery

``` js
$('table#gpas').resizeColumns();
$('table#gpas').live('change',function(event,widths_string){
	$('span#column_array_output').text(widths_string.split("+"));
});
```

## Notes

* Very early release, bugs to work out, still some procedural code in there outside the plugin. I know :-) feel free to list them as issues in GitHub if you'd like me to prioritize them, or send a pull request with your awesome fix!
* This should work with any HTML table that has <code>&lt;th&gt;</code> tags in it. If yours isn't working, check to make sure you didn't use <code>&lt;td&gt;</code> instead of <code>&lt;th&gt;</code>

## License

This plugin is dual licensed under the MIT and GPL licenses, just like jQuery itself.

## Credits

Kudos to [Paul Irish](http://paulirish.com/) for his inspiring snippet in [jQuery 1.4 Hawtness #1](http://jquery14.com/day-05/jquery-1-4-hawtness-1-with-paul-irish) and everyone from [#jquery](http://webchat.freenode.net/?channels=jquery) for the tips, ideas and patches. Much â™¥ to temp01 for his major contributions.