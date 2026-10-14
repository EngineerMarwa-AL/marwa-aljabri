Version: NAFATH-V2


Track: Networking



## Overview
A reliable 5G service for emergency responders depends on six connected IT fields. Software defines how applications send requests, handle failures, and retry operations without creating duplicate actions. Artificial intelligence can predict network congestion by learning from traffic patterns, helping operators prepare capacity before service quality declines. Mobile applications must remain useful when responders lose connectivity, storing essential information safely and synchronizing updates when the network returns. Networking provides the 5G infrastructure and traffic separation needed to prioritize emergency communications. Cybersecurity protects the service through monitoring, incident response, containment, and recovery. Data engineering organizes regional and daily usage information so teams can measure performance and make informed decisions. Together, these fields support availability, secure operations, and dependable information during emergencies. My track focuses on 5G network slicing and how a dedicated slice can support emergency responders.




## Software
Safe HTTP methods like GET do not modify server state, while idempotent methods like PUT and DELETE  provide identical results no matter how many times they are repeated. In unstable 5G emergency networks, dropped packets often obscure whether a request actually succeeded. Safe and idempotent requests can safely retry automatically without side effects. Conversely, unsafe methods like POST risk catastrophic duplicate actions if retried blindly, meaning they require unique idempotency header keys to ensure reliable execution during sudden connection failures.

Resource: <Initial Hypertext Transfer Protocol (HTTP) Method Registrations> - <https://www.rfc-editor.org/info/rfc7237/>




## AI
Under the NIST AI Risk Management Framework (AI RMF) MEASURE function, validating emergency 5G congestion models is essential for preventing critical reliability failures.Overfitting occurs when models learn noise rather than underlying traffic trends, resulting in poor performance on live data.Cross validation prevents this by evaluating the model across data folds to ensure unseen performance, keeping 5G networks resilient against outages.

Resource: <NIST AI Risk Management Framework (AI RMF 1.0)> - <https://content.salt.security/rs/352-UXR-417/images/NIST-AI-Risk-Management-Framework.pdf?version=0>




## Mobile 
Emergency responder application must incorporate local first databases(e.g SQL)and optimistic user interface updates to keep apps fully operational offline. Offline actions are maintained in a strict chronological queue. The app automatically processes this queue using first in first out (FIFO) ordering when the connectivity returns .idempotent requests and timestamp based conflict resolution ensure duplicate server synchronization.

Resource: <Data layer | Android Developers> - <https://developer.android.com/topic/architecture/data-layer>




## Networking
5G network slicing partitions physical infrastructure into virtual, independent networks. For emergency responders, a dedicated slice guarantees uninterrupted communications during heavy congestion. By isolating public safety traffic, utilizing localized backup routing for infrastructure outages, and applying end-to-end encryption against cyber attacks, the system maintains critical, real-time connectivity when standard cellular networks fail.

Resource: <How 5G in Public Safety Transforms Emergency Response Communication> - <https://www.trugemtech.com/how-5g-in-public-safety-transforms-emergency-response-communication/>




## Cybersecurity
According to the NIST SP 800-61 Revision 3 guidelines, the incident response lifecycle comprises preparation activities integrated with broader risk management, detection and analysis to triage alerts and scope impact, containment, eradication, and recovery to stop threats, remove root causes, and restore systems, and continuous improvement activities to analyze lessons learned and feed them back into risk management controls.

Resource: < Incident Response Recommendations and Considerations for Cybersecurity Risk Management: A CSF 2.0 Community Profile> - <https://csrc.nist.gov/projects/incident-response>




## Data
According on the Star Schema Guide, a star schema features denormalized, wide dimension tables directly linked to a central fact table, enabling faster queries with fewer joins.Conversely, a snowflake schema normalizes dimensions into a hierarchical structure, improving storage efficiency but requiring slower, multi-hop joins.The star schema suits best because its fast, single-hop joins ensure rapid reporting performance when speed matters most for tracking daily regional 5G emergency service usage under stress.

Resource: <What Is a Star Schema? A Complete Guide for Data Modeling | Snowflake> - <https://www.snowflake.com/en/fundamentals/star-schema/>
