# GSoC 2020: Support template syntax for Syslog-ng's Kafka Destination topic name

## General Info


* Name: Vivin Flawence Peris


* Github: [vivin-peris](https://github.com/vivinperis/)


* Email: vivinperis98@gmail.com


* Organization: [Syslog-ng](https://github.com/syslog-ng/syslog-ng)


* Mentor: [Balazs Scheidler](https://github.com/bazsi)


* Draft Proposal: [Add support for the template() syntax in the kafka() destination](https://github.com/syslog-ng/syslog-ng/wiki/GSoC-2020-Proposal-:-Add-support-for-the-template()-syntax-in-the-kafka()-destination-in-C-based-implementation(vivinperis))


## Project overview


Syslog-ng is a highly scalable logging application, which is used collect logs from various sources on a centralized log server and allows to process them with parsers, filters, and specialized modules before sending them to various destinations. 
The project involved implementation of template() syntax in the librdkafka based implementation of Kafka destination.


## Project Abstract

The librdkafka based implementation of Kafka destination doesn't support template() syntax for Kafka topic, which was earlier available in earlier Java-based Kafka destination. The GSoC project involved support for the same and introduction of a fallback topic in cases where expanded template topic name is invalid, which would ensure that no log messages are lost. Also, added unit tests to ensure that the functions work as intended.

## Link to PR(merged) : [PR#3372](https://github.com/syslog-ng/syslog-ng/pull/3372/files)
 
## Link to documentation : [GSoC2020-Documentation](https://docs.google.com/document/d/1U04Xd2DjfWwE25eGErGXVkB5rR-bbBLvdobvXG4KsPQ/edit)
