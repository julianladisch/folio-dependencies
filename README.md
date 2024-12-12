
`plugin` snippet for pom.xml to merge license names:

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
