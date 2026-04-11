*Self-Directed 4-Week Harvard-Level Curriculum for UNN Computer Science (Year 3)*

You have access to a complete set of lecture notes for *eight 300-level CS courses* plus one entrepreneurship course. Your goal: master the core material and pass your end-of-semester exams. This curriculum condenses a full semester into *4 weeks of intensive study (40–50 hours/week)*. It is designed for an autodidact with discipline, internet access, and an LLM (like me) as a Socratic tutor.

> *How to use this curriculum* 
> Each week has a theme that integrates related courses. Each day you will:  
> 1. Read your provided notes for the specified topics.  
> 2. Watch recommended video lectures (links provided).  
> 3. Work through textbook sections (free PDFs from Libgen/Anna’s Archive).  
> 4. Complete short assignments (problem sets, diagrams, code).  
> 5. Use the LLM to quiz you, explain gaps, and simulate oral exams.  
>  
> At the end of week 4, you will have a *capstone project* and a *mock final exam* for each course.

---

*📚 Core Textbooks (Free from Libgen / Anna’s Archive)*

| Course | Recommended Textbook |
|--------|----------------------|
| *Software Engineering* | *Software Engineering (10th ed.)* – Ian Sommerville |
| *Discrete Structures* | *Discrete Mathematics and Its Applications (8th ed.)* – Kenneth Rosen |
| *Operating Systems* | *Operating System Concepts (10th ed.)* – Silberschatz, Galvin, Gagne |
| *Computer Architecture* | *Computer Organization and Design (RISC-V ed.)* – Patterson & Hennessy |
| *System Analysis & Design* | *Systems Analysis and Design (12th ed.)* – Tilley & Rosenblatt |
| *Object-Oriented Programming* | *Introduction to Java Programming (10th ed.)* – Y. Daniel Liang |
| *Artificial Intelligence* | *Artificial Intelligence: A Modern Approach (4th ed.)* – Russell & Norvig |
| *Entrepreneurship* | *Entrepreneurship (10th ed.)* – Hisrich, Peters, Shepherd |

---

*🗓️ Weekly Schedule (40–50 hours/week)*

*Week 1 – Foundations: Logic, Architecture, and OOP*

| Day | Morning (4h) | Afternoon (4h) | Evening (2h) |
|-----|--------------|----------------|---------------|
| *Mon** | *Discrete Maths* – Boolean algebra, logic gates, De Morgan’s laws (Rosen ch. 12; your COS 311 notes) | *Computer Architecture* – Number systems, logic gates, combinational circuits (Patterson ch. 1–2; your COS 341 notes) | LLM Socratic quiz on Boolean identities & gate design |
| *Tue* | *OOP* – Classes, objects, methods, constructors (Liang ch. 8–9; your COS 361 notes) | *Architecture* – ALU design, sequential logic, registers | Write a simple Java `Student` class with encapsulation |
| *Wed* | *Discrete Maths* – Graph theory (adjacency matrix, Dijkstra, MST) (Rosen ch. 10) | *Architecture* – Instruction formats, addressing modes (Patterson ch. 2) | Solve 3 graph shortest‑path problems (your COS 311 exam questions) |
| *Thu* | *OOP* – Inheritance, polymorphism, overloading (Liang ch. 11) | *Architecture* – Von Neumann model, CPU instruction cycle | Implement a small inheritance hierarchy (e.g., `Shape` → `Circle`, `Rectangle`) |
| *Fri* | *Discrete Maths* – Propositional logic, truth tables, inference rules (Rosen ch. 1) | *Architecture* – Pipelining (Patterson ch. 4; your COS 341 notes) | Draw pipeline diagrams for 5‑stage MIPS |
| *Sat* | *Review & Problem Set* – Complete problem set #1 (logic, graphs, OOP, pipelining) | *LLM session* – Explain your solutions; ask for alternative proofs | *Portfolio* – Begin *Project 1*: Design a 4‑bit ALU in Logisim (or draw logic diagram) |
| *Sun* | Rest / catch‑up | Review weak topics using LLM flashcards | Watch *MIT 6.004 L01–L05* (Computation Structures) |

