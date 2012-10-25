# jQuery Filter Table Plugin

This plugin will add a search filter to tables. When typing in the filter, any rows that do not contain the filter will be hidden.

One can also define clickable shortcuts for commonly used terms.

See the demos at http://

## Usage

Include the dependencies:

	<script src="/path/to/jquery.js"></script>
	<script src="/path/to/bindWithDelay.js"></script> <!-- optional -->
	<script src="/path/to/jquery.filtertable.js"></script>
	<style>.table-filter .quick { margin-left: 0.5em; font-size: 0.8em; text-decoration: none; }</style> <!-- or put the styling in your stylesheet -->

Then apply `filterTable()` to your table(s):

	<script>
	$('table').filterTable(); //if this code appears after your tables; otherwise, include it in your document.ready() code.
	</script>

## Options

| Option | Type | Default | Description |
| ------ | ---- | ------- | ----------- |
| `hideTFootOnFilter` | boolean | false | Controls whether the table's tfoot(s) will be hidden when the table is filtered |
| `containerClass` | string | table-filter | Class applied to the main filter input container |
| `containerTag` | string | p | Tag name of the main filter input container |
| `inputType` | string | search | Tag name of the filter input itself |
| `label` | string | Filter: | Text to precede the filter input |
| `minRows` | integer | 8 | Only show the filter on tables with this number of rows or more |
| `placeholder` | string | search this table | HTML5 placeholder text for the filter input |
| `quickList` | array | [] | List of clickable phrases to quick fill the search |
| `quickListClass` | string | quick | Class of each quick list item |
| `callback` | function(`term`, `table`) | _null_ | Callback function after a filter is performed. Parameters: <ul><li><code>term</code> filter term (string)</li><li><code>table</code> table being filtered (jQuery object)</li></ul> |

## Styling

Suggested styling:

	.table-filter .quick { margin-left: 0.5em; font-size: 0.8em; text-decoration: none; }

## Dependencies

Other than jQuery, the plugin will take advantage of [bindWithDelay](https://github.com/bgrins/bindWithDelay) if it is available.

## Change Log

### 1.1

Initial public release.

## License

(The MIT License)

Copyright (c) 2012 Sunny Walker <swalker@hawaii.edu>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the 'Software'), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.