

# Interview questions

---

### Core JavaScript & Advanced Concepts

1. Explain the **Execution Context** and how the **Call Stack** manages function calls in JavaScript.
2. How does **Hoisting** differ between `var`, `let`, and `const`?
3. Describe a real-world scenario where you used a **Closure** to solve a problem.
4. What is **Prototypal Inheritance**, and how does it differ from Class-based inheritance?
5. Explain the **Event Loop**. How do Microtasks (Promises) and Macrotasks (setTimeout) prioritize?
    
    +1
    
6. How do you implement **Debouncing** and **Throttling** to optimize high-frequency events?
7. What is **Currying**, and how can it help in creating reusable utility functions?
8. Explain the difference between **Shallow Copy** and **Deep Copy**. How do you handle circular references?
9. How does `async/await` handle errors differently than `.then().catch()`?
10. Describe **Memory Management** in JS. What are common causes of memory leaks in a SPA?

### Frontend & React (Next.js Focus)

1. Compare **Virtual DOM vs. Real DOM**. When does the reconciliation process actually trigger?
2. Why is the **Key prop** critical for performance in list rendering?
    
    +1
    
3. How do you decide between using `useMemo` and `useCallback`?
4. Explain **Code Splitting** and **Lazy Loading** in the context of Next.js.
5. What are **Error Boundaries**, and why should you use them in a production app?
6. How do you handle **Role-based Authorization** using Next.js Middleware?
7. Explain the benefits of **Server-Side Rendering (SSR)** vs. **Static Site Generation (SSG)** for SEO.
    
    +1
    
8. How does **TanStack React Query** solve the problem of "Server-State" management?
9. Describe your approach to **Optimistic Updates** in a UI.
10. Why is a **Feature-based architecture** more scalable than a simple folder structure?
11. How do you implement a **Centralized API abstraction layer**?
12. What is **Hydration** in React, and what causes "Hydration mismatch" errors?
13. How do you manage global state without "Prop Drilling" in a large application?
14. Explain **Controlled vs. Uncontrolled components** in the context of complex forms.
15. How do you enforce **Strict TypeScript typing** between frontend and backend contracts?
- **The "Why":** Why use TanStack Query instead of a global state manager like Redux or the Context API for server data?
- **Stale-While-Revalidate:** Explain how `staleTime` and `gcTime` (formerly cacheTime) work together to improve user experience.
- **Server-Side Logic:** How do you handle TanStack Query in the Next.js App Router, specifically with **Hydration**?
    
    +1
    
- **Optimistic Updates:** Describe the steps to implement an optimistic update where the UI changes before the server confirms the success.
- **Manual Invalidation:** When and how would you use `queryClient.invalidateQueries` to ensure the user sees the latest data?

### Backend (Node, Express, & Architecture)

1. Describe the **Repository-based structure**. Why is it better than putting logic in controllers?
2. How does the **Event-driven architecture** of Node.js allow it to handle high concurrency?
3. What is **Middleware chaining**, and how do you pass data between middleware?
4. Explain the **JWT Authentication flow**, including the use of Access and Refresh tokens.
5. Why is **Password Salting** necessary alongside Hashing (Bcrypt)?
    
    +2
    
6. How do you design a **RESTful API** that is truly "Resource-oriented"?
7. What is **CORS**, and how do you securely configure it for a production environment?
    
    +1
    
8. How do you use **Express Validation** to protect your controllers from bad data?
9. What are the pros and cons of **Microservices vs. Monoliths** for a 2-year experienced dev?
10. How do you handle **Global Error Handling** in an Express application?
11. **Latency Optimization:** How did the implementation of a message queue specifically reduce your API latency to 100ms?
- **Worker Threads vs. Event Loop:** Why did you use Node workers for the message queue instead of just letting the standard asynchronous event loop handle it?
- **Failure Handling:** In your message queue architecture, what happens if a "worker" picks up a job but the process crashes before completion?
- **Priority Queuing:** How do you distinguish between a "low priority task" and a critical task within your queue system?
- **Multithreaded Work:** Explain how data is passed between the main thread and a Node worker thread without shared memory issues.

