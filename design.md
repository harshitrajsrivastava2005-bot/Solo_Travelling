# System Design Document: Rover

## 1. System Architecture Overview
[cite_start]The platform utilizes a serverless architecture to ensure scalability, reliability, and cost efficiency[cite: 113]. It leverages AWS cloud infrastructure to handle everything from user authentication to complex AI processing.

## 2. Process Flow
1. [cite_start]**User Input:** User enters travel preferences via the Mobile/Web[cite: 57].
2. [cite_start]**API Layer:** Request goes through Amazon API Gateway to the AWS Lambda backend for secure processing[cite: 58].
3. **AI Processing Layer:**
    * [cite_start]Itinerary generation (LLM)[cite: 59].
    * [cite_start]Budget optimization[cite: 60].
    * [cite_start]Safety risk scoring[cite: 61].
    * [cite_start]Group matching[cite: 62].
4. [cite_start]**Database Layer:** Data is stored in the Database Layer [cite: 63] (utilizing Amazon RDS and DynamoDB).
5. [cite_start]**Output:** The system returns a personalized, budget-optimized, and safety-verified travel plan to the user[cite: 64].

## 3. User Journey (Screen Flow)
The application follows a linear, easy-to-navigate process to minimize cognitive load:
* [cite_start]**Home Screen [cite: 88][cite_start]:** Enter budget, dates, interests[cite: 97].
* [cite_start]**AI Travel Roadmap [cite: 89][cite_start]:** Optimized itinerary generated[cite: 98].
* [cite_start]**Group Matching [cite: 90][cite_start]:** Verified activities & participants[cite: 99, 100].
* [cite_start]**Booking Summary [cite: 91][cite_start]:** Cost breakdown & confirmation[cite: 101].
* [cite_start]**Safety Dashboard [cite: 92][cite_start]:** Risk score & SOS options[cite: 102, 103].

## 4. Key Technologies & AWS Services
* [cite_start]**Frontend Interface:** Mobile Application / Web Interface[cite: 73].
* [cite_start]**API Routing:** Amazon API Gateway[cite: 114].
* [cite_start]**Backend Compute:** AWS Lambda[cite: 115].
* [cite_start]**AI / Machine Learning:** * Amazon Bedrock (for LLM-Based Itinerary Generation)[cite: 116].
  * [cite_start]Amazon SageMaker (for Budget Optimization and Risk Scoring Models)[cite: 117, 118, 119].
* [cite_start]**Database:** Amazon RDS / DynamoDB [cite: 121] [cite_start]for User and Booking Data[cite: 122].
* [cite_start]**Security & Identity:** Amazon Cognito Authentication & Security[cite: 124].
* [cite_start]**Monitoring:** Amazon CloudWatch[cite: 127].
