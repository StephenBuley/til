# Formats for Liquibase changelogs

We are looking at moving over to liquibase for database change management, and I understood that the format of the changelog files needed to be very specific. I was wrong - you can use SQL, XML, YAML, or JSON for free, Mongo (paid? hard to tell) or wrappers for other languages such as Groovy or Clojure.

SQL to me seems by far the most straightforward, but then you are using db vendor specific language rather than something more indirect like XML, YAML, or JSON definitions, so definitely a tradeoff there.
