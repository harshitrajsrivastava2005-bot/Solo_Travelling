# System Design Document: Rover

## 1. System Architecture Overview
The platform utilizes a serverless architecture to ensure scalability, reliability, and cost efficiency. It leverages AWS cloud infrastructure to handle everything from user authentication to complex AI processing.

## 2. Process Flow
1. **User Input:** User enters travel preferences via the Mobile/Web.
2. **API Layer:** Request goes through Amazon API Gateway to the AWS Lambda backend for secure processing.
3. **AI Processing Layer:**
    * Itinerary generation (LLM).
    * Budget optimization.
    * Safety risk scoring.
    * Group matching.
4. **Database Layer:** Data is stored in the Database Layer (utilizing Amazon RDS and DynamoDB).
5. **Output:** The system returns a personalized, budget-optimized, and safety-verified travel plan to the user.

## 3. User Journey (Screen Flow)
The application follows a linear, easy-to-navigate process to minimize cognitive load:
* **Home Screen:** Enter budget, dates, interests.
* **AI Travel Roadmap:** Optimized itinerary generated.
* **Group Matching:** Verified activities & participants.
* **Booking Summary:** Cost breakdown & confirmation.
* **Safety Dashboard:** Risk score & SOS options.

## 4. Key Technologies & AWS Services
* **Frontend Interface:** Mobile Application / Web Interface.
* **API Routing:** Amazon API Gateway.
* **Backend Compute:** AWS Lambda.
* **AI / Machine Learning:** * Amazon Bedrock (for LLM-Based Itinerary Generation).
  * Amazon SageMaker (for Budget Optimization and Risk Scoring Models).
* **Database:** Amazon RDS / DynamoDB for User and Booking Data.
* **Security & Identity:** Amazon Cognito Authentication & Security.
* **Monitoring:** Amazon CloudWatch.
