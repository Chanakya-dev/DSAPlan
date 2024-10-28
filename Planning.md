## **Frontend vs. Backend: Data Structures & Algorithms (DSA) Usage**

---

### **Week 1: User Profiles and Authentication (Auth Microservice)**

#### **Frontend (React):**
- **Hash Maps:** Manage form state (e.g., username-password pairs) using state objects.
- **Form Validation Algorithms:** Validate user input on the frontend before sending requests (e.g., regex for email validation).

#### **Backend (Spring Boot):**
- **Hash Maps:** Store user sessions and tokens in-memory.
- **Encryption Algorithms:** Use hashing algorithms (e.g., BCrypt) for password encryption.
- **Trees (JWT Parsing):** Parse JSON Web Tokens (JWT) as part of authentication.

---

### **Week 2: Tweet Posting and Retrieval (Tweet Microservice)**

#### **Frontend (React):**
- **Arrays:** Store tweets and dynamically render them in the feed.
- **Sorting Algorithms:** Apply sorting (e.g., by timestamp) to display the latest tweets first.

#### **Backend (Spring Boot):**
- **B-Trees / Indexes:** Store and query tweets efficiently in the database.
- **Linked Lists:** Store tweets in order of posting.
- **Pagination Algorithms:** Implement pagination for tweet retrieval (e.g., returning 10 tweets per page).

---

### **Week 3: Following System (Follow Microservice)**

#### **Frontend (React):**
- **Graphs (Adjacency List Representation):** Maintain local state of user relationships (followers/following).
- **Debounce/Throttling Algorithms:** Optimize API calls when users perform actions like follow/unfollow.

#### **Backend (Spring Boot):**
- **Graphs (Adjacency List):** Store and manage user relationships.
- **Hash Maps:** Cache relationship lookups to improve performance.
- **Graph Traversal Algorithms (BFS/DFS):** Use for suggesting mutual followers.

---

### **Week 4: Timeline Feed Generation (Feed Microservice)**

#### **Frontend (React):**
- **Priority Queue:** Use local state to manage and render sorted tweets.
- **Merge Sort:** Implement sorting within components to merge multiple tweet lists for display.
  
#### **Backend (Spring Boot):**
- **Priority Queue / Heap:** Efficiently manage and sort tweets by timestamp.
- **Merge Sort Algorithm:** Merge tweets from followed users into a single feed.
- **Caching Algorithms:** Use **Redis** to cache sorted feed data.

---

### **Week 5: Hashtags and Search Functionality (Search Microservice)**

#### **Frontend (React):**
- **Trie Data Structure:** Handle hashtag autocomplete on the frontend.
- **Inverted Index (Search State):** Store local search results for quick re-rendering.
- **Search Algorithms:** Implement keyword-based search filtering on the frontend.

#### **Backend (Spring Boot):**
- **Trie:** Store hashtags for efficient prefix-based search.
- **Inverted Index:** Map keywords/hashtags to relevant tweets.
- **Search Query Optimization Algorithms:** Efficiently retrieve search results from the backend.

---

### **Week 6: Integration, Review, and Cloud Deployment**

#### **Frontend (React):**
- **Sets:** Track the state of active users and microservice statuses in the UI.
- **Local Caching (LRU Cache):** Implement caching for frequently accessed UI components (e.g., timelines).

#### **Backend (Spring Boot):**
- **Sets:** Track active sessions or services connected.
- **LRU Cache:** Use Redis to cache frequently accessed feed data.
- **Load Balancing Algorithms:** Ensure the backend handles requests efficiently across services in **Google Cloud Run**.

---

## **Summary of DSA Usage Across Frontend & Backend**

| **DSA Concept**          | **Frontend (React)**                                     | **Backend (Spring Boot)**                                  |
|--------------------------|----------------------------------------------------------|-----------------------------------------------------------|
| **Hash Maps**             | Manage form states and API responses                     | Store user sessions, tokens, and cache lookups             |
| **Arrays / Linked Lists** | Render tweets sequentially in the UI                     | Store tweets and retrieve them in order of posting         |
| **Graphs**                | Maintain user relationships (followers/following) locally| Manage user relationships and perform graph traversals     |
| **Priority Queue / Heap** | Sort tweets locally before rendering                     | Manage and sort tweets by timestamp for feeds              |
| **Trie**                  | Handle hashtag autocomplete in the UI                    | Store hashtags and enable efficient prefix-based search    |
| **Inverted Index**        | Store and filter search results locally                  | Map keywords to tweets and optimize backend search queries |
| **LRU Cache**             | Cache UI components and timelines                        | Cache timeline feeds and search results using Redis        |
| **Graph Traversal**       | -                                                        | Suggest mutual followers using BFS/DFS                     |
| **Pagination Algorithms** | Paginate tweets for better UX                            | Implement pagination for API responses                     |
| **Sorting Algorithms**    | Sort tweets by timestamp                                 | Merge and sort tweets from multiple users for feeds        |

