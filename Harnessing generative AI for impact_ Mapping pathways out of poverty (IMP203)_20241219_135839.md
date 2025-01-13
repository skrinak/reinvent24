# Summary of AWS re_Invent 2024 - Harnessing generative AI for impact_ Mapping pathways out of poverty (IMP203).txt

# Summary

## FINCA International's Mission and Journey with AWS

### Main Points:

- FINCA International has been fighting global poverty for 40 years by providing small loans and supporting social enterprises that meet basic needs of the poor.
- Scott Graham, VP of Research and Data Science at FINCA, aims to provide evidence to guide and validate their work in finding effective and sustainable pathways out of poverty.
- One challenge is assessing the impact of emerging solutions, as good ideas often fail or have unintended consequences.

### Key Insights:

- Researching complex social issues like land titling for cocoa farmers involves understanding deep cultural, administrative, and behavioral factors.
- Traditional research methods involve time-consuming manual searches, filtering, and curation of relevant sources and evidence.
- FINCA developed AuRA, an Automated Research Assistant, to accelerate this process using generative AI and data engineering.

## AuRA: Automated Research Assistant

### Architecture and Process:

- AuRA uses a foundation model (e.g., Bedrock Anthropic) to expand a general query into a comprehensive set of topics and subtopics.
- These topics drive parallel searches across multiple research databases and search engines, gathering a curated data library.
- Researchers can interact with the results, provide feedback, and regenerate the topic model using Retrieval Augmented Generation (RAG) based on their expertise and trusted sources.

### Benefits:

- Significantly reduces the time and effort required for research, from weeks/months to hours/minutes.
- Allows researchers to focus on subject matter expertise rather than manual curation.
- Enables faster knowledge acquisition and better resource allocation to find sustainable solutions to poverty.

### Challenges and Lessons Learned:

- Involving subject matter experts early to validate outputs and reduce biases/hallucinations.
- Using prompt engineering to guide the AI towards more specific, relevant, and accurate results.
- Considering scalability and costs as the solution expands to the broader community.
- Collaborating with technical partners and leveraging AWS expertise and services (e.g., Amazon Bedrock, Titan Embeddings) for effective implementation.

## Next Steps:

- Enhancing the reporting layer to better summarize insights for non-researchers (program implementers, CEOs).
- Continuing to gather feedback from diverse users and refine the solution accordingly.
- Exploring AWS services and partnerships to scale AuRA's impact in the broader research community.

Overall, AuRA demonstrates how responsible integration of generative AI and human expertise can accelerate knowledge acquisition and drive impactful solutions to complex global challenges like poverty.