# Example GitHub pages site hosting UKETD_DC xsd files

http://ethos.library.leeds.ac.uk/ethos-oai/2.0/uketd_dc.xsd

This site is designed to host schema files that were previously held at http://naca.central.cranfield.ac.uk/ethos-oai/
e.g. http://naca.central.cranfield.ac.uk/ethos-oai/2.0/uketd_dc.xsd

I've started setting the site up and atempting to validate the OAI-PMH outout of White Rose eTheses Online against this site.
In the example record below, this means changing `naca.central.cranfield.ac.uk` to `ethos.library.leeds.ac.uk`, although in places this doesn't appear to work wit the files as provided from te old site.

- the included dcterms file is old, and predates the addition of `accessRights` and `dateAccepted` elements.
- the path `...ethos-oai/terms/` for `uketdterms` causes validation errors. Updating this to `...ethos-oai/2.0/terms/` seems to work. 

## Existing output from an EPrints repository

```
<record>
  <header>
    <identifier>oai:etheses.whiterose.ac.uk:3</identifier>
    <datestamp>2014-03-07T11:21:15Z</datestamp>
    <setSpec>7374617475733D756E707562</setSpec>
    <setSpec>74797065733D746865736973</setSpec>
  </header>
  <metadata>
    <uketd_dc:uketddc xmlns:uketd_dc="http://naca.central.cranfield.ac.uk/ethos-oai/2.0/" xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:dcterms="http://purl.org/dc/terms/" xmlns:uketdterms="http://naca.central.cranfield.ac.uk/ethos-oai/terms/" xsi:schemaLocation="http://naca.central.cranfield.ac.uk/ethos-oai/2.0/ http://naca.central.cranfield.ac.uk/ethos-oai/2.0/uketd_dc.xsd" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <dc:title>The Causes and Implications of Microstructures in Glacial Sediments</dc:title>
      <dc:date>1998-07</dc:date>
      <dc:creator>Evans, Andrew John</dc:creator>
      <uketdterms:department>School of Geography (Leeds)</uketdterms:department>
      <dc:identifier>uk.bl.ethos.367930</dc:identifier>
      <dcterms:abstract>This thesis examines how microstructures in glaciogenic sediments reflect the processes... [snip] ... hydraulic conditions.</dcterms:abstract>
      <uketdterms:commercial>University of Leeds</uketdterms:commercial>
      <dcterms:issued>1998-07</dcterms:issued>
      <dc:type>Thesis</dc:type>
      <dcterms:isReferencedBy>https://etheses.whiterose.ac.uk/3/</dcterms:isReferencedBy>
      <dc:identifier xsi:type="dcterms:URI">https://etheses.whiterose.ac.uk/3/2/contents.pdf</dc:identifier>
      <dc:format>text</dc:format>
      <dc:language xsi:type="dcterms:ISO639-2">eng</dc:language>
      <dcterms:accessRights>public</dcterms:accessRights>
      <dc:identifier xsi:type="dcterms:URI">https://etheses.whiterose.ac.uk/3/3/evansa_wholethesis.pdf</dc:identifier>
      <dc:format>text</dc:format>
      <dc:language xsi:type="dcterms:ISO639-2">eng</dc:language>
      <dcterms:accessRights>public</dcterms:accessRights>
      <uketdterms:qualificationname>Ph.D</uketdterms:qualificationname>
      <uketdterms:qualificationlevel>doctoral</uketdterms:qualificationlevel>
      <uketdterms:institution>University of Leeds</uketdterms:institution>
    </uketd_dc:uketddc>
  </metadata>
</record>
```
