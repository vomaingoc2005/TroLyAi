# Assignment #2 AI ASSISTANT

## 📦 How to Run the Program

### Step 1: Clone this repository
Open your terminal and run:
```
git clone https://github.com/your-username/AIAssistantCS4080.git

cd AIAssistantCS4080/source_code
```
Make sure Python is installed

### Step 2: Run the assistant
In the source_code folder, launch the assistant with:
```
python main.py
```
### Step 3: Interact with the assistant
The program will prompt you for your name, age, and whether you’re a premium user.<br/>
<br/>
Then you can type in requests like:<br/>
<br/>
	•	_"Play me something calm"_<br/>
	•	_"I want to build muscle"_<br/>
	•	_"Help me study for math"_<br/>
	•	_"Recommend a good fantasy book"_<br/>
	•	_"I'm feeling overwhelmed"_<br/>

**Free vs Premium Users**<br/>
	•	Free users can interact with assistants, but are limited to 3 high-level requests per session.<br/>
	•	Premium users have unlimited access.<br/>

## 🔍 Overview of the Assistant Functionality

This AI Assistant simulates a modular, multi-functional virtual assistant that can interact with users across various domains. Based on user input and preferences, it dynamically selects the appropriate assistant subclass to handle specific types of requests. Each assistant responds with customized messages and behaviors based on the context.<br/>

### Supported Functionalities:
🎵 **Music Assistant (MUSIC)** <br/>
Recommends music playlists based on the user’s current mood, favorite artists, or activities. Offers a wide variety of emotional tones and genres to suit personal preferences.<br/>
<br/>
💪 **Fitness Assistant (FITNESS)** <br/>
Suggests fitness plans, workout schedules, and exercises tailored to the user’s body goals and available time. Differentiates plans based on intensity and user fitness level. <br/>
<br/>
📚 **Study Assistant (STUDY)** <br/>
Helps users study smarter by offering personalized study tips, topic explanations, and the ability to schedule sessions based on areas of difficulty. <br/>
<br/>
🧠 **Psychology Assistant (PSYCHOLOGY)** <br/>
Acts as a conversational AI psychologist. Listens to the user’s thoughts, offers helpful coping strategies for stress, burnout, or mild depression, and provides insights into psychological phenomena when users are curious. <br/>
<br/>
📖 **Book Assistant (BOOK)** <br/>
Recommends books using keywords in user descriptions and genre preferences. Also provides online links to read or purchase recommended books. <br/>
<br/>
💬 **General Assistant (GENERAL)**
Handles general, undefined inputs in a friendly, helpful way when no specific category is matched. Ensures the conversation continues smoothly even with vague or ambiguous requests.

## Concepts Implemented <br/>
**Custom Data Types** <br/>
Defined UserProfile, Request, and Response in models.py using @dataclass. <br/>
<br/>
**Validation / Type-Safety:** <br/>
Validation logic is in the __post_init__ methods of the data classes to ensure correct data types and constraints. <br/>
<br/>
**Enumeration:** <br/>
CommandType enum in models.py defines valid request types (e.g., MUSIC, STUDY). <br/>
<br/>
**Inheritance & Polymorphism:** <br/>
AIAssistant is the base class in base_assistant.py. <br/>
MusicAssistant, FitnessAssistant, StudyAssistant, PsychologyAssistant, BookAssistant, and others override handleRequest() and greetUser() for customized responses. <br/>
<br/>
**Dynamic Behavior & Object Simulation:** <br/>
In main.py, multiple user profiles are created and handled dynamically using their command types to choose the appropriate assistant. <br/>
<br/>
**Command Parsing (Bonus):** <br/>
classify_command() in main.py uses string matching to simulate intent recognition. <br/>
