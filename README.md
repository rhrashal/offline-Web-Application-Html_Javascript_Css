### Html Table to Excel Generate 
```html
	<div class="table-responsive">
	<table class="table table-bordered table-striped" id="tbl_exporttable_to_xls">
	    <thead>
		<tr>
		    <th style="text-align: center">SL</th>
		    <th style="text-align: left">Artical Name</th>
		    <th style="text-align: right">Image</th>
		    <th style="text-align: right" ng-repeat="x in sizeList">{{x.Size}}</th>
		    <th style="text-align: right">Total Value</th>
		</tr>
	    </thead>
	    <tbody>
		<tr ng-repeat="x in stockList">
		    <td style="text-align: center">{{$index +1}}</td>
		    <td style="text-align: left">{{x.NAME}}</td>                                        
		    <td style="text-align: right"> <img src="data:image/jpg;base64,{{x.Image}}" alt="not support" height="100" width="100"/></td>
		    <td style="text-align: right" ng-repeat="y in sizeList">{{x[y.SizeAmt] | number }}</td>
		    <td style="text-align: right">{{x.TotalValue}}</td>
		</tr>
	    </tbody>
	</table>
	<input type="button" value="Export to Excel" data-ng-click="ExportToExcel()" class="btn btn-primary" />
    </div>

```
```js
	
	function ExportToExcel(type, fn, dl) {
	    var elt = document.getElementById('tbl_exporttable_to_xls');
	    var wb = XLSX.utils.table_to_book(elt, { sheet: "sheet1" });
	    return dl ?
	      XLSX.write(wb, { bookType: type, bookSST: true, type: 'base64' }) :
	      XLSX.writeFile(wb, fn || ('collection_due_data.' + (type || 'xlsx')));
	 }
	 
	 <script src="https://unpkg.com/xlsx@0.15.1/dist/xlsx.full.min.js"></script>
	
	 
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



 ## time in js
 ```js 
 	function getTimeString(time) {
            return time.getHours().padStart(2, '0') + "" + time.getMinutes().padStart(2, '0') + "" + time.getSeconds().padStart(2, '0');
        }
 ```
