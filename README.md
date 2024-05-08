<!-- # Generative-AI-Project -->
VidHarbor: Your Tailored YouTube Voyage

The project envisions a dedicated educational search platform that revolutionizes the way users interact with YouTube channels. The platform aims to bridge the gap between user queries and relevant content by providing a comprehensive list of reputable and curated YouTube channels. This curated collection ensures that users have access to high-quality, educational resources aligned with their learning goals.

Central to the platform is its advanced search functionality, which allows users to formulate natural language questions or use keywords to find specific information or explanations. Leveraging state-of-the-art natural language processing (NLP) techniques, the platform accurately interprets user queries and matches them with videos that provide the most relevant and comprehensive answers.

The platform's chat-based interface enhances user interaction by simulating a natural conversation. Users can engage with the platform as they would with a knowledgeable teacher, asking follow-up questions or requesting further clarification. The platform's response are tailored to the user's query, ensuring a personalized and interactive learning experience.

The project's innovative approach has several benefits:

- It empowers users to efficiently extract information from trusted and reliable YouTube creators. By aggregating content from reputable channels, the platform ensures the accuracy and credibility of the information provided.
- It enhances the overall content consumption experience by offering users a seamless and intuitive interface. The chat-based interface makes it easy for users to navigate through videos and find the exact information they need.
- The platform has the potential to democratize education by providing users with equal access to high-quality educational resources. By removing the barriers of time and location, the platform empowers individuals to learn at their own pace and on their own terms.

## Implementation Details

#### Architecture Overview

Our platform operates on a microservices architecture, comprising several interconnected components:

- Data Ingestion Service: Responsible for fetching and processing YouTube video data from selected channels.
- Indexing Service: Indexes the video content, including transcripts and metadata, for efficient retrieval.
- Query Handling Service: Receives user queries, matches them against indexed content, and returns relevant results.
- User Interface: Provides the frontend interface for users to interact with the platform.

#### Backend Implementation

- Programming Languages: Python
- Framework: Flask
- Database: MongoDB
- NLP Libraries: Spacy
- YouTube Data API: Used for fetching video content, metadata, and transcripts.
- Embeddings: Gemini's embedding function for generating embeddings.
- Model: Gemini-Pro for generating responses to user queries.

#### Frontend Implementation

- Programming Languages: JavaScript
- Framework: React

#### Data Extraction

Transcripts were extracted from 9 YouTube channels, including:

- Programming with Mosh
- TEDx Talks
- Y Combinator
- BroCodez
- freeCodeCamp
- Clever Programmer
- Net Ninja
- Lex Fridman (Podcasts on Tech)
- Huberman Lab (Neuroscience and Science-based Tools)

Initially, 5 videos were extracted from each channel.

#### Database

The database used is ChromaDB.

#### Under the Hood

- Data Processing: Videos are fetched from YouTube channels using the YouTube Data API. Transcripts are generated using speech-to-text services and stored alongside metadata.
- Indexing: Transcripts and metadata are indexed using Elasticsearch for efficient retrieval.
- Query Handling: User queries are processed using NLP techniques to extract intent and keywords. Elasticsearch is then queried to find relevant videos matching the user's query.
- User Interaction: The frontend provides an intuitive interface for users to input queries and browse search results. Results are displayed with relevant timestamps, allowing users to jump directly to the relevant section of a video.

## Deployment

#### Deployment Strategy

- The deployment strategy involved considerations for scalability, reliability, and performance.
- The platform was deployed on Vercel, a cloud platform for static sites and serverless functions.
- Vercel provides seamless integration with frontend frameworks like React, making it ideal for hosting single-page applications.

####

#### Infrastructure Used

- Cloud Infrastructure Provider: Vercel
- Considerations:
- Scalability: Vercel's auto-scaling capabilities were leveraged to handle varying traffic loads without manual intervention.
- Reliability: Vercel's global CDN and redundant infrastructure ensured high availability and reliability of the deployed application.
- Performance: Static assets were served through Vercel's CDN, optimizing load times and improving the overall performance of the application.

#### Continuous Integration/Continuous Deployment (CI/CD)

- Vercel provides built-in CI/CD capabilities, enabling automated deployments from GitHub or other version control systems.
- Automatic preview deployments allowed for testing changes in a production-like environment before merging them into the main branch.

#### Monitoring and Logging

- Vercel's dashboard provides insights into deployment metrics, including latency, traffic, and errors.
- Application logs can be accessed through Vercel's logging interface for troubleshooting and performance monitoring.