*Week 2 – Systems: OS, Architecture, and SDLC*

| Day | Morning (4h) | Afternoon (4h) | Evening (2h) |
|-----|--------------|----------------|---------------|
| *Mon* | *Operating Systems* – Process states, PCB, scheduling (FCFS, SJF, RR) (Silberschatz ch. 3–5; your COS 331 notes) | *Architecture* – Memory hierarchy, cache (Patterson ch. 5) | Calculate average access time for cache configurations |
| *Tue* | *OS* – Memory management (paging, segmentation, virtual memory) (Silberschatz ch. 8–9) | *System Analysis* – SDLC models (waterfall, agile, spiral) (Tilley ch. 2–3; your COS 337 notes) | Compare waterfall vs. agile for a real project |
| *Wed* | *OS* – Synchronisation, deadlocks (Silberschatz ch. 6–7) | *System Analysis* – Requirements, fact‑finding (interviews, questionnaires) | Draw a context DFD for a library system |
| *Thu* | *OS* – File systems, I/O (Silberschatz ch. 10, 13) | *Architecture* – Virtual memory, page tables, TLB (Patterson ch. 5; your COS 341 notes) | Solve page replacement problems (FIFO, LRU, optimal) |
| *Fri* | *OS* – Multi‑threading, concurrency (Silberschatz ch. 4) | *System Analysis* – Data flow diagrams, data dictionary, decision trees | Create a decision table for a course registration system |
| *Sat* | *Review & Problem Set* – OS scheduling, paging, deadlock, DFDs | *LLM session* – Role‑play as a system analyst; defend your SDLC choice | *Portfolio* – *Project 2*: Write a report (2 pages) analysing the OS structure of a Linux process |
| *Sun* | Rest / catch‑up | Watch *MIT 6.033 L02–L05* (Operating Systems) | Review OS memory management with LLM flashcards |

*Week 3 – AI & Software Engineering*

| Day | Morning (4h) | Afternoon (4h) | Evening (2h) |
|-----|--------------|----------------|---------------|
| *Mon* | *AI* – Agents, environments, PEAS (Russell & Norvig ch. 2; your COS 335 notes) | *Software Eng.* – UML use‑case, class diagrams (Sommerville ch. 5; your COS 333 notes) | Draw a use‑case diagram for an ATM system |
| *Tue* | *AI* – Uninformed search (BFS, DFS, UCS, IDDFS) (Russell ch. 3) | *Software Eng.* – Sequence, activity, state machine diagrams | Model the “withdraw money” use case with a sequence diagram |
| *Wed* | *AI* – Informed search (A*, greedy) (Russell ch. 3) | *Software Eng.* – ER diagrams, database design (Sommerville ch. 8) | Design an ERD for a hospital management system |
| *Thu* | *AI* – Propositional & first‑order logic, inference (Russell ch. 7–8) | *Software Eng.* – Software testing (verification & validation) (Sommerville ch. 8) | Write black‑box test cases for a temperature converter |
| *Fri* | *AI* – Fuzzy logic, fuzzy systems (your COS 335 notes) | *Software Eng.* – Deployment diagrams, design patterns | Draw a deployment diagram for a web application |
| *Sat* | *Review & Problem Set* – Search algorithms, logic, UML, testing | *LLM session* – Explain A* heuristic admissibility; review your UML models | *Portfolio* – *Project 3*: Implement A* search for a 8‑puzzle (Python or Java) |
| *Sun* | Rest / catch‑up | Watch *MIT 6.034 L01–L05* (AI) | Build an LLM prompt to explain unification in FOL |

*Week 4 – Advanced Topics, Integration & Exam Prep*

