# Blank Maven skin

Blank Maven skin renders the Maven site pages without any additional skinning or decoration.
It only outputs the contents of each page.

The skin uses short title as output's `<title>` tag. If one is not available, tries to derive
it from the first `<h1>` header in the content.

## Usage

To use this Maven skin, include it in your `site.xml` file:

```xml
<project>
  ...
  <skin>
    <groupId>lt.velykis.maven.skins</groupId>
    <artifactId>blank-maven-skin</artifactId>
    <version>1.0.0</version>
  </skin>
  ...
</project>
```

The skin requires Velocity >= 1.7 when generating Maven site.
Add it as a dependency to `maven-site-plugin` in your POM file:

```xml
<build>
  <plugins>
    ...
    <plugin>
      <groupId>org.apache.maven.plugins</groupId>
      <artifactId>maven-site-plugin</artifactId>
      <version>3.2</version>
      <dependencies>
        ...
        <!-- Blank skin requires Velocity >= 1.7  -->
        <dependency>
          <groupId>org.apache.velocity</groupId>
          <artifactId>velocity</artifactId>
          <version>1.7</version>
        </dependency>
        ...
      </dependencies>
      ...
    </plugin>
    ...
  </plugins>
</build>
```

## Bug tracker

Have a bug or a feature request? Please create an issue here on GitHub that conforms with
[necolas's guidelines](http://github.com/necolas/issue-guidelines).

http://github.com/andriusvelykis/blank-maven-skin/issues


## Contributing

Fork the repository and submit pull requests.


## Author

**Andrius Velykis**

+ http://andrius.velykis.lt
+ http://github.com/andriusvelykis



## Copyright and license

Copyright 2013 Andrius Velykis

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this work except in compliance with the License.
You may obtain a copy of the License in the LICENSE file, or at:

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
