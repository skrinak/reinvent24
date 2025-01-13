# Summary of AWS re_Invent 2024 - How Stripe achieves five and a half 9s of availability (FSI321).txt

# Summary: How Stripe Achieves Five and a Half 9s of Availability

## Introduction

- Stripe supports the highly regulated financial industry and serves as the backbone of the global economy, moving trillions of dollars every year.
- Ensuring uninterrupted operations is critical, and Stripe strives to achieve five and a half 9s of availability, which means only 13 seconds of downtime per month.
- Reliability is not a property of the system on its best day but on its worst day, under load and strain.

## Technical Strategies for High Reliability

### Cell-based Architectures

- Stripe uses cell-based architectures, where isolated copies of a system independently serve traffic, to isolate failures.
- Cells help reduce the blast radius of failures and enable controlled rollouts of changes.
- Cell-based architectures can be introduced incrementally and don't have to be implemented across the entire system at once.

### Detecting and Remediating Gray Failures

- Gray failures, such as high disk latency or noisy neighbors, are partial or intermittent issues that are harder to detect than outright failures.
- Stripe uses anomaly detection to automatically discover misbehaving nodes based on metrics like request latency and removes them from the service mesh.
- Anomaly detection should start with the assumption that only one node at a time will experience gray failure and should be implemented outside of the potentially failing nodes.

### Chaos Testing and Fault Injection

- Stripe simulates node failures and gray failures through chaos testing and fault injection to ensure automated remediations work.
- Chaos testing frameworks introduce faults like increased network latency, CPU contention, or disk latency, and teams gradually enable more faults as their services mature.

### Load Testing

- Stripe uses massive synthetic traffic to load test systems at many times the load of peak user traffic, uncovering weaknesses and identifying resource exhaustion points before failure.
- Load testing helps identify opportunities to make systems more efficient at lower scales and ensures systems can handle all-time high traffic events like Black Friday and Cyber Monday.

### Continuous Delivery

- Stripe deploys tens of thousands of changes per day across thousands of services, primarily through automated continuous delivery pipelines.
- Continuous delivery increases reliability by ensuring consistent, repeatable deploys, reducing the chance of human error, and minimizing the cost of fleet-wide changes.

### Retries

- Stripe retries failed requests on behalf of users within their internal network, reducing overall latency and leveraging internal knowledge of the architecture for efficient retries.
- Retries should be implemented at the outermost layer closest to the user, and APIs should be designed with idempotency in mind to handle retries correctly.

### User Experience Monitoring

- Stripe proactively alerts users when they're having a particularly bad experience, monitoring for spikes in specific error codes, APIs, payment methods, and latency.
- Stripe works with users to improve inefficient integrations, benefiting both parties by reducing load and improving reliability.

## Building a Culture of Reliability

### Practice Your Worst Day Every Day

- Stripe exhibits extreme curiosity about its systems, pushing them to their breaking points through various scenarios to understand their limits and failure modes.
- Systems are designed from the ground up to tolerate failures, combining technology with observability and automation for early detection and self-healing.
- Stripe continuously stresses its systems through load testing, synthetic traffic, chaos engineering, and fault testing to control its destiny and fail on its own timeline.

### Never Send a Human to Do a Machine's Job

- Stripe relies on machines to detect and mitigate incidents within its tight error budget, as humans react in minutes while machines react in milliseconds.
- Stripe has dedicated over a million CPUs to observe and monitor systems, emitting millions of metrics and running billions of automated tests daily.
- Automation is used to mitigate failures and degradations quickly, without human involvement in the critical path.

### Extreme Ownership

- Reliability is not owned by a committee but comes from the passion and pride of engineers and leaders.
- Stripe institutionalizes accountability through weekly senior executive reviews, where leaders must demonstrate intimate knowledge of their services, incidents, and plans for improvement.
- Operational wins are recognized and celebrated, and leaders are accountable for the end-to-end customer experience, not just their slice.

## Partnership with AWS

- Stripe's exceptional partnership with AWS is a foundational part of its ability to drive reliability and availability goals.
- Stripe routinely meets and shares technical ideas and feedback with critical AWS teams like EBS, EC2, and networking.
- Stripe is excited about its partnership with AWS and aims to win and build together.