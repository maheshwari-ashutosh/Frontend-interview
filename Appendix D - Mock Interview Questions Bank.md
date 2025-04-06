# Appendix D: Mock Interview Questions Bank

This appendix provides a curated collection of mock interview questions designed to simulate the types of challenges you might encounter during senior frontend interviews. Use these questions to practice your problem-solving skills, articulate your thought processes, and refine your communication. Remember, the goal isn't just to get the "right" answer, but to demonstrate your expertise, reasoning, and approach.

---

#### A. Coding Challenge Examples (Varying Difficulty)

These challenges test your practical JavaScript, HTML, and CSS skills, often within a specific time limit. Focus on writing clean, efficient, and maintainable code. Explain your approach and trade-offs as you code.

**1. Warm-up / Foundational (Typically 15-30 minutes)**

- **Debounce/Throttle Implementation:**
  - Implement `debounce` and `throttle` utility functions from scratch.
  - Explain the difference between them and provide use cases for each (e.g., handling search input, resizing events, button clicks).
  - Consider edge cases like leading/trailing options.
- **Array Manipulation:**
  - Given an array of objects, write a function to group them by a specific property (e.g., `groupBy(users, 'department')`).
  - Implement a function `deepFlatten` that flattens a deeply nested array.
  - Write a function `uniqueElements` that returns an array containing only the unique elements from an input array, preserving order.
- **Basic DOM Manipulation:**
  - Create a simple "accordion" component using only vanilla JavaScript and CSS. Clicking a header should expand its content and collapse others.
  - Implement a function that takes a CSS selector and highlights all matching elements on the page by adding a specific class.
- **Simple Promise Handling:**
  - Write an async function that fetches data from two different API endpoints concurrently and returns the combined results only after both have successfully resolved. Handle potential errors from either fetch.

**2. Intermediate / Component-Focused (Typically 30-60 minutes)**

- **Autocomplete/Typeahead Component:**
  - Build a functional typeahead input component (HTML, CSS, JS).
  - As the user types, fetch suggestions from a mock API (or a provided list).
  - Display suggestions, allow navigation with arrow keys, and selection with Enter key or click.
  - Consider debouncing input, handling loading states, and error states. Accessibility (ARIA attributes) is a plus.
- **Modal/Dialog Component:**
  - Create a reusable modal component.
  - It should be triggerable via a button click.
  - Include features like closing via an overlay click, an explicit close button, and the Escape key.
  - Manage focus trapping within the modal for accessibility.
  - Style it appropriately using CSS.
- **Star Rating Component:**
  - Build a star rating component (e.g., 1-5 stars).
  - Allow users to select a rating by clicking or hovering.
  - Persist the selected rating.
  - Ensure it's keyboard accessible.
- **Data Transformation and Rendering:**
  - Given a nested data structure representing comments and replies, render it as a threaded comment view in the DOM.
  - Implement functionality to toggle the visibility of replies for each comment.
- **Implement `Promise.allSettled`:**
  - Write a function that mimics the behavior of `Promise.allSettled`, taking an array of promises and resolving with an array of status objects (indicating fulfilled or rejected) once all input promises have settled.

**3. Advanced / Algorithmic / Architectural (Typically 45-75 minutes)**

