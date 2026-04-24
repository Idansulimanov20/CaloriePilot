🥗 Fitness & Nutrition AI Tracker

A full-stack web application for tracking calories, meals, and water intake with AI-powered food analysis.

⸻

🚀 Features

🥗 Nutrition Tracking

* Add meals manually
* AI-based food analysis (text)
* Daily calorie tracking
* Goal tracking (on track / exceeded)

💧 Water Tracking

* Daily water goal (default: 8 cups)
* Add water intake
* Progress tracking
* Custom target

🔔 Notifications

* Smart reminders for water intake
* Daily goal alerts

⸻

🧱 Tech Stack

Frontend

* Next.js
* React
* TailwindCSS
* Zustand

Backend

* Node.js
* Express.js
* Prisma ORM

Database

* PostgreSQL

AI

* OpenAI API / Gemini

Notifications

* Firebase Cloud Messaging

⸻

🏗️ Architecture Diagram

graph TD
%% CLIENT
A[Client (Next.js App)] -->|HTTP Requests| B(API Layer)
%% BACKEND
B --> C[Express Server]
%% MODULES
C --> D[Auth Module]
C --> E[User Module]
C --> F[Meal Module]
C --> G[Water Module]
C --> H[AI Module]
C --> I[Notification Module]
%% DATABASE
D --> J[(PostgreSQL)]
E --> J
F --> J
G --> J
%% AI SERVICES
H --> K[OpenAI / Gemini]
%% NOTIFICATIONS
I --> L[Firebase Cloud Messaging]
%% RESPONSE FLOW
J --> C
K --> C
L --> A
%% LABELS
classDef core fill:#1e293b,color:#fff;
classDef ext fill:#0ea5e9,color:#fff;
classDef db fill:#22c55e,color:#fff;
class A,B,C core;
class D,E,F,G,H,I core;
class K,L ext;
class J db;

⸻

🧠 Architecture Explanation

🔹 Client Layer

* Built with Next.js
* Handles UI, state, and API calls

🔹 API Layer

* Central entry point (Express)
* Routes requests to modules

🔹 Backend Modules

* Auth → authentication & JWT
* User → profile & calorie logic
* Meal → food tracking
* Water → hydration tracking
* AI → food analysis
* Notification → reminders

🔹 Database

* PostgreSQL via Prisma
* Stores all persistent data

🔹 External Services

* AI → OpenAI / Gemini
* Notifications → Firebase

⸻

📁 Project Structure

fitness-app/
├── apps/
│   ├── client/
│   └── server/
├── packages/
│   ├── ui/
│   ├── types/
│   └── config/
├── prisma/

⸻

⚙️ Getting Started

1. Install pnpm

npm install -g pnpm

2. Install dependencies

pnpm install

3. Setup environment variables

DATABASE_URL=
JWT_SECRET=
OPENAI_API_KEY=

4. Run development

pnpm dev

⸻

🗄️ Database

Using Prisma ORM with PostgreSQL.

npx prisma migrate dev

⸻

🤖 AI Usage

AI is used for:

* Parsing food descriptions
* Estimating calories

⚠️ AI is NOT the source of truth.

⸻

🚀 Deployment

Frontend

* Vercel

Backend

* Railway / Render

Database

* Supabase

⸻

🧪 MVP Definition

* User can register/login
* Set calorie target
* Add meals
* Track calories
* Track water intake

⸻

📌 Future Improvements

* Image recognition
* Barcode scanning
* Health integrations
* AI recommendations
