# Incident Management for Large-scale Systems

[![Linter](https://github.com/phamquiluan/awesome-incident-management/actions/workflows/linter.yml/badge.svg)](https://github.com/phamquiluan/awesome-incident-management/actions/workflows/linter.yml)

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Big tech cloud incident status](#big-tech-cloud-incident-status)
- [Sample microservices systems](#sample-microservices-systems)
- [Dataset](#dataset)
- [Tools](#tools)
  - [Metrics](#metrics)
  - [Logs](#logs)
  - [Traces](#traces)
  - [Load generators](#load-generators)
- [Academia](#academia)
  - [Conferences and Journals](#conferences-and-journals)
  - [Paper](#paper)
  - [Researcher](#researcher)
- [Reading List](#reading-list)
- [Video](#video)
- [Others](#others)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Big tech cloud incident status

- [Azure Cloud - https://status.azure.com/en-us/status/history](https://status.azure.com/en-us/status/history)
- [IBM Cloud - https://cloud.ibm.com/status/incident-reports](https://cloud.ibm.com/status/incident-reports)
- [Google Cloud - https://status.cloud.google.com/summary](https://status.cloud.google.com/summary)
- [Google Cloud - https://www.google.com/appsstatus/dashboard/summary](https://www.google.com/appsstatus/dashboard/summary)
- [AWS Cloud - https://aws.amazon.com/premiumsupport/technology/pes/](https://aws.amazon.com/premiumsupport/technology/pes/)
- [Verica Open Incident Database](https://www.thevoid.community/)

# Sample microservices systems

- [Train Ticket @ Fudan University](https://github.com/FudanSELab/train-ticket) (40+ microservices)
- [Train Ticket @ Tsinghua University](https://github.com/lizeyan/train-ticket)
- [Online Boutique @ Google Cloud](https://github.com/GoogleCloudPlatform/microservices-demo) (10 microservices)
- [Sock Shop](https://github.com/microservices-demo) https://microservices-demo.github.io/

# Dataset

- https://github.com/logpai/loghub
- [Error logs produced by OpenStack.](https://figshare.com/articles/Failure_dataset/7732268/2)
- [Computer failure data repository.](https://www.usenix.org/cfdr)
- [A list of security log data.](http://www.secrepo.com)
- [Apache log files.](https://www.sec.gov/dera/data/edgar-log-file-data-set.html)
- [Toward generating a new intrusion detection dataset and intrusion traffic characterization.](https://www.researchgate.net/publication/322870768_Toward_Generating_a_New_Intrusion_Detection_Dataset_and_Intrusion_Traffic_Characterization)
- https://github.com/shaido987/alarm-rca
- https://github.com/huawei-noah/trustworthyAI/tree/master/gcastle
- https://github.com/alibaba/clusterdata
- https://github.com/Azure/AzurePublicDataset

# Tools

## Metrics

- https://prometheus.io/docs
- https://github.com/blue-yonder/tsfresh: Time-series feature extraction

## Logs

- https://github.com/logpai/loglizer
- ELK ([Elasticsearch](https://github.com/elastic/elasticsearch) + [Logstash](https://www.elastic.co/logstash/) + [Kibana](https://www.elastic.co/kibana/))
- EFK ([Elasticsearch](https://github.com/elastic/elasticsearch) + [Fluentd](https://www.fluentd.org/) + [Kibana](https://www.elastic.co/kibana/))
- https://github.com/grafana/loki

## Traces

- https://github.com/apache/skywalking
- https://github.com/jaegertracing/jaeger
- https://github.com/openzipkin/zipkin

## Load generators

- https://github.com/locustio/locust
- https://github.com/apache/jmeter

# Academia

## Conferences and Journals

- A\* Ranked Conference: [ICSE](https://dblp.uni-trier.de/db/conf/icse/index) | [FSE](https://dblp.uni-trier.de/db/conf/sigsoft/index) | [ASE](https://dblp.org/db/conf/kbse/index.html)
- A Ranked Conference: ICSME | ICPC | ESEM | RE | MSR | ISSTA | SANER | ICST | ISSRE
- Top Q1 Journal: [IEEE TSE](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=32)

[[Check Conference Rank](http://portal.core.edu.au/conf-ranks/)][[Check Journal Rank](https://www.scimagojr.com/journalrank.php)][[Check Paper Acceptance Status](https://dblp.org/)]

## Paper

- [2022 - Constructing Large-Scale Real-World Benchmark Datasets for AIOps](https://arxiv.org/abs/2208.03938)
- [ASE'22 - Graph based Incident Extraction and Diagnosis in Large-Scale Online Systems](https://dl.acm.org/doi/abs/10.1109/ASE51524.2021.9678746)
- [KDD'22 - Causal Inference-Based Root Cause Analysis for Online Service Systems with Intervention Recognition](https://dl.acm.org/doi/10.1145/3534678.3539041) [[Code]](https://github.com/NetManAIOps/CIRCA)
- [ISSRE'22 - Going through the Life Cycle of Faults in Clouds: Guidelines on Fault Handling](https://ieeexplore.ieee.org/document/9978764/) [[Code, Data]](https://github.com/IntelligentDDS/Post-mortems-Analysis)
- [CSUR'22 - A Survey on Deep Learning for Software Engineering](https://dl.acm.org/doi/abs/10.1145/3505243)
- [VLDB'22 - Diagnosing Root Causes of Intermittent Slow Queries in Cloud Databases.](https://dl.acm.org/doi/abs/10.14778/3389133.3389136)[[Code]](https://zenodo.org/record/6544901#.Y60s_tVBzP9)
- [ASE'22 - WOLFFI: A fault injection platform for learning AIOps models.](https://research.ibm.com/publications/wolffi-a-fault-injection-platform-for-learning-aiops-models)
- [FSE'22 - Actionable and interpretable fault localization for recurring failures in online service systems.](https://dl.acm.org/doi/abs/10.1145/3540250.3549092) [[Code]](https://github.com/NetManAIOps/DejaVu)
- [SIGOPS'22 - An Intelligent Framework for Timely, Accurate, and Comprehensive Cloud Incident Detection.](https://dl.acm.org/doi/abs/10.1145/3544497.3544499)
- [ICSE'21 - MicroHECL: High-efficient root cause localization in large-scale microservice systems.](https://ieeexplore.ieee.org/abstract/document/9402058/)
- [WWW'21 - MicroRank: End-to-End Latency Issue Localization with Extended Spectrum Analysis in Microservice Environments](https://dl.acm.org/doi/10.1145/3442381.3449905)
- [ICSOC'21 - Localization of Operational Faults in Cloud Applications by Mining Causal Dependencies in Logs Using Golden Signals.](https://link.springer.com/chapter/10.1007/978-3-030-76352-7_17)
- [CSUR'21 - A survey on automated log analysis for reliability engineering.](https://dl.acm.org/doi/pdf/10.1145/3460345)
- [ICSE'21 - Fast outage analysis of large-scale production clouds with service correlation mining.](https://ieeexplore.ieee.org/abstract/document/9402074/)
- [FSE'21 - Onion: Identifying Incident-Indicating Logs for Cloud Systems.](https://dl.acm.org/doi/abs/10.1145/3468264.3473919)
- [ISSRE'21 - Identifying Root-Cause Metrics for Incident Diagnosis in Online Service Systems.](https://doi.org/10.1109/ISSRE52982.2021.00022)
- [FSE'20 - Towards intelligent incident management: why we need it and how we make it.](https://dl.acm.org/doi/abs/10.1145/3368089.3417055)
- [2020 - Loghub: a large collection of system log datasets towards automated log analytics.](https://arxiv.org/abs/2008.06448) [[Code]](https://github.com/logpai/loghub)
- [FSE'20 - Graph-based trace analysis for microservice architecture understanding and problem diagnosis.](https://dl.acm.org/doi/abs/10.1145/3368089.3417066)
- [ICSE'19 - Tools and Benchmarks for Automated Log Parsing.](https://ieeexplore.ieee.org/abstract/document/8804456) [[Code]](https://github.com/logpai/logparser)
- [FSE'19 - Latent error prediction and fault localization for microservice applications by learning from system trace logs](http://dl.acm.org/citation.cfm?doid=3338906.3338961)
- [ISSRE'19 - FluxRank: A Widely-Deployable Framework to Automatically Localizing Root Cause Machines for Software Service Failure Mitigation.](https://ieeexplore.ieee.org/abstract/document/8987478)
- [FSE'18 - Identifying impactful service system problems via log analysis.](https://dl.acm.org/doi/abs/10.1145/3236024.3236083)
- [TNSM'2017 - Mining causality of network events in log data.](https://ieeexplore.ieee.org/abstract/document/8122062) [[Code]](https://github.com/cpflat/LogCausalAnalysis)

## Researcher

- [Assoc Prof. Hongyu Zhang - Newcastle University](https://sites.google.com/site/hongyujohn/) [[Google Scholar]](https://scholar.google.com/citations?user=zsUN6PkAAAAJ&hl=en&oi=ao)
- [Assoc Prof. Dan Pei - Tsinghua University](https://netman.aiops.org/~peidan/) [[Google Scholar]](https://scholar.google.com/citations?user=i_zA1VsAAAAJ&hl=en&oi=ao)
- [Prof. Tao Xie - Fudan University](https://taoxiease.github.io/) [[Google Scholar]](https://scholar.google.com/citations?user=DhhH9J4AAAAJ&hl=en&oi=ao)
- [Prof. Peng Xin - Fudan University](https://cspengxin.github.io/) [[Google Scholar]](https://scholar.google.com/citations?user=wATYGXEAAAAJ&hl=en&oi=ao)
- [Dr. Dongmei Zhang - Microsoft Asia Research](https://www.microsoft.com/en-us/research/people/dongmeiz/) [[Google Scholar]](https://scholar.google.com/citations?user=jLlBBl4AAAAJ&hl=en&oi=ao)
- [Qingwei Lin - Microsoft Research Asia](https://www.microsoft.com/en-us/research/people/qlin/publications/) [[Google Scholar]](https://scholar.google.com/citations?user=W9fdsxMAAAAJ&hl=en&oi=ao)

# Reading List

- [AWS Observability Recipes](https://aws-observability.github.io/aws-o11y-recipes/)
- [Monitoring the Golden Signals (Latency, Traffic, Errors, and Saturation)](https://www.slideshare.net/OpsStack/how-to-monitoring-the-sre-golden-signals-ebook)
- [Kibana vs Grafana](https://signoz.io/blog/kibana-vs-grafana/): **Kibana for logs, Grafana for metrics**, although both tools can use for aggregating metrics and logs. Kibana sticks with ELK (or EFK). Grafana goes with Loki and Prometheus.
- [Google SRE - Monitoring Distributed Systems](https://sre.google/sre-book/monitoring-distributed-systems/): Four golden signals of monitoring includes latency, traffic, errors, and saturation (How "full" your service is? It is about resource usages).
- [Computer Security Incident Handling Guide](https://nvlpubs.nist.gov/nistpubs/specialpublications/nist.sp.800-61r2.pdf)
- [CNCF Cloud Native Interactive Landscape](https://landscape.cncf.io/)

# Video

- [Adobe - The Good, the Bad and the Ugly: The 3 Learnings of an SRE](https://www.usenix.org/conference/srecon20americas/presentation/charagondla)
- [The Smallest Possible SRE Team](https://www.usenix.org/conference/srecon20americas/presentation/thomas)

# Others

- https://github.com/upgundecha/howtheysre
- https://github.com/dastergon/awesome-sre
- https://github.com/logpai/awesome-log-analysis
- https://github.com/yzhao062/anomaly-detection-resources
- https://github.com/hoya012/awesome-anomaly-detection
- https://github.com/adriannovegil/awesome-observability
- https://github.com/dastergon/awesome-chaos-engineering
- https://github.com/awesome-foss/awesome-sysadmin