| Day | Morning (4h) | Afternoon (4h) | Evening (2h) |
|-----|--------------|----------------|---------------|
| *Mon* | *AI* – Neural networks (perceptron, MLP, backprop) (Russell ch. 21; your COS 335 notes) | *Software Eng.* – Advanced UML (communication, timing, interaction overview) | Hand‑compute one iteration of perceptron learning |
| *Tue* | *AI* – Pattern recognition (k‑NN, decision boundaries) (your COS 335 notes) | *Entrepreneurship* – Opportunity evaluation, business models (Hisrich ch. 4; your CED 341 notes) | Write a one‑page evaluation of a startup idea using RAMP model |
| *Wed* | *AI* – Multi‑layer neural networks, backpropagation (Russell ch. 21) | *Software Eng.* – Software project management, risk analysis | Create a Gantt chart for a small software project (use Excel or draw) |
| *Thu* | *Entrepreneurship* – Intrapreneurship, family business, IPR (your CED 341 notes) | *Integration* – How does virtual memory interact with cache? How does UML support SDLC? | Write short essays (1 page each) linking two courses |
| *Fri* | *Mock Exams* – Take a 3‑hour mock exam covering OS, Architecture, AI, SE (use past questions from your materials) | *Mock Exams* – Take a 3‑hour mock exam covering Discrete Maths, OOP, SAD, Entrepreneurship | Self‑grade with LLM; identify weak areas |
| *Sat* | *Final Review* – Re‑study weak topics using LLM‑generated quizzes and flashcards | *Capstone* – Complete *Project 4* (see below) – a small integrated system | *Portfolio* – Polish all projects and upload to GitHub |
| *Sun* | Rest – do nothing. You have earned it. | Optional: review any remaining exam questions | Prepare for real exams |

---

*📘 Course‑Specific Details*

*1. COS 333 – Software Engineering II*
*Learning Objectives* (from your materials)  
- Draw and interpret UML diagrams: use‑case, class, sequence, activity, state machine, deployment.  
- Apply ER diagrams to design a relational database.  
- Explain and compare SDLC models (waterfall, agile, spiral, V‑model, iterative).  
- Write basic SQL queries and normalise tables to 3NF.  
- Perform software testing (black‑box, white‑box, unit, integration, acceptance).  

*Assignments*  
- Problem set: Convert a textual problem into a complete set of UML diagrams (use‑case, class, sequence).  
- Design a database for a library system (ERD → relational schema → SQL `CREATE TABLE` statements).  
- Write a test plan for a simple calculator (test cases, expected results).  

*Final Exam / Capstone*  
- *Capstone Project 4*: Develop a complete design for an “Online Course Registration System” (use‑case, class, sequence, activity, deployment diagrams; ERD; database schema; test plan).  
- Mock exam: 2 hours, covering all UML diagrams, SDLC models, testing, and SQL.  