---

### Database & Performance (MongoDB & Redis)

1. What is the **N+1 Query problem**, and how do you solve it using **Aggregation Pipelines**?
2. When should you use a **Reference Schema** vs. an Embedded Document in MongoDB?
3. How does **Database Indexing** work, and when can it actually slow down your DB?
4. How did you implement **Redis** to achieve fast response times?
5. Explain the role of **Message Queues** (like Node Workers) in reducing API latency.
    
    +1
    
6. What is the difference between a **Document and a Collection** in MongoDB?
7. How do you handle **Database Migrations** in a NoSQL environment?
8. Describe a **complex database design** you have worked on.
9. How do you implement **Rate Limiting** to prevent API abuse?
10. What are **AWS S3 Presigned URLs**, and why are they safer for file uploads?

### Project & Behavioral

1. Walk me through the **folder structure** of your most recent professional project.
2. What was the most **difficult bug** you faced, and how did you debug it?
3. Why did you choose **Next.js App Router** over the traditional Pages router?
4. How do you ensure your code is **maintainable** for other developers?
    
    +2
    
5. Explain a time you had to **optimize a slow API** or a slow-rendering component.
    
    +1
    

---

## Machine Coding Round Questions (20 Tasks)

These tasks evaluate your ability to write clean, modular, and typed code within a 60–90 minute window.

### Frontend (React/Next.js)

1. **Search Bar with Debouncing:** Build a search input that calls a dummy API and displays results, ensuring the API is not spammed.
2. **Infinite Scroll Component:** Implement a list that loads more data as the user scrolls, using the `Intersection Observer API`.
3. **Custom Modal System:** Build a reusable Modal using React Portals and a custom hook (`useModal`).
    
    +1
    
4. **Multi-step Form:** Create a form with validation at each step and "Lifting State Up" to a parent component.
5. **TanStack Query Integration:** Fetch a list of users, implement "Click to Retry" on error, and cache the results.
6. **Theme Switcher:** Implement a Dark/Light mode toggle using React Context and CSS Variables.
7. **Dynamic Filter Gallery:** A list of items with multiple categories; filtering should update the URL (query params).
8. **Optimistic UI Task List:** A Todo list where items appear instantly on "Add," but revert if the API call fails.
9. **Image Gallery with Lazy Loading:** Use `React.lazy` and `Suspense` to load heavy components/images.
10. **Role-based Sidebar:** Build a navigation component that renders different links based on a "User Role" object.

### Backend (Node/Express/MongoDB)

1. **Rate Limiter Middleware:** Write a custom Express middleware to limit a user to 5 requests per minute.
2. **JWT Auth Scaffolding:** Implement `/register`, `/login`, and a `/protected` route using Bcrypt and JWT.
    
    +1
    
3. **File Upload to S3:** Create an endpoint that generates a **Presigned URL** for a client to upload a profile picture.
4. **Aggregation Pipeline Task:** Given a "Sales" collection, write a query to find the top 3 customers by total spend.
5. **Repository Pattern Implementation:** Refactor a simple "User CRUD" controller into a Repository + Service pattern.
6. **Bulk Data Import:** Create an API that accepts a JSON array and performs a `bulkWrite` to MongoDB safely.
7. **Middleware Chaining:** Create three middlewares (Logger, Auth, Validator) and chain them on a specific route.
8. **Redis Caching Layer:** Wrap a slow "Get Product" API with Redis to cache results for 60 seconds.
9. **Worker Thread Logic:** Offload a "Heavy PDF Generation" task to a Node Worker thread to keep the main thread free.
10. **Zod/Joi Validation:** Implement strict request body validation for a complex "Job Application" schema.