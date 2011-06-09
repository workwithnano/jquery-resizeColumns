# resizeColumns jQuery Plugin

This jQuery plugin lets you enable super-simple column resizing on any HTML table. It also provides callbacks and javascript cookie writing to store the column widths for future use if desired.

Based off of the simple, working code provided at http://bz.var.ru/comp/web/resizable.html by "bz" (I don't speak Russian.)

## Demo & Examples

See <code>example.html</code>

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
	$('span#column_array_output').text(widths_string);
});
```

## Notes

* Very early release, bugs to work out, still some procedural code in there outside the plugin. I know :-) feel free to list them as issues in GitHub if you'd like me to prioritize them, or send a pull request with your awesome fix!
* This should work with any HTML table that has <code>&lt;th&gt;</code> tags in it. If yours isn't working, check to make sure you didn't use <code>&lt;td&gt;</code> instead of <code>&lt;th&gt;</code>

## License

This plugin is dual licensed under the MIT and GPL licenses, just like jQuery itself.

## Credits

Thanks to "bz" for the initial code. Thanks to an unknown engineer at Justin.TV who insulted my code test by telling the recruiter to pass on me on grounds of "bad taste". That really upset me, and kicked my ass into programming overdrive.