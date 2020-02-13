# Search Box

Libraries wishing to add a OneSearch search box to their websites are encouraged to do so.

Please use the following code, customizing it for your library:

```text
<form id="simple" name="searchForm" method="get" target="_self" action="https://onesearch.cuny.edu/primo-explore/search" enctype="application/x-www-form-urlencoded; charset=utf-8" onsubmit="searchPrimo()">
<input type="hidden" name="institution" value="XX">
<input type="hidden" name="vid" value="xx">
<input type="hidden" name="tab" value="default_tab">
<input type="hidden" name="search_scope" value="everything">
<input type="hidden" name="mode" value="Basic">
<input type="hidden" name="query" id="primoQuery">
<input type="hidden" name="displayField" value="all">
<!-- Include below ONLY if "Expand My Results" is enabled by default in your instance -->
<input type="hidden" name="pcAvailabilityMode" value="true">
<!-- End "Include this..." -->
<input type="text" id="primoQueryTemp" value="" size="35">
<input id="go" title="Search" onclick="searchPrimo()" type="submit" value="Search" alt="Search">
<script type="text/javascript">
function searchPrimo() {
	document.getElementById("primoQuery").value = "any,contains," + document.getElementById("primoQueryTemp").value.replace(/[,]/g, " ");
	document.forms["searchForm"].submit();
}
</script>
</form>
```

 Replace `XX` with your 2-letter [Aleph OWN code](https://ols-support.cuny.edu/?q=libraries/own-codes). **Capitalization matters!** `XX` refers to your code in uppercase letters whereas `xx` refers to your code in lowercase letters.

For more options and the ability to create custom HTML code for the OneSearch widget, see [http://ols.cuny.edu/onesearch](http://ols.cuny.edu/onesearch).