#### Security

- Vercel ensures secure deployments by providing SSL encryption for data in transit and at rest.
- Access controls and authentication mechanisms were implemented within the application to restrict unauthorized access to sensitive resources.

## Experiments and Iterations

#### Iterative Process

- The development process followed an iterative approach, with a series of experiments and refinements aimed at improving the platform's functionality and user experience.
- Each iteration focused on specific aspects of the platform, including data extraction, model performance, user interface design, and deployment optimizations.

#### Feedback Loop

- Continuous feedback from users and stakeholders played a crucial role in shaping the evolution of the platform.
- User testing sessions were conducted regularly to gather feedback on usability, search accuracy, and overall satisfaction with the platform.

#### Improvements Made

- Data Extraction Optimization: Initially, data extraction focused on a limited number of videos from each channel. Subsequent iterations optimized the extraction process to include more videos and improve coverage of content.
- Model Fine-tuning: The GPT-4 model underwent iterative fine-tuning based on user feedback. Emphasis was placed on improving the model's ability to accurately interpret user queries and provide relevant responses.
- User Interface Refinements: Iterative improvements were made to the frontend interface based on user feedback and usability testing results. Changes included enhancements to search functionality, result presentation, and overall user interaction flow.
- Deployment Optimization: Deployment configurations were iteratively optimized to ensure scalability, reliability, and performance. Load testing and monitoring were conducted to identify and address any performance bottlenecks.

#### Evaluation Metrics

- Performance metrics, including response time, search accuracy, and user engagement metrics, were continuously monitored throughout the development process.
- User satisfaction surveys and qualitative feedback collection mechanisms were employed to gauge user satisfaction and gather insights for further improvements.

#### Future Directions

- Future iterations will focus on enhancing the platform's capabilities, including the incorporation of advanced NLP techniques and expanding the dataset to include additional channels and topics.
- Collaboration with content creators and domain experts will be pursued to ensure the platform remains relevant and valuable to its users.
- Ongoing optimization efforts will continue to improve scalability, reliability, and overall user experience based on feedback and emerging technologies.
- Addition of chat history through which the user can look at the prompts and answers of their previous sessions.

## Reflections

#### Successes

- User Engagement: The platform garnered positive feedback from users, with many appreciating its intuitive interface and ability to provide relevant insights from YouTube videos.
- Search Accuracy: Through iterative improvements, the platform achieved significant enhancements in search accuracy, enabling users to quickly find precise information within their favorite creators' videos.
- Scalability and Performance: Deployment optimizations ensured the platform's scalability and reliability, allowing it to handle increasing user loads without compromising performance.

#### Challenges

- Data Coverage: Despite efforts to extract transcripts from a diverse set of channels, achieving comprehensive coverage of all relevant topics remains a challenge. Expanding the dataset to include more channels and topics is essential for improving the platform's usefulness.
- Model Complexity: Fine-tuning the Gemini-Pro model required substantial experimentation and expertise. Balancing model complexity with computational resources and deployment constraints posed challenges during development.
- User Feedback Incorporation: Effectively incorporating user feedback into the development process required careful consideration and prioritization. Balancing user requests with technical feasibility and project goals was sometimes challenging.

#### Next Steps

- Dataset Expansion: Expanding the dataset to include a broader range of channels and topics will be a priority to improve the platform's coverage and usefulness.
- Model Enhancement: Continued refinement and enhancement of the Gemini-Pro model will focus on improving response accuracy and understanding of user queries.
- User Experience Optimization: Iterative improvements to the user interface and search functionality will aim to further enhance user experience and satisfaction.
- Community Engagement: Establishing a community forum or feedback channel will facilitate ongoing communication with users and content creators, enabling continuous improvement and innovation.

#### Lessons Learned

- Iterative Development: Embracing an iterative development approach enabled rapid experimentation and adaptation to evolving user needs and technical challenges.
- User-Centric Design: Prioritizing user feedback and usability testing was crucial for ensuring the platform's relevance and adoption by its target audience.
- Collaborative Approach: Collaborating with domain experts and stakeholders, including content creators and users, enriched the development process and contributed to the platform's success.

## Demonstration of the Project

- 1. **Main Usage Diagrams: Provide visual aids demonstrating the primary functionalities and user interactions of the application.**


It has login screen which allows an already registered user to login using their credentials.


It has signup screen which allows a new user to register.

Once the user has successfully logged in, the user is redirected to the main screen.

The screen shows the list of channels and a window where prompts can be written and answers will be displayed.