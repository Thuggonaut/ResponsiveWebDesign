# HTML Tables

# caption
- HTML tables use the `caption` element to describe what the table is about.
- The caption element should always be the first child of a `table`, but can be positioned with the `caption-side` CSS property.
- e.g. 
```html
<table><caption>Assets</caption></table>
```

# thead and tbody
- The `thead` and `tbody` elements are used to indicate which portion of your table is the header, and which portion contains the primary data or content.
- e.g.
```html
<table>
	<caption>Assets</caption>
		<thead>
			<tr>
				<td></td>
				<th><span class="sr-only year">2019</span></th>
				<th><span class="sr-only year">2020</span></th>
				<th class="current"><span class="sr-only year">2021</span></th>
			</tr>
		</thead>
	<tbody></tbody>
</table>
```
- The `tr` element is used to indicate a table row.
- The `td` element indicates a data cell
- The `th` element indicates a header cell.
