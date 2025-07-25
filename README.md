# Awesome Failure Diagnosis for Software Systems

[![Linter](https://github.com/phamquiluan/awesome-incident-management/actions/workflows/linter.yml/badge.svg)](https://github.com/phamquiluan/awesome-incident-management/actions/workflows/linter.yml)

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Reading](#reading)
  - [Anomaly Detection](#anomaly-detection)
  - [Root Cause Analysis / Fault Localization](#root-cause-analysis--fault-localization)
  - [Others Paper](#others-paper)
  - [Misc](#misc)
- [Big tech cloud incident status](#big-tech-cloud-incident-status)
- [Benchmark & Microservices Systems](#benchmark--microservices-systems)
- [Dataset](#dataset)
- [Tools](#tools)
  - [Metrics](#metrics)
  - [Logs](#logs)
  - [Traces](#traces)
  - [Load generators](#load-generators)
  - [Chaos Engineering / Fault Injection](#chaos-engineering--fault-injection)
- [Academia](#academia)
  - [Conferences and Journals](#conferences-and-journals)
  - [Researcher](#researcher)
- [Video](#video)
- [Others](#others)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Reading

## Anomaly Detection

- [UAC-AD: Unsupervised Adversarial Contrastive Learning for Anomaly Detection on Multi-modal Data in Microservice Systems](https://ieeexplore.ieee.org/abstract/document/10552111) [[Code]](https://github.com/lhysgithub/UAC-AD)
- [Robust multimodal failure detection for microservice systems](https://dl.acm.org/doi/pdf/10.1145/3580305.3599902) [[Code]](https://github.com/AIOps-Lab-NKU/AnoFusion)
- [ICSE'23 - Eadro: An End-to-End Troubleshooting Framework for Microservices on Multi-source Data](https://arxiv.org/abs/2302.05092) [[Code]](https://github.com/BEbillionaireUSD/Eadro)
- [ICSE'21 - Log-based Anomaly Detection with Deep Learning: How Far Are We?](https://dl.acm.org/doi/10.1145/3510003.3510155) [[Code]](https://github.com/LogIntelligence/LogADEmpirical)
- [IPCCC'18 - Rapid deployment of anomaly detection models for large number of emerging kpi streams](https://ieeexplore.ieee.org/document/8711315)
- [IMC'15 - Opprentice: Towards practical and automatic anomaly detection through machine learning.](https://ieeexplore.ieee.org/document/8711315)
- [ATC'21 - {Jump-Starting} Multivariate Time Series Anomaly Detection for Online Service Systems](https://www.usenix.org/conference/atc21/presentation/ma)
- [WWW'18 - Unsupervised Anomaly Detection via Variational Auto-Encoder for Seasonal KPIs in Web Applications.](https://dl.acm.org/doi/10.1145/3178876.3185996)
- [CCS'17 - DeepLog: Anomaly Detection and Diagnosis from System Logs through Deep Learning](https://dl.acm.org/doi/10.1145/3133956.3134015)
- [ICSE'16 - Behavioral Log Analysis with Statistical Guarantees](https://ieeexplore.ieee.org/document/7886964/)
- [TKDE'04 - Workflow Mining: Discovering Process Models from Event Logs](https://ieeexplore.ieee.org/document/1316839/)

## Root Cause Analysis / Fault Localization

- [WWW'25 - RCAEval: A Benchmark for Root Cause Analysis of Microservice Systems with Telemetry Data](https://arxiv.org/abs/2412.17015) [[Code]](https://github.com/phamquiluan/rcaeval/)
- [ICLR'25 - Robust Root Cause Diagnosis using In-Distribution Interventions](https://openreview.net/pdf?id=l11DZY5Nxu)
- [ICLR'25 - OpenRCA: Can Large Language Models Locate the Root Cause of Software Failures?](https://github.com/microsoft/OpenRCA)
- [2025 - LEMMA-RCA: A Large Multi-modal Multi-domain Dataset for Root Cause Analysis](https://openreview.net/forum?id=0R8JUzjSdq)
- [ASE'24 - Root Cause Analysis for Microservice System based on Causal Inference: How Far Are We?](https://conf.researchr.org/details/ase-2024/ase-2024-research/57/Root-Cause-Analysis-for-Microservice-System-based-on-Causal-Inference-How-Far-Are-We) [[Code]](https://github.com/phamquiluan/rcaeval/)
- [FSE'24 - BARO: Robust Root Cause Analysis for Microservices via Multivariate Bayesian Online Change Point Detection](https://2024.esec-fse.org/details/fse-2024-research-papers/81/BARO-Robust-Root-Cause-Analysis-for-Microservices-via-Multivariate-Bayesian-Online-C) [[Code]](https://github.com/phamquiluan/baro/)
- [TSE'24 - TrinityRCL: Multi-Granular and Code-Level Root Cause Localization Using Multiple Types of Telemetry Data in Microservice Systems](https://ieeexplore.ieee.org/document/10034937)
- [HeMiRCA: Fine-Grained Root Cause Analysis for Microservices with Heterogeneous Data Sources](https://dl.acm.org/doi/pdf/10.1145/3674726) [[Code]](https://github.com/Zhuzrx/HeMiRCA/)
- [ASE'24 - Giving Every Modality a Voice in Microservice Failure Diagnosis via Multimodal Adaptive Optimization](https://conf.researchr.org/details/ase-2024/ase-2024-research/89/Giving-Every-Modality-a-Voice-in-Microservice-Failure-Diagnosis-via-Multimodal-Adapti)
- [ASE'24 - MRCA: Metric-level Root Cause Analysis for Microservices via Multi-Modal Data](https://conf.researchr.org/details/ase-2024/ase-2024-research/85/MRCA-Metric-level-Root-Cause-Analysis-for-Microservices-via-Multi-Modal-Data)
- [SIGCOMM'23 - Network-centric distributed tracing with deepflow: Troubleshooting your microservices in zero code](https://dl.acm.org/doi/abs/10.1145/3603269.3604823) [[Code]](https://github.com/deepflowio/deepflow)
- [FSE'23 - Nezha: Interpretable Fine-Grained Root Causes Analysis for Microservices on Multi-modal Observability Data](https://dl.acm.org/doi/abs/10.1145/3611643.3616249) [[Code]](https://github.com/IntelligentDDS/Nezha)
- [ICSE'23 - Eadro: An End-to-End Troubleshooting Framework for Microservices on Multi-source Data](https://arxiv.org/abs/2302.05092) [[Code]](https://github.com/BEbillionaireUSD/Eadro)
- [NeuIPS'22 - Root Cause Discovery: Root Cause Analysis of Failures in Microservices through Causal Discovery](https://openreview.net/forum?id=weoLjoYFvXY) [[Code]](https://github.com/azamikram/rcd)
- [KDD'22 - Causal Inference-Based Root Cause Analysis for Online Service Systems with Intervention Recognition](https://dl.acm.org/doi/10.1145/3534678.3539041) [[Code]](https://github.com/NetManAIOps/CIRCA)
- [VLDB'22 - Diagnosing Root Causes of Intermittent Slow Queries in Cloud Databases.](https://dl.acm.org/doi/abs/10.14778/3389133.3389136)[[Code]](https://zenodo.org/record/6544901#.Y60s_tVBzP9)
- [FSE'22 - Actionable and interpretable fault localization for recurring failures in online service systems.](https://dl.acm.org/doi/abs/10.1145/3540250.3549092) [[Code]](https://github.com/NetManAIOps/DejaVu)
- [ICSE'21 - MicroHECL: High-efficient root cause localization in large-scale microservice systems.](https://ieeexplore.ieee.org/abstract/document/9402058/)
- [ISSRE'21 - Identifying Root-Cause Metrics for Incident Diagnosis in Online Service Systems.](https://doi.org/10.1109/ISSRE52982.2021.00022)
- [FSE'20 - Graph-based trace analysis for microservice architecture understanding and problem diagnosis.](https://dl.acm.org/doi/abs/10.1145/3368089.3417066)
- [FSE'19 - Latent error prediction and fault localization for microservice applications by learning from system trace logs](http://dl.acm.org/citation.cfm?doid=3338906.3338961)
- [ISSRE'19 - FluxRank: A Widely-Deployable Framework to Automatically Localizing Root Cause Machines for Software Service Failure Mitigation.](https://ieeexplore.ieee.org/abstract/document/8987478)

## Others Paper

- [WWW'25 - RCAEval: A Benchmark for Root Cause Analysis of Microservice Systems with Telemetry Data](https://arxiv.org/abs/2412.17015) [[Code]](https://github.com/phamquiluan/rcaeval/)
- [SANER'25 - AIOpsArena: Scenario-Oriented Evaluation and Leaderboard for AIOps Algorithms in Microservices](https://nkcs.iops.ai/wp-content/uploads/2025/01/AIOpsArena.pdf)
- [2025 - AIOpsLab: A Holistic Framework to Evaluate AI Agents for Enabling Autonomous Clouds](#)
- [2024 - A Comprehensive Survey on Root Cause Analysis in (Micro) Services: Methodologies, Challenges, and Trends](https://www.arxiv.org/abs/2408.00803)
- [2024 - Failure Diagnosis in Microservice Systems: A Comprehensive Survey and Analysis](https://arxiv.org/pdf/2407.01710)
- [2022 - Constructing Large-Scale Real-World Benchmark Datasets for AIOps](https://arxiv.org/abs/2208.03938)
- [ASE'22 - Graph based Incident Extraction and Diagnosis in Large-Scale Online Systems](https://dl.acm.org/doi/abs/10.1109/ASE51524.2021.9678746)
- [ISSRE'22 - Going through the Life Cycle of Faults in Clouds: Guidelines on Fault Handling](https://ieeexplore.ieee.org/document/9978764/) [[Code, Data]](https://github.com/IntelligentDDS/Post-mortems-Analysis)
- [CSUR'22 - A Survey on Deep Learning for Software Engineering](https://dl.acm.org/doi/abs/10.1145/3505243)
- [ASE'22 - WOLFFI: A fault injection platform for learning AIOps models.](https://research.ibm.com/publications/wolffi-a-fault-injection-platform-for-learning-aiops-models)
- [SIGOPS'22 - An Intelligent Framework for Timely, Accurate, and Comprehensive Cloud Incident Detection.](https://dl.acm.org/doi/abs/10.1145/3544497.3544499)
- [WWW'21 - MicroRank: End-to-End Latency Issue Localization with Extended Spectrum Analysis in Microservice Environments](https://dl.acm.org/doi/10.1145/3442381.3449905)
- [ICSOC'21 - Localization of Operational Faults in Cloud Applications by Mining Causal Dependencies in Logs Using Golden Signals.](https://link.springer.com/chapter/10.1007/978-3-030-76352-7_17)
- [CSUR'21 - A survey on automated log analysis for reliability engineering.](https://dl.acm.org/doi/pdf/10.1145/3460345)
- [ICSE'21 - Fast outage analysis of large-scale production clouds with service correlation mining.](https://ieeexplore.ieee.org/abstract/document/9402074/)
- [FSE'21 - Onion: Identifying Incident-Indicating Logs for Cloud Systems.](https://dl.acm.org/doi/abs/10.1145/3468264.3473919)
- [FSE'20 - Towards intelligent incident management: why we need it and how we make it.](https://dl.acm.org/doi/abs/10.1145/3368089.3417055)
- [2020 - Loghub: a large collection of system log datasets towards automated log analytics.](https://arxiv.org/abs/2008.06448) [[Code]](https://github.com/logpai/loghub)
- [ICSE'19 - Tools and Benchmarks for Automated Log Parsing.](https://ieeexplore.ieee.org/abstract/document/8804456) [[Code]](https://github.com/logpai/logparser)
- [FSE'18 - Identifying impactful service system problems via log analysis.](https://dl.acm.org/doi/abs/10.1145/3236024.3236083)
- [TNSM'2017 - Mining causality of network events in log data.](https://ieeexplore.ieee.org/abstract/document/8122062) [[Code]](https://github.com/cpflat/LogCausalAnalysis)

## Misc

- [Datadog Incident Management](https://www.datadoghq.com/blog/tag/incident-management/)
- [Introducing Bits AI, your new DevOps copilot](https://www.datadoghq.com/blog/datadog-bits-generative-ai/)
- [AWS Observability Recipes](https://aws-observability.github.io/aws-o11y-recipes/)
- [Monitoring the Golden Signals (Latency, Traffic, Errors, and Saturation)](https://www.slideshare.net/OpsStack/how-to-monitoring-the-sre-golden-signals-ebook)
- [Kibana vs Grafana](https://signoz.io/blog/kibana-vs-grafana/): **Kibana for logs, Grafana for metrics**, although both tools can use for aggregating metrics and logs. Kibana sticks with ELK (or EFK). Grafana goes with Loki and Prometheus.
- [Google SRE - Monitoring Distributed Systems](https://sre.google/sre-book/monitoring-distributed-systems/): Four golden signals of monitoring includes latency, traffic, errors, and saturation (How "full" your service is? It is about resource usages).
- [Computer Security Incident Handling Guide](https://nvlpubs.nist.gov/nistpubs/specialpublications/nist.sp.800-61r2.pdf)
- [CNCF Cloud Native Interactive Landscape](https://landscape.cncf.io/)
- [Inside Azure Search: Chaos Engineering](https://azure.microsoft.com/en-us/blog/inside-azure-search-chaos-engineering/): Chaos engineering is the practice of intentionally introducing controlled failures and disruptions into a system to test its resilience and identify potential vulnerabilities.
- https://learn.microsoft.com/en-us/azure/azure-monitor/
- https://cloud.google.com/monitoring/docs/apis
- https://github.com/mooselab/DevOpsDataCollection

# Big tech cloud incident status

- [OpenAI - https://status.openai.com/history](https://status.openai.com/history)
- [Azure Cloud - https://status.azure.com/en-us/status/history](https://status.azure.com/en-us/status/history)
- [IBM Cloud - https://cloud.ibm.com/status/incident-reports](https://cloud.ibm.com/status/incident-reports)
- [Google Cloud - https://status.cloud.google.com/summary](https://status.cloud.google.com/summary)
- [Google Cloud - https://www.google.com/appsstatus/dashboard/summary](https://www.google.com/appsstatus/dashboard/summary)
- [AWS Health Dashboard - https://health.aws.amazon.com/health/status](https://health.aws.amazon.com/health/status)
- [AWS Post-Event Summaries - https://aws.amazon.com/premiumsupport/technology/pes/](https://aws.amazon.com/premiumsupport/technology/pes/)
- [Alibaba Cloud - https://status.alibabacloud.com/](https://status.alibabacloud.com/)
- [Verica Open Incident Database](https://www.thevoid.community/)
- [Github Incidents](https://www.githubstatus.com/history)
- [Atlassian](https://status.atlassian.com/)
- [CircleCI](https://status.circleci.com/)
- [Notion](https://status.notion.so/)

# Benchmark & Microservices Systems

- [RCAEval: A Benchmark for Root Cause Analysis of Microservice Systems (ASE'24, WWW'25)](https://github.com/phamquiluan/RCAEval): Ready-to-use datasets and framework.
- [Train Ticket @ Fudan University](https://github.com/FudanSELab/train-ticket) (40+ microservices) [How to deloy](docs/how-to-deploy-train-ticket.md)
- [Train Ticket @ RMIT](https://github.com/phamquiluan/rmit-train-ticket) [How to deploy](docs/how-to-deploy-rmit-train-ticket.md)
- [Online Boutique @ Google Cloud](https://github.com/GoogleCloudPlatform/microservices-demo)
- [Sock Shop @ RMIT](https://github.com/phamquiluan/sock-shop)
- [Sock Shop @ Weaveworks](https://github.com/microservices-demo/microservices-demo)
- [Robot Shop @ Instana](https://github.com/instana/robot-shop)
- https://www.instana.com/blog/stans-robot-shop-sample-microservice-application/
- https://istio.io/latest/docs/examples/bookinfo/
- https://wilsonmar.github.io/easytravel/

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
- [Prometheus - Node Exporter](https://github.com/prometheus/node_exporter): Exporter for machine metrics.
- [Prometheus - Blackbox prober exporter](https://github.com/prometheus/blackbox_exporter): Allows blackbox probing of endpoints over HTTP, HTTPS, DNS, TCP, ICMP and gRPC.
- [tsfresh](https://github.com/blue-yonder/tsfresh): Automatic extraction of relevant features from time series.
- [cAdvisor (Container Advisor)](https://github.com/google/cadvisor): Analyzes resource usage and performance characteristics of running containers.

## Logs

- https://github.com/logpai/loglizer
- ELK ([Elasticsearch](https://github.com/elastic/elasticsearch) + [Logstash](https://www.elastic.co/logstash/) + [Kibana](https://www.elastic.co/kibana/))
- EFK ([Elasticsearch](https://github.com/elastic/elasticsearch) + [Fluentd](https://www.fluentd.org/) + [Kibana](https://www.elastic.co/kibana/))
- https://github.com/grafana/loki

## Traces

- https://github.com/apache/skywalking
- https://github.com/jaegertracing/jaeger
- https://github.com/openzipkin/zipkin
- [OpenTelemetry](https://opentelemetry.io/docs/concepts/signals/): supports metrics, logs, and traces.

## Load generators

- [Locust](https://github.com/locustio/locust): a load testing tool for web applications. It is used to simulate a large number of users accessing a web application simultaneously, in order to test its performance and scalability.
- [Vegeta](https://github.com/tsenart/vegeta): HTTP load testing tool and library. It's over 9000!
- [Jmeter](https://github.com/apache/jmeter): a testing tool used to test the performance of web applications, databases, and APIs. It can simulate a heavy load on a server, group of servers, network, or object to test its strength or to analyze overall performance under different load types. It can also be used to test the performance of different protocols such as HTTP, FTP, TCP, JDBC, and JMS.
- [Stress-ng](https://github.com/ColinIanKing/stress-ng): a tool that can be used to stress test various aspects of a Linux system, such as the CPU, memory, I/O, and network.
- [wrk2](https://github.com/giltene/wrk2): HTTP workload generator.

## Chaos Engineering / Fault Injection

- [Chaos Mesh](https://github.com/chaos-mesh/chaos-mesh): an open-source chaos engineering platform for Kubernetes. It provides a set of APIs and CLI tools that allow users to define and orchestrate chaos experiments, such as network latency injection, pod failure, etc.
- [TC (Traffic Control)](https://man7.org/linux/man-pages/man8/tc.8.html): Delay and drop packets.
- [tc-netem (Network Emulator)](https://man7.org/linux/man-pages/man8/tc-netem.8.html): an enhancement of the Linux traffic control facilities that allow one to add delay, packet loss, duplication and more other characteristics to packets outgoing from a selected network interface. NetEm is built using the existing Quality Of Service (QOS) and Differentiated Services (diffserv) facilities in the Linux kernel.
- https://github.com/Netflix/chaosmonkey
- [ChaosBlade](https://github.com/chaosblade-io/chaosblade): a performance testing and analysis tool for microservices. It allows users to simulate various types of failures and network conditions, such as network delays and packet loss, to test the resilience and stability of microservices in a controlled environment.
- [Strace](https://strace.io/): a diagnostic, debugging and instructional userspace utility for Linux. It is used to monitor and tamper with interactions between processes and the Linux kernel, which include system calls, signal deliveries, and changes of process state.
- [Chaos Toolkit](https://github.com/chaostoolkit/chaostoolkit): a CLI tool which helps to run Chaos Engineering experiments.
- [Chaos Genius](https://docs.chaosgenius.io/docs/introduction)

# Academia

## Conferences and Journals

- A\* Ranked Conference: [ICSE](https://dblp.uni-trier.de/db/conf/icse/index) | [FSE](https://dblp.uni-trier.de/db/conf/sigsoft/index) | [ASE](https://dblp.org/db/conf/kbse/index.html) | [WWW](https://dblp.org/db/conf/www/index.html) | [KDD](https://dblp.org/db/conf/kdd/index.html) | [NeurIPS](https://dblp.org/db/conf/nips/index.html)
- A Ranked Conference: ICSME | ICPC | ESEM | RE | MSR | ISSTA | SANER | ICST | ISSRE
- Top Q1 Journal: [IEEE TSE](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=32), [IEEE TDSC](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=8858), [TOSEM](https://dl.acm.org/journal/tosem)

[[Check Conference Rank](http://portal.core.edu.au/conf-ranks/)][[Check Journal Rank](https://www.scimagojr.com/journalrank.php)][[Check Paper Acceptance Status](https://dblp.org/)]

## Researcher

- [Prof. Hongyu Zhang - Chongqing University](https://sites.google.com/site/hongyujohn/) [[Google Scholar]](https://scholar.google.com/citations?user=zsUN6PkAAAAJ&hl=en&oi=ao)
- [Prof. Odej Kao - TU Berlin](https://scholar.google.com/citations?hl=en&user=mvOSfFAAAAAJ) [[Google Scholar]](https://scholar.google.com/citations?hl=en&user=mvOSfFAAAAAJ)
- [Prof. Michael R. Lyu - The Chinese University of Hong Kong](https://www.cse.cuhk.edu.hk/lyu/) [[Google Scholar]](https://scholar.google.com/citations?user=uQnBgK0AAAAJ&hl=en)
- [Assoc Prof. Dan Pei - Tsinghua University](https://netman.aiops.org/~peidan/) [[Google Scholar]](https://scholar.google.com/citations?user=i_zA1VsAAAAJ&hl=en&oi=ao)
- [Prof. Tao Xie - Fudan University](https://taoxiease.github.io/) [[Google Scholar]](https://scholar.google.com/citations?user=DhhH9J4AAAAJ&hl=en&oi=ao)
- [Prof. Peng Xin - Fudan University](https://cspengxin.github.io/) [[Google Scholar]](https://scholar.google.com/citations?user=wATYGXEAAAAJ&hl=en&oi=ao)
- [Dr. Dongmei Zhang - Microsoft Asia Research](https://www.microsoft.com/en-us/research/people/dongmeiz/) [[Google Scholar]](https://scholar.google.com/citations?user=jLlBBl4AAAAJ&hl=en&oi=ao)
- [Qingwei Lin - Microsoft Research Asia](https://www.microsoft.com/en-us/research/people/qlin/publications/) [[Google Scholar]](https://scholar.google.com/citations?user=W9fdsxMAAAAJ&hl=en&oi=ao)
- [Assoc. Prof. Pengfei Chen - Sun Yat-sen University](https://scholar.google.com/citations?user=g9tdjgQAAAAJ&hl=en) [[Google Scholar]](https://scholar.google.com/citations?user=g9tdjgQAAAAJ&hl=en)
- [Guangba Yu - Sun Yat-sen University](https://yuxiaoba.github.io/) [[Google Scholar]](https://scholar.google.com/citations?user=wXY0D6YAAAAJ&hl=en&oi=ao)

# Video

- [Causal Inference Course Lectures - Brady Neal](https://www.youtube.com/playlist?list=PLoazKTcS0Rzb6bb9L508cyJ1z-U9iWkA0)
- [Adobe - The Good, the Bad and the Ugly: The 3 Learnings of an SRE](https://www.usenix.org/conference/srecon20americas/presentation/charagondla)
- [The Smallest Possible SRE Team](https://www.usenix.org/conference/srecon20americas/presentation/thomas)
- [Banking on Continuous Delivery - Capital One](https://www.youtube.com/watch?v=_DnYSQEUTfo)

# Others

- https://github.com/chenryn/aiops-handbook
- https://github.com/donnemartin/system-design-primer
- https://github.com/upgundecha/howtheysre
- https://github.com/dastergon/awesome-sre
- https://github.com/logpai/awesome-log-analysis
- https://github.com/yzhao062/anomaly-detection-resources
- https://github.com/hoya012/awesome-anomaly-detection
- https://github.com/adriannovegil/awesome-observability
- https://github.com/dastergon/awesome-chaos-engineering
- https://github.com/awesome-foss/awesome-sysadmin
- https://github.com/rguo12/awesome-causality-algorithms
- https://www.amazon.science/blog/a-gentle-introduction-to-automated-reasoning
