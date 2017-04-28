#Instructions

oc secret new datasource-secret datasources.properties

oc process -f datavirt64-secure-demo-s2i.json -p HTTPS_NAME=jboss -p HTTPS_PASSWORD=mykeystorepass -p TEIID_USERNAME=tombrady -p TEIID_PASSWORD=Password1! | oc create -f -
