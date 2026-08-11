# Google Cloud Options for Gemini XPRIZE

## Context & Project Needs
This document outlines the infrastructure choices for **Proof-By-User**, an AI-native SaaS built for the Gemini XPRIZE hackathon. 

**Project Summary:** 
Proof-By-User helps founders run customer interviews the "Mom Test" way. The core data model is relational, involving:
- Users & Organizations
- Projects & Hypotheses
- Interview Transcripts (raw text/audio)
- Assumption Maps (linking transcript evidence to assumptions)

**Why this matters for infrastructure:**
1. **Competition Rules:** The Gemini XPRIZE requires that the final product utilizes at least one Google Cloud product in production, and uses the Gemini API for at least one core LLM function.
2. **Speed vs. Structure:** As a 90-day hackathon, development speed is critical. However, the relational nature of the data (Transcripts mapped to Assumptions) means the database choice (SQL vs. NoSQL) will heavily impact the backend architecture.
3. **AI Agent Context:** Any AI coding assistant reading this document should understand that we are evaluating infrastructure options based on finding the optimal balance between meeting competition requirements, executing quickly, and supporting a moderately complex relational data model.

---

## Google Cloud Fulfillments
To fulfill the technical requirement of using **at least one product from Google Cloud**, you have several options when building your SaaS application. You only need to implement **one** of these to check the box for the competition.

Here are the most common and accessible options for a hackathon project like Proof-By-User:

## 1. Firebase (Highly Recommended)
Firebase is Google's platform for quickly building web and mobile apps. It is part of Google Cloud and is usually the fastest way to fulfill this requirement for a web app.
* **Firebase Hosting:** Easily host your front-end web application (e.g., React, Vue, HTML/JS).
* **Firebase Authentication:** Handle user logins, signups, and session management securely.
* **Cloud Firestore:** A NoSQL database perfect for storing user data, project insight vaults, and transcript records.

*Pro-tip: Using Firebase Hosting or Firebase Auth immediately satisfies the Google Cloud requirement with minimal setup.*

## 2. Google Cloud Run
If you are building a backend server (like a Node.js/Express API, Python backend, or Next.js app) and can put it in a Docker container, you can deploy it to **Cloud Run**. 
* **Benefits:** It scales automatically from zero to thousands of users and is very cost-effective (often completely free for low-traffic prototypes).

## 3. Google Cloud Storage
If your application allows users to upload files—such as raw PDF/TXT interview transcripts or audio recordings—you can store these files in **Cloud Storage** (Google's equivalent to AWS S3).

## 4. Vertex AI
The XPRIZE rules explicitly state that using **Vertex AI** (Google's enterprise machine learning platform) counts towards the Google Cloud requirement. 
* **How to use:** Instead of using the standard Google AI Studio for your Gemini API calls, you can route your Gemini API requests through Vertex AI. This fulfills both the LLM requirement and the Google Cloud requirement simultaneously.

## 5. Google Cloud SQL
If your architecture requires a traditional relational database (PostgreSQL, MySQL, or SQL Server), you can host it using **Cloud SQL**. This is a fully managed database service on Google Cloud.

---

## Supabase vs. Firebase (Recommendation)

For a 90-day hackathon, speed and developer experience (DX) are your top priorities. Here is a breakdown of how to choose between them:

### Recommendation A: Go with Firebase (Google Infra)
**Choose this if:** You want the absolute fastest path to an MVP, want to keep everything in one ecosystem, and don't mind NoSQL databases.
* **Why:** Firebase is technically Google Cloud. By using Firebase Auth and Firestore, you instantly check the competition requirement without having to think about it. It is historically the fastest way to get a web app running, and the integration between Firebase, Google Cloud Functions, and the Gemini API is seamless.
* **The Catch:** Firestore is a NoSQL database. If you have highly complex relational data, it can be slightly harder to query compared to SQL.

### Recommendation B: Go with Supabase + Vertex AI
**Choose this if:** You strongly prefer SQL (PostgreSQL), you love Supabase's developer experience, or you plan on having complex data relationships (Users -> Projects -> Transcripts -> Assumptions).
* **Why:** Supabase is phenomenal. It gives you a proper Postgres database, instant APIs, and great Auth out of the box. For an app like "Proof-By-User", a relational SQL database is a very natural fit. 
* **How to meet the rules:** You would build the app on Supabase, but you would make your Gemini API calls via **Google Vertex AI** instead of Google AI Studio. This satisfies the "Must use Google Cloud" requirement.
