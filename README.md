# 332s-chatbot

## Section 1: Overview
This project aims to create a chatbot for answering questions related to CSE 332S: Object-oriented software development. This course is offered at WashU as part of the Computer Science and Engineering department and is a required course for all CS majors and minors. The goal of the project is to give students access to a resource for getting help quickly, even if that help may not be perfect. The chatbot will include:
1. a student facing user interface (likly a web based fron-end), allowing students to submit questions to the chatbot.
2. a large language model trained on course resources including past piazza posts, course lecture videos, and course recitation recordings. 
3. a RestAPI that connects the user to the chatbot, allowing user questions to be submitted and answers returned.

More details on will be provided regarding each of the above in section 3.

## Client 
This project is proposed by Prof. Shidal, Senior Lecturer at WashU and instructor of CSE 332S (shidalj@wustl.edu)

## Section 2: Project requirements
A minimal viable solution for this project includes a working chatbot, accessible via a RestAPI and a user interface allowing a user to ask questions to the chatbot and display the bots answers. 
### Minimum equirements for the user interface are:
1. accepts user input in the form of text
2. makes API calls to forward user input to the chatbot
3. displays the answer to the user, waits for additional user input

Additional features worth considering if time permits:
1. direct interface Piazza to automatically send questions asked via piazza to the chatbot and automatically post the response
2. ability for a user to rate the response reeceived as helpful/not helpful to assist with additional training/tuning of the bot
3. web interface to allow users to ask questions anywhere with a web connection

### Minimum requirements for the LLM bot
1. trained via archived class resources including text (piazza notes, questions, and answers) and video (lecture videos, recitation recordings)
2. given a question as input, respond with an answer to that question with reasonable accuracy (~75% helpful/accurate)

Additional features
1. continuos training, incrmenetal updates - take user input into account to update (helpful/not helpful), easy to update model given new resources (new recitation recording, new piazza posts)
2. Tuning to produce more accurate results

### Minimum requirements for RestAPI
1. endpoint for submitting a question, cleans the user input and invokes the bot to receive an answer and send back to the user interface

Additional features
1. endpoint for submitting new data to be used to train
2. endpoint for requesting question/answer history
3. ability to manually review history and mark as correct/incorrect to facilitate model tuning

## additional features beyond the three pieces above
1. user interface targeted towards insructors to monitor and review the bots performance. Displays saved questions/answers, allows feedback from the instructor on correctness, allows instructor to provide additional resources for training, etc.

## Technologies required/used for development
1. Version control - git and github.com will be used for manageing the codebase
2. Issue tracking - github issues will be used for planning and tracking rogress on project development
3. other technologies TBD based on further research

## Product testing
### User interface
A unit testing frameowrk will be used to ensure user interface is working correctly and correctly invoking API endpoints with appropriate data. **Framework TBD**.
### Chat bot performance
Manual grading will be used to verify the bots performance in certain areas. Some ideas for test questions:
1. questions directly from newer piazza posts not used in training
2. class discussion board questions
3. a representative set of questions created by instructor and TAs covering all course concepts
4. old exam questions
### API testing
A unit testing framework will be used to ensure API endpoints are correctly processing inputs and invoking the bot program - **Framework TBD**

## Estimated development timeline
An incremental building approach will be used to construct this software, building it piece by piece. 
1. simple user interface to grab a single question from the user and display a response from the API (weeks 1-2)
2. A simple RestAPI to receive requests and respond with a default message (weeks 1-2)
3. Create a simple program to take in a message as input and respond with a answer (generic answer). Modify the API endpoint to invoke this program to generate a response, sned the response back to the user interface to be displayed (weeks 3-4)
4. Select LLM model to use, collect inputs for model training. (weeks 3-4)
5. Clean data and preapre data for model training (video to text, etc.) (weeks 3-4)
6. Train LLM model given collected data (week 5-6)
7. Update API to invoke chat bot program rather than generic program to connect the user interface to the bot (week 7)
8. Test bot performanced based on testing criteria and document work (week 8)
9. Iterate and improve or implement additional features (weeks 9+)

## Transferring deliverables to the client
In my case, the client is me..I will make this repository accessible to myself. Throughout my work, I will document exactly what I have done via a note taking app like Google Docs. I will upload all notes to this repository for later review. I will create necessary guides and documentation to allow others to easily follow my work and reproduce it if desired (installation guide for necessary libraries, software. Installation and compilation guide for code I've written. Instructions for hosting any cloud services on AWS, etc.). I will also upload to this repositroy a copy of any slides used during presentations throughout the semester.

