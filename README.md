# Imixs-Workflow - Maven Skins

This project provides some Maven Site Skins used in the Imixs Workflow Project

## Build 

To build current version run:

	$ mvn clean install

	
## Integration

To use a skin in your project add the following settings to the parent pom.xml
	
	
	
	<build>
		<plugins>
			...
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-site-plugin</artifactId>
				<version>3.9.0</version>
			</plugin>
	....
	<reporting>
		<plugins>
			<!-- java doc -->
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-javadoc-plugin</artifactId>
				<version>3.2.0</version>
				<configuration>
					<additionalOptions>-Xdoclint:none</additionalOptions>
				</configuration>
			</plugin>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-jxr-plugin</artifactId>
				<version>3.0.0</version>
			</plugin>
		</plugins>
	</reporting>
	...


Than create a `site.xml` in your /src folder with at least the following entry:

	<?xml version="1.0" encoding="ISO-8859-1"?>
	<project name="Imixs Open Source Workflow">
	
		<skin>
			<groupId>org.imixs.workflow</groupId>
			<artifactId>imixs-workflow-skin</artifactId>
			<version>1.0.0</version>
		</skin>
		.....
		
	

	