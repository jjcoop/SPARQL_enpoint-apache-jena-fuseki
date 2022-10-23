# SPARQL_enpoint-apache-jena-fuseki
 Owl ontologies representing the Schwarts Human values mapped with the GDPR rights and principles.

## The Binaries were downloaded at the [jena](https://jena.apache.org/documentation/archive/serving_data/fuseki1.html) website.
I have simply uploaded some owl documents in order to run queries on them using the SPARQL enpoint. 

## Get the server started

### Linux Commands
``` bash
chmod +x fuseki-server bin/s-*
./fuseki-server –update –mem /ds
```

### Windows
1. click on the *fuseki-server* windows batch file located in the root of the project directoy.

## Visit the control panel
```uri
http://localhost:3030/
```

## Query the Endpoint
```SQL
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>

SELECT DISTINCT ?class ?label ?description
WHERE {
  ?class a owl:Class.
  OPTIONAL { ?class rdfs:label ?label}
  OPTIONAL { ?class rdfs:comment ?description}
}
LIMIT 25
```

```csv
"class","label","description"
"http://www.semanticweb.org/jjc836/ontologies/2022/9/human-values#Value_Item",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/human-values#Values",,
"http://dbpedia.org/resource/Theory_of_Basic_Human_Values",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/human-values#Human",,
"http://dbpedia.org/resource/Shalom_H._Schwartz",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/human-values#achievement",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/human-values#benevolence",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/human-values#conformity",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/human-values#face",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/human-values#hedonism",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/human-values#humility",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/human-values#power",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/human-values#security",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/human-values#self_direction",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/human-values#stimulation",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/human-values#tradition",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/human-values#universalism",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/GDPR-ontology#Sub_Provision",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/GDPR-ontology#Data_Protection_Principles",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/GDPR-ontology#Data_Subject_Rights",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/GDPR-ontology#Accuracy",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/GDPR-ontology#Data_Minimization",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/GDPR-ontology#Fairness",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/GDPR-ontology#Integrity_and_Confidentiality",,
"http://www.semanticweb.org/jjc836/ontologies/2022/9/GDPR-ontology#Lawfulness",,
```