*Free Resources*  
- MIT OCW 6.031 (Software Construction) – [link](https://ocw.mit.edu/courses/6-031-software-construction-spring-2021/)  
- YouTube: “UML 2.0 Tutorial” by Derek Banas; “Database Normalisation” by Studytonight.

---

*2. COS 311 – Switching Algebra & Discrete Structures*
*Learning Objectives*
- Simplify Boolean expressions using postulates, laws, and De Morgan’s theorems.  
- Design logic circuits using basic gates (AND, OR, NOT, XOR, NAND, NOR).  
- Solve graph problems: adjacency matrix, Dijkstra’s algorithm, MST (Prim’s).  
- Construct truth tables and prove logical equivalence.  

*Assignments*
- Weekly problem sets (provided in your past questions).  
- Build a truth‑table generator in Python (optional).  

*Final Exam*  
- 2‑hour exam with Boolean simplification, circuit design, graph algorithm tracing.  

*Free Resources* 
- MIT OCW 6.042J (Mathematics for Computer Science) – [link](https://ocw.mit.edu/courses/6-042j-mathematics-for-computer-science-fall-2010/)  
- YouTube: “Neso Academy – Digital Electronics” playlist.

---

*3. COS 331 – Operating Systems II*
*Learning Objectives*  
- Explain process states, PCB, context switching, and CPU scheduling algorithms.  
- Implement memory management techniques: paging, segmentation, virtual memory, page replacement.  
- Analyse deadlock conditions and apply prevention/avoidance strategies.  
- Describe file system implementation and I/O management.  

*Assignments*  
- Simulate scheduling algorithms (FCFS, SJF, RR) in Java/Python.  
- Solve page replacement problems (FIFO, LRU, Optimal).  

*Final Exam*  
- 2‑hour exam with scheduling calculations, page‑fault analysis, deadlock detection.  
*Free Resources* 
- MIT OCW 6.828 (Operating Systems) – [link](https://ocw.mit.edu/courses/6-828-operating-system-engineering-fall-2012/)  
- YouTube: “Operating Systems” by Neso Academy.

---

*4. COS 341 – Computer Architecture & Organization II*
*Learning Objectives*  
- Distinguish Flynn’s classifications (SISD, SIMD, MISD, MIMD).  
- Analyse memory hierarchy (cache, main, virtual) and calculate hit/miss rates.  
- Explain pipelining, hazards, and superscalar architectures.  
- Compare hardwired vs. microprogrammed control units.  
- Describe DMA, interrupts, and I/O modes.  

*Assignments*  
- Calculate cache performance (average access time, hit ratio).  
- Draw pipeline diagrams and identify hazards.  

*Final Exam*  
- 2‑hour exam with memory hierarchy calculations, pipeline diagrams, architecture classification.  

*Free Resources*  
- MIT OCW 6.004 (Computation Structures) – [link](https://ocw.mit.edu/courses/6-004-computation-structures-spring-2017/)  
- YouTube: “Computer Architecture” by Onur Mutlu (lectures).

---

*5. COS 337 – System Analysis & Design*
*Learning Objectives*  
- Apply structured analysis tools: DFD, data dictionary, decision trees/tables.  
- Select appropriate SDLC model for a given scenario.  
- Perform feasibility analysis and requirements gathering.  
- Create UML diagrams for system design.  

*Assignments*  
- Draw a level‑0 DFD and a decision table for a “Book Borrowing System”.  
- Write a mini‑report on the choice of SDLC model for a mobile app.  

*Final Exam / Capstone*  
- Part of Capstone Project 4 (integrated with SE).  

*Free Resources*  
- Open Yale: “Software Engineering” (CS 105) – not directly, but MIT 6.031 works.  
- YouTube: “System Analysis and Design” by Dr. Gaurav Garg.

---

*6. COS 361 – Object-Oriented Programming*
*Learning Objectives*  
- Write Java classes with constructors, methods, and encapsulation.  
- Implement inheritance and polymorphism.  
- Overload and override methods correctly.  
- Use arrays and basic collections.  

*Assignments*  
- Weekly coding exercises (see your COS 361 notes).  
- Capstone integration: implement a simple console‑based registration system.  

*Final Exam*  
- 2‑hour coding exam (write classes, inheritance, polymorphism).  

*Free Resources*  
- MIT OCW 6.092 (Introduction to Programming in Java) – [link](https://ocw.mit.edu/courses/6-092-introduction-to-programming-in-java-january-iap-2010/)  
- YouTube: “Java Tutorial for Beginners” by Programming with Mosh.

---

*7. COS 335 – Artificial Intelligence I*
*Learning Objectives*  
- Define AI agents and their PEAS description.  
- Implement uninformed and informed search algorithms (BFS, DFS, A*).  
- Represent knowledge using propositional and first‑order logic.  
- Explain fuzzy logic and basic neural networks.  

*Assignments*  
- Code BFS and A* for a grid world.  
- Convert natural language statements into first‑order logic.  

*Final Exam / Capstone*  
- *Project 3* (A* for 8‑puzzle).  
- 2‑hour exam with search traces, logic translations, and neural network calculations.  

*Free Resources*  
- MIT OCW 6.034 (Artificial Intelligence) – [link](https://ocw.mit.edu/courses/6-034-artificial-intelligence-fall-2010/)  
- YouTube: “CS188 UC Berkeley AI” (full course).

---

*8. CED 341 – Introduction to Entrepreneurship*
*Learning Objectives*  
- Identify characteristics of women and youth entrepreneurship.  
- Evaluate business opportunities using RAMP model.  
- Explain intrapreneurship and social entrepreneurship.  
- Describe intellectual property rights (patents, trademarks, copyright).  

*Assignments*  
- Write a one‑page business opportunity evaluation (RAMP).  
- Case study: analyse a social entrepreneur (e.g., Muhammad Yunus).  

*Final Exam*  
- 1‑hour short‑answer exam (from your past questions).  

*Free Resources*  
- MIT OCW 15.390 (Entrepreneurship) – [link](https://ocw.mit.edu/courses/15-390-new-enterprises-spring-2013/)  
- YouTube: “How to Start a Startup” (CS183F) by Stanford.

---

*🎓 Portfolio Projects (Proof of Competency)*

Complete at least *3 of these 5* (you will already do #1, #2, #3 during the weeks).

1. *Project 1 – 4‑bit ALU in Logisim*  
   - Draw logic diagram or simulate in Logisim.  
   - Show addition, subtraction, AND, OR.  
   - Write a short report explaining the circuit.

2. *Project 2 – OS Process Scheduler Simulation*  
   - Write a Java/Python program that simulates FCFS, SJF, and Round‑Robin scheduling.  
   - Compute average waiting time and turnaround time.  
   - GitHub repo with README.

3. *Project 3 – A* Search for 8‑puzzle*  
   - Implement A* with Manhattan distance heuristic.  
   - Output the sequence of moves and number of expanded nodes.  
   - Compare with BFS (performance analysis).

4. *Project 4 – Complete Software Design Document* (Capstone)  
   - “Online Course Registration System” – includes all UML diagrams, ERD, database schema, test plan, and a small working Java console prototype (optional).  
   - This is your main portfolio piece.

5. *Project 5 – Research Paper*  
   - Choose a topic: e.g., “Comparison of Page Replacement Algorithms in Virtual Memory” or “Fuzzy Logic vs. Probability in Medical Diagnosis”.  
   - 4–6 pages, with citations (use Google Scholar).

---

*🤖 How to Use an LLM (Me) for Socratic Learning*

| Activity | How to prompt me |
|----------|------------------|
| *Quiz after reading* | *“Ask me 5 short‑answer questions about OS paging.”* |
| *Explain a gap* | *“I don’t understand how TLB works. Explain it like I’m 15, then give an example.”* |
| *Debug code* | *“Here is my Java code for inheritance. Why does it print the wrong value?”* (paste code) |
| *Simulate an oral exam* | *“Act as a professor. Ask me 3 questions about Dijkstra’s algorithm, one at a time. Wait for my answer before revealing the correct one.”* |
| *Generate flashcards* | *“Create 10 Anki‑style flashcards for deadlock conditions.”* |
| *Compare two concepts* | *“Compare and contrast paging and segmentation. Use a table.”* |
| *Trace an algorithm* | *“Walk me through the A* algorithm on this graph: …”* |
| *Review your solution* | *“Here is my solution to the page replacement problem. Point out any mistakes.”* |

> *Important*: Do not just ask for answers. First attempt problems yourself, then use me to verify and deepen understanding.

---

*📌 Final Advice*

- *Print or download* all your provided notes. Highlight key definitions and diagrams.  
- *Use Anki* for spaced repetition of definitions (Boolean laws, scheduling algorithms, UML symbols).  
- *Form a virtual study group* (Discord, WhatsApp) – explain concepts to others.  
- *Sleep 7–8 hours* – memory consolidation is critical.  
- *Take the mock exams seriously* – time yourself, no notes.  

You have everything you need. Now execute. Good luck.