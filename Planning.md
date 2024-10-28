

## **6-Week Plan with Data Structures, Local Development, and Cloud Deployment**

---

### **Week 1: User Profiles and Authentication (Auth Microservice)**

#### **Data Structures Used:**
- **Hash Tables/Objects:** Store user credentials and profile information (e.g., username, email, profile picture).
- **Dictionaries in Firebase or SQL:** Map user data efficiently using keys like user ID.

#### **Key Tasks:**
- Use **Firebase Authentication** to manage logins.
- Store user profile information using **MongoDB Atlas** or **SQL**.
- API Endpoints:  
  - `/user/register`, `/user/login`, `/user/profile`

#### **Testing:**
- Test locally with **Postman** to verify login and profile retrieval.
  
---

### **Week 2: Tweet Posting and Retrieval (Tweet Microservice)**

#### **Data Structures Used:**
- **Arrays/Linked Lists:** Store tweets sequentially in the order they are posted.
- **B-Trees:** Use B-Trees or indexes in MongoDB/SQL to retrieve tweets efficiently by timestamp or user ID.

#### **Key Tasks:**
- Implement CRUD operations for tweets.
- Store tweets in **MongoDB/SQL**, indexed by user ID and timestamp.
- API Endpoints:  
  - `/tweet/create`, `/tweet/get/{userId}`, `/tweet/delete`

#### **Testing:**
- Use **Postman** to test CRUD operations.
- Store tweets locally and test sorting and retrieval.

---

### **Week 3: Following System (Follow Microservice)**

#### **Data Structures Used:**
- **Graph (Adjacency List):** Represent user connections (followers and following) as a graph.
- **Hash Maps:** Store follower/following relationships for efficient lookups.

#### **Key Tasks:**
- Implement APIs to manage followers/following.
- Store relationships using **MongoDB** or **SQL** with adjacency lists.
- API Endpoints:  
  - `/follow`, `/followers/{userId}`, `/following/{userId}`

#### **Algorithms:**
- **Graph Traversal (BFS/DFS):** Suggest mutual followers or connections.

#### **Testing:**
- Use **Postman** to test follow APIs.
- Verify graph-based queries locally.

---

### **Week 4: Timeline Feed Generation (Feed Microservice)**

#### **Data Structures Used:**
- **Priority Queue/Heap:** Sort and display tweets based on timestamps in the timeline feed.
- **Merge Sorted Arrays:** Merge tweets from multiple followed users into a single timeline.

#### **Key Tasks:**
- Implement personalized feed aggregation based on follow data.
- Use **Redis** (optional) for caching feed data.
- API Endpoints:  
  - `/feed/{userId}`

#### **Algorithms:**
- **Merge Sort:** Combine tweets from followed users efficiently.

#### **Testing:**
- Use **Postman** to test API responses.
- Verify sorting with different timestamps.

---

### **Week 5: Hashtags and Search Functionality (Search Microservice)**

#### **Data Structures Used:**
- **Trie:** Store hashtags for fast autocomplete and prefix matching.
- **Inverted Index:** Map keywords and hashtags to relevant tweets for search.

#### **Key Tasks:**
- Implement search with hashtags and autocomplete.
- Store hashtags in a **Trie** data structure for autocomplete.
- Use **Inverted Index** for fast keyword-based search.
- API Endpoints:  
  - `/search?q={query}`

#### **Algorithms:**
- **Trie Traversal:** Provide real-time hashtag suggestions.
- **Search Query Optimization:** Query tweets efficiently based on keywords.

#### **Testing:**
- Use **Postman** to test search and autocomplete functionality.
- Validate index-based search locally.

---

### **Week 6: Integration, Review, and Cloud Deployment**

#### **Data Structures Used:**
- **Set:** Track active users and connected microservices.
- **Cache (LRU Cache):** Use **Redis** to cache frequently accessed data like timelines.

#### **Key Tasks:**
- Integrate all microservices locally.
- Test all endpoints and connections between services using **Postman collections**.
- Optimize performance with **Redis caching**.
- Deploy microservices to **Google Cloud Run** with CI/CD pipelines using **GitHub Actions**.

#### **Testing:**
- Perform **unit tests** and **integration tests** locally using **Jest** or **PyTest**.
- Test API interactions between microservices locally before deployment.

---

## **Summary of Data Structures Used Across the Plan**

1. **Week 1: Hash Tables/Objects** – Efficient user data storage and access.
2. **Week 2: Arrays/Linked Lists, B-Trees** – Tweet storage and retrieval.
3. **Week 3: Graph (Adjacency List), Hash Maps** – Manage follower/following relationships.
4. **Week 4: Priority Queue/Heap, Merge Sort** – Timeline feed sorting and aggregation.
5. **Week 5: Trie, Inverted Index** – Hashtag search and autocomplete.
6. **Week 6: Sets, LRU Cache** – Active users tracking and data caching.

---

## **Development Workflow**

### **Local Development:**
- Use **MongoDB Atlas** or **SQL** for local testing.
- Each microservice is containerized with **Docker** for easy setup.
- Use **Postman** to test API endpoints during development.

### **Cloud Deployment:**
- Deploy each microservice on **Google Cloud Run** using **GitHub Actions** for CI/CD.
- Use **Redis** for caching timeline feeds and search queries.

