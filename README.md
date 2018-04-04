# VIVO Dependencies

Distribution of required dependencies not provided by Maven central

## Adding artefacts to this project

Create a Maven project, and include a deploy plugin configuration:

Note: <url> should point to the file location where this project has been cloned

<plugin>
	<artifactId>maven-deploy-plugin</artifactId>
	<executions>
		<execution>
			<id>install-agrovocws</id>
			<phase>validate</phase>
			<goals>
				<goal>deploy-file</goal>
			</goals>
			<configuration>
				<url>file:/[file location]/url>
				<file>[name of file in system]</file>
				<groupId>org.vivoweb.dependencies</groupId>
				<artifactId>[artifact name]</artifactId>
				<version>[artifact version]</version>
				<packaging>[format - usually jar]</packaging>
			</configuration>
		</execution>
	</executions>
</plugin>

Simply getting Maven to load the pom - e.g. mvn install - will cause the file to be deployed to the <url> location provided.

After "deployment", the project can be checked in to make available on GitHub.

# Licenses

## Apache License 2.0

csv

## BSD

sparqltag

## GNU LGPL 3

fedora-client

## JRL 1.5

jai_codec
jai_core

## ORCID API client

Written as part of the ORCID A&I grant. Source is available at https://github.com/j2blake/orcid-api-client
