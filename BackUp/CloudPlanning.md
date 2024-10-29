## **Updated Plan with Cloud Run**

### **Infrastructure Overview with Cloud Run**  
- **Backend APIs:** Spring Boot services deployed to Cloud Run.
- **Frontend:** React served from Cloud Run (or Firebase Hosting).
- **PostgreSQL:** Managed with **Google Cloud SQL**.
- **Redis:** Use **Redis locally** (students) and migrate to **Redis Cloud Memorystore** for production.
- **Messaging:** Use **Google Pub/Sub** for notifications.
- **Storage:** Store uploaded files and images in **Google Cloud Storage**.

---

### **Week-by-Week Plan with Cloud Run**

---

### **Week 1: Local Setup and Basic Project Structure**  
#### **Cloud Admin Tasks:**
- Set up **Google Cloud Project** and **billing**.
- Create **PostgreSQL Cloud SQL** instance and share connection strings.
- Deploy a simple **Spring Boot backend API** on Cloud Run to verify deployment.
- Enable **Cloud Build** to automate deployments from GitHub to Cloud Run.
- Create **Cloud Storage** buckets for future profile uploads.

#### **Student Focus:**
- Set up **React and Spring Boot** locally.
- Configure **PostgreSQL** locally or use the **Cloud SQL instance**.
- Push code to GitHub and integrate with **Cloud Build** for CI/CD.

---

### **Week 2: Authentication and User Profiles**  
#### **Cloud Admin Tasks:**
- Set up **Google Identity Services** for OAuth2.0 login.
- Deploy **JWT-based authentication** service to Cloud Run.
- Prepare a **Cloud Storage bucket** for profile picture uploads.

#### **Student Focus:**
- Implement **JWT authentication** with Spring Security.
- Add **login and registration APIs** to the backend.
- Connect profile uploads to **local storage** and test uploading files to **Cloud Storage**.

---

### **Week 3: CRUD Operations and Timeline**  
#### **Cloud Admin Tasks:**
- Deploy **CRUD APIs** for tweets on Cloud Run.
- Set up **Google Pub/Sub** topics for notifications.
- Monitor API usage via **Cloud Monitoring** to track load.

#### **Student Focus:**
- Implement CRUD operations for **tweets** and **user timelines**.
- Use **Kafka locally** to simulate message queues.
- Deploy frontend components with **pagination** to Cloud Run.

---

### **Week 4: User Relationships and Search Functionality**  
#### **Cloud Admin Tasks:**
- Set up a **Cloud Pub/Sub topic** for real-time messaging.
- Deploy **search functionality** to Cloud Run using SQL queries on Cloud SQL.

#### **Student Focus:**
- Develop **Follow/Unfollow APIs**.
- Implement **search bar** with local SQL queries and integrate with the frontend.
- Prepare **adjacency lists** to represent user relationships.

---

### **Week 5: Caching, Load Balancing, and Monitoring**  
#### **Cloud Admin Tasks:**
- Enable **Redis Cloud Memorystore** for caching tweets and sessions.
- Set up **Nginx load balancing** (optional) for performance testing.
- Use **Cloud Monitoring and Cloud Trace** for request monitoring.

#### **Student Focus:**
- Set up **Redis caching** locally.
- Add **caching strategies** to timeline APIs.
- Use **Zipkin tracing** locally to monitor requests.

---

### **Week 6: Scaling and Optimization**  
#### **Cloud Admin Tasks:**
- Configure **Cloud Run autoscaling** with limits to prevent cost overrun.
- Implement **consistent hashing** logic in code to simulate load balancing.
- Optimize Cloud SQL queries with **indexes** for faster retrieval.

#### **Student Focus:**
- Implement **sharded counters** for likes/retweets locally.
- Simulate **high-traffic scenarios** in local environments.
- Use **profiling tools** to optimize backend code.

---

### **Week 7: Testing, Debugging, and Deployment**  
#### **Cloud Admin Tasks:**
- Set up **CI/CD pipelines** using **Cloud Build and GitHub Actions**.
- Automate deployments to Cloud Run for both frontend and backend.
- Monitor logs via **Cloud Logging** to debug performance issues.

#### **Student Focus:**
- Write **unit and integration tests** using **Jest** (frontend) and **JUnit** (backend).
- Conduct **load testing** with **JMeter** locally.
- Ensure the application deploys smoothly with **Docker Compose**.

---

### **Week 8: Final Review and Wrap-up**  
#### **Cloud Admin Tasks:**
- Conduct a **final walkthrough** of the cloud setup.
- Demonstrate **system architecture** using Cloud Run, Cloud SQL, Pub/Sub, and Redis.
- Review **performance and scalability trade-offs** with students.

#### **Student Focus:**
- Document the project and submit **code to GitHub**.
- Present the final application and **reflect on DSA concepts** used throughout.

---


---

## **Other Recommendations**  
1. **Firebase Hosting for Frontend:**  
   - If React is static, consider hosting it on **Firebase Hosting** instead of Cloud Run for better performance and lower costs.

2. **Secrets Management:**  
   - Use **Google Secret Manager** to store sensitive data like API keys.

3. **Alerting and Monitoring:**  
   - Set up **alerts** for Cloud SQL and Cloud Run to monitor resource usage and prevent cost overruns.

4. **Cloud Scheduler:**  
   - Use **Google Cloud Scheduler** to automate tasks like database backups.

5. **Local Development with Docker Compose:**  
   - Encourage students to use **Docker Compose** locally to simulate cloud environments and ensure easy deployment.

---

### **Conclusion**  
This **Cloud Run-based setup** simplifies deployment, reduces costs, and allows students to focus on coding without worrying about complex infrastructure management. You, as the **cloud admin**, can handle deployments and demos smoothly using **Cloud Run, Cloud SQL, Pub/Sub**, and **Redis**, ensuring that the project scales efficiently.
