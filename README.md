## Starter for Spring MVC projects

This is a blank [Spring MVC](http://projects.spring.io/spring-framework/) project that will connect to any [prismic.io](https://prismic.io) repository, and trivially list its documents. It uses the prismic.io Java developement kit, and provide a few helpers to integrate with the Spring framework.

### Getting started

#### Launch the starter project

Assuming you've installed [Maven](http://maven.apache.org/download.cgi), just run ```mvn jetty:run```, and open your browser at http://localhost:8080/

Your Spring MVC starter project is now up and running! However, by default, it will list and display documents from our "[Les Bonnes Choses](http://lesbonneschoses.prismic.me)" example repository.

#### Configure the starter project

Edit the `web-context.xml` file to make the application point to the correct repository:

```
<!-- Prismic Config -->
<bean id="prismicConfig" class="io.prismic.starter.helper.PrismicConfig">
  <property name="apiEndpoint" value="https://lesbonneschoses.prismic.io/api" />
  <!-- <property name="accessToken" value="xxxxxx" /> -->
  <!-- <property name="clientId" value="xxxxxx" /> -->
  <!-- <property name="clientSecret" value="xxxxxx" /> -->
</bean>
```

To set up the OAuth configuration and interactive signin, go to the _Applications_ panel in your repository's settings, and create a new OAuth application. You simply have to fill in an application name and potentially the callback URL (`localhost` URLs are always authorized, so at development time you can omit to fill in the Callback URL field). After submitting, copy/paste the `clientId` & `clientSecret` tokens into the proper place in your configuration.

You may have to restart your Spring MVC server.


#### Get started with prismic.io

You can find out [how to get started with prismic.io](https://developers.prismic.io/documentation/UjBaQsuvzdIHvE4D/getting-started) on our [prismic.io developer's portal](https://developers.prismic.io/).

#### Understand the Java development kit

You'll find more information about how to use the development kit included in this starter project, by reading [its README file](https://github.com/prismicio/java-kit/blob/master/README.md).

### Contribute to the starter project

Contribution is open to all developer levels, read our "[Contribute to the official kits](https://developers.prismic.io/documentation/UszOeAEAANUlwFpp/contribute-to-the-official-kits)" documentation to learn more.

### Licence

This software is licensed under the Apache 2 license, quoted below.

Copyright 2013 Zengularity (http://www.zengularity.com).

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this project except in compliance with the License. You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0.

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.