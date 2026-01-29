# TMS Foundation - Architecture & Technical Assignment

## Introduction 
This repository contains my reponses to the assignment shared by TMS Foundation. As a fresher-level developer, my goal is to explain concepts in a clear and practical way, with a focus on real-world usability for a non-profit organization. 

---

## Task 1: Strategic Analysis & Audit

### a) Benefits of Using a Decoupled Architecture (React + Django REST) 

A decoupled architecture means the frontend and backend are developed as separate
applications and communicate using APIs.

A common example of this is React for the frontend and Django REST Framework for
the backend. This approach is beneficial for non-profit organizations because it
allows independent development, easier maintenance, and future scalability.

However, based on my practical experience, a similar and equally effective
approach is using Next.js (React-based framework) for the frontend and Node.js
(Express) for the backend.

For a non-profit platform, this setup is beneficial because:
- Next.js provides built-in routing and performance optimizations.
- Node.js allows faster development using JavaScript across the full stack.
- The frontend and backend remain fully decoupled through REST APIs.
- This stack is easier to manage for small teams or volunteer-based development.

From a fresher’s perspective, this approach is easier to learn and implement while
still following proper architectural separation.

---

### d) Redesign Vision: Interactive React-Based Dashboard

One modern React-based feature that would significantly improve the portal is an interactive dashboard with role-based data and client-site filtering.

In a non-profit portal, users such as administrators, volunteers, and members often need quick access relevant information like activities, tasks, events, or reports. A react-based dashboard can display this information using cards, tables, and simple status indicators.

Using React and Next.js, the dashboard can:
- Fetch data from backend APIs and display it in real time.
- Show different data based on user roles ( admin, volunteer, member).
- Allow users to filter or search data on the client side without reloading the page.
- Provide a smooth and responsive user experience.

From a fresher-level implementation perspective, this feature can be built using React state, effects, and reusable components, making it both practical and scalable for future improvements.


---

## Task 2: Technical Proficiency

### a) Handling CORS in a Django + React Setup

Cross-Origin Resource Sharing (CORS) is a browser security mechanism that restricts
frontend applications from accessing backend APIs hosted on a different origin.

In a React and Django REST setup, CORS issues usually appear when the frontend and
backend are running on different ports or domains, causing the browser to block API
requests even though the backend is working correctly.

From my practical experience, CORS issues are handled mainly on the backend side.
The backend needs to explicitly allow requests coming from the frontend application.

In a Django REST Framework setup, this is commonly handled using a CORS middleware
such as `django-cors-headers`, where trusted frontend origins are added to the allowed
list. During development, allowing all origins helps in faster testing, while in
production, only specific frontend URLs should be allowed for security reasons.

Once the backend allows the frontend origin, the browser permits communication,
and the frontend and backend can exchange data without issues.

---

### b) State Management Choice (useState vs Context/Redux)

In a React-based non-profit platform, the choice of state management depends on the
application size and the type of data being shared across components.

For small and medium-sized features, I prefer using React’s `useState` and `useEffect`
for managing local UI state such as form inputs, loading indicators, and component-level
logic. This approach keeps the code simple and easy to maintain.

When the same data needs to be accessed by multiple components (for example, shared UI
state or common data), the Context API is a better choice. It helps reduce prop drilling
and allows cleaner data sharing without adding extra complexity.

Redux or Redux Toolkit becomes useful only when the application grows significantly and
has complex global state requirements. For a non-profit platform with limited resources
and simpler workflows, Redux can feel like overkill at the early stages and is best
introduced only when scalability demands it.

From my experience, starting with `useState`, then moving


---

## Practical Demonstration

This repository includes a sample folder structure demonstrating a decoupled architecture
where frontend and backend are developed independently.

---

## Conclusion
This assignment helped me understand how frontend and backend separation improves scalability,
maintainability, and collaboration, especially for non-profit platforms.
