# nuxeo-unique-title-validator

This Nuxeo plugin implements how validate unique titles, it means, user only can create unique titles. It must be used from another plugin (the one you are developing).

Code Example

Use it in your contribution (extensions.xml):

    <widget name="Expedient Number" type="text">
        <labels>
            <label mode="any">label.ExpedientNumber</label>
        </labels>
        <translated>true</translated>
        <fields>
            <field>dc:title</field>
        </fields>
        <properties WidgetMode="edit">
            <property name="validator">#{AthentoValidatorTitle.validateuniquetitle}</property>
        </properties>
    </widget>
    
    
    Motivation

It's very usefull to have a feature that it don't allow to create documents with same title

Installation

You just have to compile the pom.xml using Maven and deploy the plugin in

cd nuxeo-unique-title-validator
mvn clean install
cp target/athento-nx-validator-title.*.jar $NUXEO_HOME/nxserver/plugins
And then, restart your nuxeo server and enjoy.
