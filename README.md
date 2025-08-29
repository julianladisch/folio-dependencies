How to generate the HTML page for a maven project:

Optionally add this `plugin` snippet into the pom.xml if you want some license names being merged:

```
      <plugin>
        <artifactId>maven-project-info-reports-plugin</artifactId>
        <configuration>
          <licenseMappings>
            <licenseMapping>
              <froms>
                <from>The Apache Software License, Version 2.0</from>
                <from>Apache Public License 2.0</from>
                <from>Apache 2</from>
                <from>Apache-2.0</from>
                <from>Apache License, 2.0</from>
                <from>Apache Software License, version 2.0</from>
                <from>Apache 2.0</from>
                <from>The Apache License, Version 2.0</from>
                <from>Apache License 2.0</from>
              </froms>
              <to>Apache License, Version 2.0</to>
            </licenseMapping>
            <licenseMapping>
              <froms>
                <from>MIT License</from>
                <from>The MIT License</from>
                <from>MIT license</from>
                <from>The MIT License (MIT)</from>
              </froms>
              <to>MIT</to>
            </licenseMapping>
          </licenseMappings>
        </configuration>
      </plugin>
```

Then run `mvn clean project-info-reports:dependencies` and copy `target/reports/dependencies.html`
into this repository and rename it so that the file name contains module name and version.

Add an entry for it to `index.html`.

This repository has GitHub Pages configured to automatically deploy it from the root directory of the `main` branch.