- **Simple Virtual DOM Implementation:**
  - Implement a basic `createElement` function (similar to React's) that returns a virtual node object (e.g., `{ type: 'div', props: { id: 'foo' }, children: [...] }`).
  - Implement a basic `render` function that takes a virtual node and mounts it into a real DOM container.
  - (Advanced) Implement a basic `diff` and `patch` function that compares two virtual trees and applies the minimal necessary changes to the real DOM.
- **Build a Simple Data Grid:**
  - Create a data grid component that takes an array of objects and column definitions.
  - Render the data in a table.
  - Implement client-side sorting by clicking column headers.
  - Implement client-side filtering based on a text input.
  - Consider performance for large datasets (e.g., basic virtualization or pagination).
- **Implement a Basic Client-Side Router:**
  - Using the History API (`pushState`, `popstate`), create a simple client-side router.
  - Define routes that map URL paths to specific rendering functions or components.
  - Handle navigation between routes without full page reloads.
- **DOM Traversal/Manipulation Challenge:**
  - Write a function that takes two DOM nodes as input and finds their lowest common ancestor in the DOM tree.
  - Implement a function `highlightText(searchTerm, containerNode)` that finds all occurrences of `searchTerm` within the text content of `containerNode` and its descendants, wrapping each occurrence in a `<mark>` tag without breaking existing DOM structure.
- **Frontend Performance Optimization Task:**
  - Given a sample code snippet (e.g., a React component fetching and rendering a large list) that is demonstrably slow, identify performance bottlenecks.
  - Refactor the code to improve performance using techniques like memoization (`useMemo`, `useCallback`), virtualization, code splitting, or optimizing data fetching. Explain your reasoning.

---

#### B. Frontend System Design Prompts

These prompts assess your ability to design scalable, maintainable, and performant frontend architectures. Focus on requirements gathering, component breakdown, state management strategy, API design considerations, performance, accessibility, and trade-offs.

- **Design a News Feed (like Twitter/Facebook/LinkedIn):**
  - _Core Features:_ Infinite scrolling, posting updates, displaying posts (text, images, videos), liking/commenting.
  - _Considerations:_ Real-time updates (WebSockets vs. polling), rendering performance for potentially thousands of items, state management complexity, API design (pagination, data structure), optimizing media loading, offline support.
- **Design an E-commerce Product Page (like Amazon):**
  - _Core Features:_ Product image gallery (thumbnails, zoom), product details (name, price, description), variant selection (size, color), add-to-cart functionality, customer reviews section.
  - _Considerations:_ State management for variants and cart, performance optimization for images, SEO, accessibility for interactive elements, A/B testing infrastructure, API design for product data and reviews.
- **Design a Collaborative Text Editor (like Google Docs - Frontend Focus):**
  - _Core Features:_ Rich text editing (bold, italics, lists), multiple users editing simultaneously, showing cursor positions of other users, real-time saving.
  - _Considerations:_ Real-time synchronization (Operational Transformation vs. CRDTs), handling conflicts, state management for complex document structure, rendering performance for large documents, cursor presence implementation, WebSocket communication.
- **Design a Video Streaming Platform UI (like Netflix/YouTube):**
  - _Core Features:_ Browsing content (carousels, categories), video player controls (play/pause, volume, fullscreen, seeking), user authentication, personalized recommendations.
  - _Considerations:_ Performance of carousels with many items (lazy loading, virtualization), state management for player and user session, adaptive bitrate streaming integration (frontend controls), API design for content discovery and playback, accessibility of player controls.
- **Design a Real-time Dashboard (like a Stock Ticker or Analytics Dashboard):**
  - _Core Features:_ Displaying various charts and data points, real-time updates pushed from the server, user-configurable widgets/layout.
  - _Considerations:_ Choosing a real-time communication method (WebSockets, Server-Sent Events), efficient rendering of frequent updates (throttling, batching), state management for diverse data sources, charting library selection and integration, performance optimization for rendering many data points.
- **Design a Micro-Frontend Architecture for a Large Portal:**
  - _Core Features:_ A shell application managing routing and shared services, independently deployable feature modules (e.g., profile, search, settings).
  - _Considerations:_ Framework choices (single vs. multiple), communication between micro-frontends (events, custom elements, window), shared component libraries, routing integration, managing shared state/authentication, build/deployment strategy, performance implications (bundle size).
- **Design an Offline-First E-commerce Wishlist Feature:**
  - _Core Features:_ Users can add/remove items to a wishlist even when offline. Changes are synced when connectivity returns.
  - _Considerations:_ Service Workers for caching and offline access, client-side storage (IndexedDB), synchronization strategies (background sync), conflict resolution (if applicable), UI feedback for offline status and syncing progress.

---

#### C. Behavioral Interview Questions (Mapped to Competencies)

These questions assess your soft skills, experience, and fit for a senior role. Use the STAR method (Situation, Task, Action, Result) to structure your answers, providing specific examples from your past experience.

| Competency                   | Sample Questions                                                                                                                                                                                                                                                                                                                                                                                                                       | What Interviewers Look For                                                                                                                              |
| :--------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Technical Leadership**     | - Tell me about a time you mentored a junior engineer. What was your approach, and what was the outcome? <br/> - Describe a situation where you influenced the technical direction of a project or team. <br/> - How do you advocate for technical best practices (e.g., testing, code quality) within your team? <br/> - Describe a time you had to make a difficult technical decision with incomplete information.                  | Mentoring ability, technical vision, ability to influence others, advocacy for quality, sound judgment, strategic thinking.                             |
| **Problem Solving**          | - Describe the most complex technical challenge you've faced recently. How did you approach it, and what was the solution? <br/> - Tell me about a time you had to debug a critical production issue under pressure. <br/> - How do you approach breaking down a large, ambiguous feature into smaller, manageable tasks? <br/> - Walk me through your process for troubleshooting a performance bottleneck in a frontend application. | Analytical skills, systematic debugging process, ability to handle complexity and ambiguity, root cause analysis, practical problem-solving techniques. |
| **Communication**            | - How do you explain complex technical concepts to non-technical stakeholders (e.g., product managers, designers)? <br/> - Describe a time you had a technical disagreement with a colleague. How did you resolve it? <br/> - How do you effectively document your technical designs or decisions? <br/> - How do you provide constructive feedback on a code review?                                                                  | Clarity, conciseness, active listening, empathy, ability to tailor communication to the audience, conflict resolution skills, written communication.    |
| **Collaboration & Teamwork** | - Tell me about a project where you collaborated closely with backend engineers, designers, and product managers. What was your role, and how did you ensure smooth collaboration? <br/> - Describe a time you had to work with a difficult team member. How did you handle the situation? <br/> - How do you contribute to a positive and inclusive team environment?                                                                 | Team player attitude, cross-functional collaboration skills, conflict management, building relationships, contributing to team health.                  |
| **Adaptability & Learning**  | - How do you stay up-to-date with the rapidly evolving frontend ecosystem? <br/> - Tell me about a time you had to quickly learn a new technology or framework for a project. <br/> - Describe a situation where project requirements changed significantly mid-way. How did you adapt? <br/> - Tell me about a mistake you made and what you learned from it.                                                                         | Curiosity, continuous learning mindset, resilience, ability to handle change, self-awareness, growth mindset.                                           |
| **Ownership & Initiative**   | - Describe a time you took initiative to improve a process, tool, or feature beyond your assigned tasks. <br/> - Tell me about a time you identified and fixed a critical bug or performance issue proactively. <br/> - How do you ensure the quality and reliability of the code you ship? <br/> - Describe a project you owned from conception to delivery. What were the biggest challenges?                                        | Proactiveness, accountability, commitment to quality, driving projects forward, sense of responsibility, impact-oriented.                               |
| **Impact & Results**         | - Tell me about a project you worked on that had a significant positive impact on users or the business. What was your contribution? <br/> - How do you measure the success of the features you build? <br/> - Describe a time you significantly improved the performance or user experience of an application.                                                                                                                        | Focus on outcomes, understanding business value, data-driven decision making, quantifying impact, user-centricity.                                      |

---

#### D. Framework-Specific Deep Dive Questions

These questions probe your in-depth understanding of the specific frameworks, libraries, and tools mentioned in your resume or required for the role. Expect questions about internals, trade-offs, best practices, and common pitfalls.

**React**

- Explain the React reconciliation algorithm (virtual DOM diffing). How does React determine when and how to update the actual DOM?
- What are React Hooks? Explain the rules of Hooks. Why are they important?
- Deep dive into `useState`, `useEffect`, `useContext`, `useReducer`, `useCallback`, `useMemo`. When and why would you use each? Provide examples of misuse.
- How does the Context API work? What are its performance implications compared to libraries like Redux or Zustand? When would you choose one over the other?
- What are Higher-Order Components (HOCs) and Render Props? How do they compare to Hooks for sharing logic?
- Explain Server Components vs. Client Components in React (especially with Next.js). What are the trade-offs?
- How would you optimize the performance of a large React application? (Code splitting, memoization, virtualization, lazy loading, analyzing bundle size).
- How does error handling work in React? (Error Boundaries).
- Discuss state management strategies in large React applications (Context, Redux, Zustand, Jotai, etc.). What factors influence your choice?

**Angular**

- Explain Angular's change detection mechanism (NgZone, default vs. OnPush). How can you optimize it?
- What is Dependency Injection (DI) in Angular? How does it work (Injectors, Providers)? What are its benefits?
- Explain the difference between Angular Modules (NgModule) and Standalone Components. What are the advantages of the standalone approach?
- What is RxJS, and how is it used heavily in Angular (e.g., HttpClient, Router, reactive forms)? Explain operators like `map`, `filter`, `switchMap`, `mergeMap`, `takeUntil`.
- How do you handle state management in complex Angular applications (Services with Subjects, NgRx, NGXS)? Discuss the pros and cons.
- Explain Angular lifecycle hooks (e.g., `ngOnInit`, `ngOnChanges`, `ngAfterViewInit`, `ngOnDestroy`). When is each called?
- What are Angular directives (component, structural, attribute)? Provide examples and explain how structural directives like `*ngIf` and `*ngFor` work internally (`<ng-template>`).
- How does routing work in Angular? (RouterOutlet, RouterModule, route guards, lazy loading modules).
- How would you approach performance optimization in an Angular application? (ChangeDetectionStrategy.OnPush, trackBy in `*ngFor`, lazy loading, build optimizer, tree shaking).

**Vue.js**

- Explain Vue's reactivity system. How does it track dependencies and update the DOM when data changes (Proxies in Vue 3 vs. Object.defineProperty in Vue 2)?
- Compare and contrast the Composition API and the Options API. What are the benefits of the Composition API, especially in large applications?
- Explain Vue's lifecycle hooks (e.g., `onMounted`, `onUpdated`, `onUnmounted` in Composition API; `mounted`, `updated`, `beforeDestroy` in Options API).
- What are slots in Vue? How do they enable component flexibility? Explain scoped slots.
- How does routing work in Vue (Vue Router)? (Dynamic routes, nested routes, navigation guards).
- Discuss state management solutions in Vue (Pinia, Vuex). How do they compare? When would you use them?
- What are Vue directives (e.g., `v-if`, `v-for`, `v-bind`, `v-on`, `v-model`)? How would you create a custom directive?
- How can you optimize the performance of a Vue application? (KeepAlive, `v-once`, lazy loading components/routes, virtual scrolling, analyzing bundle size).
- Explain Server-Side Rendering (SSR) concepts in the context of Vue (e.g., using Nuxt.js).

**General Frontend / Tooling / Concepts**

- Explain the differences between `null`, `undefined`, and undeclared variables in JavaScript.
- What is the Event Loop? Explain how asynchronous operations (callbacks, Promises, async/await) work in JavaScript.
- Describe different ways to handle `this` context in JavaScript ( `bind`, `call`, `apply`, arrow functions).
- What are Promises? Explain `Promise.all`, `Promise.race`, `Promise.allSettled`, `Promise.any`. How do they differ from `async/await`?
- What are Web Components (Custom Elements, Shadow DOM, HTML Templates)? How do they compare to framework components?
- Explain the critical rendering path. How can you optimize it? (Minimizing render-blocking resources, optimizing CSS delivery, etc.).
- Discuss different CSS layout techniques (Flexbox, Grid). When would you use one over the other?
- What is BEM (Block, Element, Modifier) or other CSS methodologies? Why are they useful?
- Explain the purpose of tools like Webpack, Vite, Rollup, or Parcel. What are the key differences between them (e.g., Vite's native ESM dev server)?
- What is tree shaking? How does it work?
- Discuss TypeScript: What are its benefits? Explain key features like interfaces, types, generics, enums, utility types.
- How do you ensure web accessibility (A11y) in your applications? (Semantic HTML, ARIA attributes, keyboard navigation, color contrast).
- What are common frontend security vulnerabilities (XSS, CSRF)? How do you mitigate them?
