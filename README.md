# Incident Management for Large-scale Systems

[![Linter](https://github.com/phamquiluan/awesome-incident-management/actions/workflows/linter.yml/badge.svg)](https://github.com/phamquiluan/awesome-incident-management/actions/workflows/linter.yml)

- [Public Resource](#public-resource)
  - [Big tech cloud incident status](#big-tech-cloud-incident-status)
  - [Github](#github)
  - [Sample microservices systems](#sample-microservices-systems)
  - [Dataset](#dataset)
  - [Other](#other)
- [Academic Conferences and Journals](#academic-conferences-and-journals)
- [Academic Paper](#academic-paper)
- [Academic Researcher](#academic-researcher)
- [Reading List](#reading-list)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

# Public Resource

## Big tech cloud incident status

- [Azure Cloud - https://status.azure.com/en-us/status/history](https://status.azure.com/en-us/status/history)
- [IBM Cloud - https://cloud.ibm.com/status/incident-reports](https://cloud.ibm.com/status/incident-reports)
- [Google Cloud - https://status.cloud.google.com/summary](https://status.cloud.google.com/summary)
- [Google Cloud - https://www.google.com/appsstatus/dashboard/summary](https://www.google.com/appsstatus/dashboard/summary)
- [AWS Cloud - https://aws.amazon.com/premiumsupport/technology/pes/](https://aws.amazon.com/premiumsupport/technology/pes/)

## Github

- https://github.com/upgundecha/howtheysre
- https://github.com/dastergon/awesome-sre
- https://github.com/logpai/awesome-log-analysis
- https://github.com/yzhao062/anomaly-detection-resources
- https://github.com/hoya012/awesome-anomaly-detection
- https://github.com/topics/incident-management
- https://github.com/topics/incident-response
- https://github.com/NetManAIOps

## Sample microservices systems

- [Train Ticket @ Fudan University](https://github.com/FudanSELab/train-ticket) (40+ microservices)
- [Train Ticket @ Tsinghua University](https://github.com/lizeyan/train-ticket)
- [Online Boutique @ Google Cloud](https://github.com/GoogleCloudPlatform/microservices-demo) (10 microservices)
- [Sock Shop](https://github.com/microservices-demo) https://microservices-demo.github.io/

## Dataset

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

## Other

- [Computer Security Incident Handling Guide](https://nvlpubs.nist.gov/nistpubs/specialpublications/nist.sp.800-61r2.pdf)
- [CNCF Cloud Native Interactive Landscape](https://landscape.cncf.io/)

# Academic Conferences and Journals

- A\* Ranked Conference: [ICSE](https://dblp.uni-trier.de/db/conf/icse/index) | [FSE](https://dblp.uni-trier.de/db/conf/sigsoft/index) | [ASE](https://dblp.org/db/conf/kbse/index.html)
- A Ranked Conference: ICSME | ICPC | ESEM | RE | MSR | ISSTA | SANER | ICST | ISSRE
- Top Q1 Journal: [IEEE TSE](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=32)

[[Check Conference Rank](http://portal.core.edu.au/conf-ranks/)][[Check Journal Rank](https://www.scimagojr.com/journalrank.php)][[Check Paper Acceptance Status](https://dblp.org/)]

# Academic Paper

- [2022 - Constructing Large-Scale Real-World Benchmark Datasets for AIOps](https://arxiv.org/abs/2208.03938)
- [2022 - Graph based Incident Extraction and Diagnosis in Large-Scale Online Systems](https://dl.acm.org/doi/abs/10.1109/ASE51524.2021.9678746)
- [2022 - Causal Inference-Based Root Cause Analysis for Online Service Systems with Intervention Recognition](https://dl.acm.org/doi/10.1145/3534678.3539041) [[Code]](https://github.com/NetManAIOps/CIRCA)
- [2022 - Going through the Life Cycle of Faults in Clouds: Guidelines on Fault Handling](https://ieeexplore.ieee.org/document/9978764/) [[Code, Data]](https://github.com/IntelligentDDS/Post-mortems-Analysis)
- [2022 - A Survey on Deep Learning for Software Engineering](https://dl.acm.org/doi/abs/10.1145/3505243)
- [2022 - Diagnosing Root Causes of Intermittent Slow Queries in Cloud Databases.](https://dl.acm.org/doi/abs/10.14778/3389133.3389136)[[Code]](https://zenodo.org/record/6544901#.Y60s_tVBzP9)
- [2022 - WOLFFI: A fault injection platform for learning AIOps models.](https://research.ibm.com/publications/wolffi-a-fault-injection-platform-for-learning-aiops-models)
- [2022 - Actionable and interpretable fault localization for recurring failures in online service systems.](https://dl.acm.org/doi/abs/10.1145/3540250.3549092) [[Code]](https://github.com/NetManAIOps/DejaVu)
- [2022 - An Intelligent Framework for Timely, Accurate, and Comprehensive Cloud Incident Detection.](https://dl.acm.org/doi/abs/10.1145/3544497.3544499)
- [2021 - MicroHECL: High-efficient root cause localization in large-scale microservice systems.](https://ieeexplore.ieee.org/abstract/document/9402058/)
- [2021 - MicroRank: End-to-End Latency Issue Localization with Extended Spectrum Analysis in Microservice Environments](https://dl.acm.org/doi/10.1145/3442381.3449905)
- [2021 - Localization of Operational Faults in Cloud Applications by Mining Causal Dependencies in Logs Using Golden Signals.](https://link.springer.com/chapter/10.1007/978-3-030-76352-7_17)
- [2021 - A survey on automated log analysis for reliability engineering.](https://dl.acm.org/doi/pdf/10.1145/3460345)
- [2021 - Fast outage analysis of large-scale production clouds with service correlation mining.](https://ieeexplore.ieee.org/abstract/document/9402074/)
- [2021 - Onion: Identifying Incident-Indicating Logs for Cloud Systems.](https://dl.acm.org/doi/abs/10.1145/3468264.3473919)
- [2021 - Identifying Root-Cause Metrics for Incident Diagnosis in Online Service Systems.](https://doi.org/10.1109/ISSRE52982.2021.00022)
- [2020 - Towards intelligent incident management: why we need it and how we make it.](https://dl.acm.org/doi/abs/10.1145/3368089.3417055)
- [2020 - Loghub: a large collection of system log datasets towards automated log analytics.](https://arxiv.org/abs/2008.06448) [[Code]](https://github.com/logpai/loghub)
- [2020 - Graph-based trace analysis for microservice architecture understanding and problem diagnosis.](https://dl.acm.org/doi/abs/10.1145/3368089.3417066)
- [2019 - Tools and Benchmarks for Automated Log Parsing.](https://ieeexplore.ieee.org/abstract/document/8804456) [[Code]](https://github.com/logpai/logparser)
- [2019 - Latent error prediction and fault localization for microservice applications by learning from system trace logs](http://dl.acm.org/citation.cfm?doid=3338906.3338961)
- [2019 - FluxRank: A Widely-Deployable Framework to Automatically Localizing Root Cause Machines for Software Service Failure Mitigation.](https://ieeexplore.ieee.org/abstract/document/8987478)
- [2018 - Identifying impactful service system problems via log analysis.](https://dl.acm.org/doi/abs/10.1145/3236024.3236083)
- [2017 - Mining causality of network events in log data.](https://ieeexplore.ieee.org/abstract/document/8122062) [[Code]](https://github.com/cpflat/LogCausalAnalysis)

# Academic Researcher

- [Assoc Prof. Hongyu Zhang - Newcastle University](https://sites.google.com/site/hongyujohn/) [[Google Scholar]](https://scholar.google.com/citations?user=zsUN6PkAAAAJ&hl=en&oi=ao)
- [Assoc Prof. Dan Pei - Tsinghua University](https://netman.aiops.org/~peidan/) [[Google Scholar]](https://scholar.google.com/citations?user=i_zA1VsAAAAJ&hl=en&oi=ao)
- [Prof. Tao Xie - Fudan University](https://taoxiease.github.io/) [[Google Scholar]](https://scholar.google.com/citations?user=DhhH9J4AAAAJ&hl=en&oi=ao)
- [Prof. Peng Xin - Fudan University](https://cspengxin.github.io/) [[Google Scholar]](https://scholar.google.com/citations?user=wATYGXEAAAAJ&hl=en&oi=ao)
- [Dr. Dongmei Zhang - Microsoft Asia Research](https://www.microsoft.com/en-us/research/people/dongmeiz/) [[Google Scholar]](https://scholar.google.com/citations?user=jLlBBl4AAAAJ&hl=en&oi=ao)
- [Qingwei Lin - Microsoft Research Asia](https://www.microsoft.com/en-us/research/people/qlin/publications/) [[Google Scholar]](https://scholar.google.com/citations?user=W9fdsxMAAAAJ&hl=en&oi=ao)

# Reading List

- [Kibana vs Grafana](https://signoz.io/blog/kibana-vs-grafana/): **Kibana for logs, Grafana for metrics**, although both tools can use for aggregating metrics and logs. Kibana sticks with ELK (or EFK). Grafana goes with Loki and Prometheus.
- [Google SRE - Monitoring Distributed Systems](https://sre.google/sre-book/monitoring-distributed-systems/): Four golden signals of monitoring includes latency, traffic, errors, and saturation (How "full" your service is? It is about resource usages).
