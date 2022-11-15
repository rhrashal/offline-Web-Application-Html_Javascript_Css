### Html Table to Excel Generate 
```js
	<script src="https://unpkg.com/xlsx@0.15.1/dist/xlsx.full.min.js"></script>
	
	function ExportToExcel(type, fn, dl) {
	    var elt = document.getElementById('tbl_exporttable_to_xls');
	    var wb = XLSX.utils.table_to_book(elt, { sheet: "sheet1" });
	    return dl ?
	      XLSX.write(wb, { bookType: type, bookSST: true, type: 'base64' }) :
	      XLSX.writeFile(wb, fn || ('collection_due_data.' + (type || 'xlsx')));
	 }
	 
```


## Validations In JavaScript

Validations are required in Web Programming to insure that contradictionary & unauthorized data is not get stored in the Database.

Javascript enables the UI to Validate the fields on Client Machine which reduces burden on Server.

### Validation Patterns
  The Validations in Javascript can be handled by using built-in functions and Patterns. The Patterns are designed by using Meta Characters



<table>
	<thead>
		<tr>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px; text-align:center"><strong>Meta Characters</strong></td>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px; text-align:center"><strong>Description</strong></td>
		</tr>
		<tr>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">\d</td>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">Decimal Number</td>
		</tr>
		<tr>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">\w</td>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">Words [A-Za-z0-9]</td>
		</tr>
		<tr>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">\[A=Z]</td>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">Uppercase</td>
		</tr>
		<tr>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">\[a-z]</td>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">Lowercase</td>
		</tr>
		<tr>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">\[a-z]/[A-Za-z]</td>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">Both Upper and Lowercase</td>
		</tr>
		<tr>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">\[0-9]</td>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">Number</td>
		</tr>
		<tr>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">\[a,d,m,z]</td>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">Specified Characters</td>
		</tr>
		<tr>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">[^,x,y,z]</td>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">Excludes Specified Characters</td>
		</tr>
		<tr>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">[a-kA-K0-9]</td>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">Specified range</td>
		</tr>
		<tr>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">\+\@\#</td>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">Special Character Must Preside with "\"</td>
		</tr>
		<tr>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">{n,m}</td>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">Minimum <strong>n</strong> and maximum <strong>m</strong></td>
		</tr>
		<tr>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">{f,}</td>
			<td style="border-color:#e0e0e0; border-style:dashed; border-width:1px">Minimum <strong>f and Maximum any</strong></td>
		</tr>
	</thead>
</table>
