# GSoC 2020: Add support for the template() syntax in the topic parameter of kafka destination

## General Info


* Name: Vivin Flawence Peris


* Github: [vivin-peris](https://github.com/vivinperis/)


* Email: vivinperis98@gmail.com


* Organization: [Syslog-ng](https://github.com/syslog-ng/syslog-ng)


* Mentors: [Balazs Scheidler](https://github.com/bazsi) and
           [Attila Szakacs](https://github.com/alltilla)


* Draft Proposal: [Add support for the template() syntax in the kafka() destination](https://github.com/syslog-ng/syslog-ng/wiki/GSoC-2020-Proposal-:-Add-support-for-the-template()-syntax-in-the-kafka()-destination-in-C-based-implementation(vivinperis))


## Project overview


Syslog-ng is a highly scalable logging application, which is used collect logs from various sources on a centralized log server and allows to process them with parsers, filters, and specialized modules before sending them to various destinations. 
The project involved implementation of template() syntax in the librdkafka based implementation of Kafka destination.


## Project Abstract

The project involved adding support for template() syntax in the topic() parameter of librdkafka based implementation of Kafka destination as earlier available in earlier Java-based Kafka destination. Along with this, the patch freatures a fallback_topic() which would be useful in cases where expanded template topic name is invalid and thus ensure that no log messages are lost. Also, the topic name for a literal string is validated at the driver to ensure that the topic name is valid. Incase of template topic name, the fallback_topic() is validated to make sure it is a valid topic name. Inorder to test the functionality of the patch, unit tests have been added.


## Tasks involved

* Change in grammar and parser to include fallback_topic() and convert topic() into template type.

* Refactoring changes in the driver to support template and non template cases.

* Validation function to check if the topic name is valid or not.

* Changes at the worker threads to account for literal and template topic name

* Unit tests to test the validate and calculate topic methods.

* Created an internal header file for access to methods required for unit test.

* Test for memory leaks using Valgrind.

## Link to PR(merged) : [PR#3372](https://github.com/syslog-ng/syslog-ng/pull/3372/files)
 
## Link to documentation : [GSoC2020-Documentation](https://docs.google.com/document/d/1U04Xd2DjfWwE25eGErGXVkB5rR-bbBLvdobvXG4KsPQ/edit)
