# AI-Interview-Preparation-Assistant
AI Interviewer will conduct the interview based on the real interview questions asked in the interview. It will help with weak topics and keep track of your performance with every interview and customizes interview for you.


Here’s a structured documentation-style explanation of the **four tables** in your *AI Interviewer* solution, including their **custom columns**:

---

## 📑 Tables Overview


### 1. **Student Table**
- **Purpose**: Maintains candidate/student profiles for interviews.
- **Primary Column**: *Student Name*.
- **Custom Columns**:
  - **Email Address** – Contact details for communication.  
  - **Phone Number** – Candidate’s mobile number.  
  - **Skills Tag** –Skills Tag multiple choice column (e.g. power automate, dataverse, AI Builder etc)  
  - **Target Role** – RRole Target to identified questions  (e.g., Power Platform Developer, Salesforce Developer etc).
  - **Weak Topics** – Students Weak topics from skills tag in text filed. 

### 2. **Questions Table**
- **Purpose**: Stores interview questions along with metadata such as difficulty and categorization.
- **Primary Column**: *Question Number* (human-readable identifier).
- **Custom Columns**:
  - **Answer** – Stores the detailed answer or explanation for the question.  
  - **Cross Question** – Links related or follow-up questions for contextual flow.  
  - **Difficulty** – Categorizes questions as *Easy*, *Medium*, or *Hard*.  
  - **Question Number** – Unique identifier for each question (e.g., QN-1007).
  - **Skills Tag** –Skills Tag multiple choice column (e.g. power automate, dataverse, AI Builder etc).
  - **Target Role** – RRole Target to identified questions  (e.g., Power Platform Developer, Salesforce Developer etc).

---
### 3. **Interview Sessions Table**
- **Purpose**: Represents an interview event/session, grouping together candidate responses.
- **Primary Column**: *Session ID* or *Session Name*.
- **Custom Columns**:
  - **Student Name** – Lookup to *Student* table.  
  - **Start Date/Time** – DateTime field marking when the interview started.  
  - **End Date/Time** – DateTime field marking when the interview ended.  
  - **Feedback** –Interview feedback remarks .  
  - **Total Score** – Total score out of 10 (Summarize by whole interview).
  - 

--- 
### 4. **Interview Response Table**
- **Purpose**: Captures candidate responses to specific questions during an interview session.
- **Custom Columns** (based on typical design for interview solutions):
  - **Candidate Response** – Text field storing the actual answer given by the candidate.  
  - **Question ID** – Lookup to the *Questions* table, ensuring responses are tied to specific questions.
  - **Interview Session ID** - Lookup to Interview Sesson Table 
  - **Score/Rating** – Numeric or choice field for evaluator feedback.  
  

---

---

## 🔗 Relationships
- **Questions ↔ Interview Response**: Each response is tied to a specific question.  
- **Interview Response ↔ Interview Sessions**: Responses are grouped under sessions.  
- **Interview Sessions ↔ Student**: Each session belongs to a candidate.  

