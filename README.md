# advancedSearch

This project is a (prototype of) UI widget for building structured search queries. 
It is a full jQuery UI widget, supporting various configurations and themes.

THIS PROJECT IS STILL UNDER CONSTRUCTION

## Demo

Check the [demo](http://evoluteur.github.com/advancedSearch/index.html) for a live example.

## Overview
-to do-

## Usage
-to do-

## Data Format
-to do-

## Options

advancedSearch provides several options to customize its behaviour:

### dateFormat (String)

The format for parsed and displayed dates. This attribute is one of the regionalisation attributes. 
Common formats are: Default - "mm/dd/yy", ISO 8601 - "yy-mm-dd", Short - "d M, y", Medium - "d MM, y", Full - "DD, d MM, yy". For a full list of the possible formats see the [jQuery formatDate function](http://docs.jquery.com/UI/Datepicker/formatDate).

    $("#advSearch").advancedSearch({
        dateFormat: "d M, y"
    });

Defaults to *"mm/dd/yy"*.

### fields (array)

The list of fields (with id, label and type) to participate in the advanced search.

    $("#advSearch").advancedSearch({
        fields: [
			{ type:"text", id:"lastname", label:"Lastname"},
			{ type:"text", id:"firstname", label:"Firstname"},
			{ type:"boolean", id:"active", label:"Is active"},
			{ type:"number", id:"age", label:"Age"},
			{ type:"date", id:"bday", label:"Birthday"}			
		]
    });

Defaults to *[]*.

### highlight (Boolean)

A highlight animation performed on the last added or modified filter.

    $("#advSearch").advancedSearch({
        highlight: false
    });

Defaults to *true*.

### buttonLabels (Boolean)

The labels of buttons used to manipulate filters.

    $("#advSearch").advancedSearch({
        buttonLabels: true
    });

Defaults to *false*.

## Events

### change.search

This event is triggered when the list of search conditions is modified.

    $("#advSearch").on("change.search", function(event){
        // do something
    })

## Methods

### addFilter(data)
Add a new filter.

    $("#advSearch").advancedSearch(data);

### empty()
Remove all search filters.

    $("#advSearch").advancedSearch("empty");

### length()
Get the number of filters.

    $("#advSearch").advancedSearch("length");
	
### removeFilter(index)
Remove the filter of the specified index.

    $("#advSearch").advancedSearch("removeFilter", 0);

### val([data])
Get or set the search definition (as an array of filters).

    $("#advSearch").advancedSearch("val");

    $("#advSearch").advancedSearch("val", data);

### valText()
Get the search definition (as a readable text string).

    $("#advSearch").advancedSearch("valText");
	
### valUrl()
Get the search definition (as a URL string).

    $("#advSearch").advancedSearch("valUrl");


