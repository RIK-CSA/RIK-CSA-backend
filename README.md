# Worker Hiring System - Backend API

This repository contains the Java-based backend for the Worker Hiring System. Built with **Spring Boot**, it provides a RESTful interface to manage worker data and utilizes a **K-Nearest Neighbors (KNN)** algorithm to match candidates with employer requirements based on skills and location.

## 🧠 Core Logic: KNN Matching
Unlike simple keyword searches, this backend utilizes a custom `KNNWorkerHiring` utility. This allows the system to find the "closest" matches in a multi-dimensional feature space—such as programming languages known, location, and internship status—providing more intelligent results than a standard database query.



## 🛠️ Tech Stack
* [cite_start]**Language:** Java 11+ 
* [cite_start]**Framework:** Spring Boot 
* [cite_start]**Web:** Spring Web MVC (REST Controller) 
* [cite_start]**Security:** Cross-Origin Resource Sharing (CORS) configured for secure frontend integration 

## 🚀 API Documentation

The `WorkerController` manages all candidate data through the following endpoints:

### 1. Add New Candidate
Allows employers or users to register a new worker profile.
* **Endpoint:** `POST /api/worker/add`
* **Payload:** ```json
{
  "name": "Kevin Du",
  "languagesKnown": ["Java", "Spring Boot", "React"],
  "preferredLocation": "West Lafayette",
  "internshipPreferred": true
}
