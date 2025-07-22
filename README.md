🎯 Customer Behavioral Analytics & Churn Prediction
Hi there! 👋
Welcome to my project Customer Behavioral Analytics & Churn Prediction, where I’ve tried to bring data, machine learning, real-time pipelines, and dashboards all together to understand customer behavior and predict churn — in a way that’s both smart and actionable.

This project walks through everything — from collecting the data, streaming it, training a model, deploying it via API, and finally visualizing insights using Power BI.

🚀 What’s This Project About?
Objective: To predict whether a customer will churn (leave the service) based on their behavior like clicks, purchases, login activity, feedback, etc.

Whether you’re a data science enthusiast, recruiter, or fellow developer — this walkthrough shows how I went from raw simulated data to actionable dashboards in a real-time system.

 Project Roadmap
🏁 Phase 1: Data Understanding & Collection
  I started by thinking through: What kind of customer behaviors actually matter?

  This included data like:

   Click counts

   Purchase history

   Session duration

   Support tickets

   Feedback scores

Since real-time customer data wasn’t available, I created dummy data manually and saved it as a CSV.

🔄 Phase 2: Real-Time Data Ingestion
To simulate real-time behavior, I used Apache Kafka.

The CSV from Phase 1 acted as input.

Wrote a Kafka Producer to stream the rows one by one.

A Kafka Consumer captured the data and stored it in MongoDB — our centralized NoSQL database.

🧠 Phase 3: Churn Prediction Model
Once the data was in MongoDB, I built a machine learning classification model.

The model predicts:

1 → The customer is likely to churn

0 → The customer is likely to stay

The model was trained using behavioral features from MongoDB.

🌐 Phase 4: Model API Deployment
I wanted the model to serve predictions in real time.

So I created an API using Flask, and exposed it publicly using Ngrok.

Here's what happens:

API fetches only new records from MongoDB.

Makes churn predictions using the model.

Saves the results into a new CSV file.

Automatically uploads the CSV to Google Drive for dashboard use.

📊 Phase 5: Power BI Dashboard
This phase turned raw predictions into interactive dashboards.

Power BI is connected directly to the Google Drive CSV.

The moment new predictions are uploaded, you just need to hit the refresh button, and voilà — the dashboard updates!

This setup lets me track churn data hourly, daily, or on demand.
