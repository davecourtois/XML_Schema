# XML_Schema

## Desctiption

A complete XSD (XML Schema) parser to parse any schema. XML schema 

## usage

Simply import the package in your application and use it like regular XML file.

~~~
package main

import (
	"encoding/xml"
	"github.davecourtois/XML_Schema"
)

/**
 * Read the content of XSD file.
 */
func ReadXSD(reader io.Reader) (*XML_Schema.XSD_Schema, error) {
	var doc *XML_Schema.XSD_Schema
	doc = new(XML_Schema.XSD_Schema)
	if err := xml.NewDecoder(reader).Decode(doc); err != nil {
		return nil, err
	}

	return doc, nil
}
~~~

That's it!-)
