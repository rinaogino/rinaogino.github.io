---
layout: essay
type: essay
title: "AI and I"
# All dates must be YYYY-MM-DD format!
date: 2024-05-06
published: true
labels:
  - Artificial Intelligence
  - Software Engineering
  - Education
---

<div style="text-align: center;">
    <img src="../img/ai/ai-hands.jpeg" width="500px">
</div>

### I. Introduction

By now, there are approximately 180.5 million users of ChatGPT, which certainly proves the enormous influence of artificial intelligence (AI) in this world. Ever since I was introduced to AI last year, I have somehow implemented this tool into my courses of study, particularly in ICS 314: Software Engineering. From simple syntax or spelling corrections, AI has the ability to assist in writing code, whilst providing efficient and secure solutions. As AI has become a part of modern education, I am starting to see many of professors allow the use of it as an expansion of resources.

In software engineering, I have utilized ChatGPT to fix bugs, choosing which function/class to use, and overall to understand code. I have also used ChatGPT generally in every day tasks such as finding a dinner recipe, or finding an outfit to wear. AI has definitely revolutionized the way students learn, how schools or teachers facilitate, and or completing life tasks where people are starting to depend on it.

However, can AI really give us all the answers? No, not necessarily. AI may be useful in many perspectives, as I access it almost every other day, yet it cannot be fully depended on. As useful as it is, AI is still a tool and lacks several aspects. Nonetheless, here are some of the experiences I have had with AI below.

### II. Personal Experience with AI:
I have used AI in class this semester in the following areas:

1. Experience WODs e.g. E18  
   In the past 63 experience WODs, I did not utilize AI. Most of the experiences included screencasts of step-by-step instructions on completing the assignments provided by the instructors, and I felt that it was better to follow these given resources instead of depending on AI to understand the material. As a visual learner, it was helpful to watch the Professors' solve the similar prompt in their perspective, which allowed me to follow along and detect any mistakes that I may have made. In [E18](https://courses.ics.hawaii.edu/ics314s24/morea/javascript-3/experience-underscore.html), I took my first look into functional programming utilizing Underscore.JS. I had no idea what Underscore.JS really was, but given the resources, I felt that I was able to pick this up quickly.

2. In-class Practice WODs  
   In-class practice WODs were completed in groups of randomly chosen classmates, so it was interesting to see others' different approaches toward solving coding problems. In this case, I used ChatGPT when I was not able to my classmates' approaches or the prompt itself. I would ask, for example, "How can I approach the following issue using Underscore.JS: <insert prompt>" and ChatGPT would list out what I must do along with an example snippet code. I then would compare what ChatGPT gave me with what my group came up with, and find a overall solution.

3. In-class WODs  
   With the pressure of having to clear each WOD and receive a 100% score (WODs were based on 'all or nothing' scoring system), I used AI for majority of the in-class WODs. If I were stuck on a specific step during the WOD, I knew that I did not have enough time to look it up, so I would ask ChatGPT to summarize what I needed to do in order to successfully complete the WOD (I would use a similar question as the in-class practice WODs mentioned above). Additionally, at the very end of each WOD, to ensure that my code would run without any errors, I would input my entire code to ChatGPT and confirm before stressing myself out by seeing warnings in the output console.

4. Essays  
   I am not much of a creative writer nor have perfect grammar, so I utilized AI in many of my essays. I used ChatGPT to ask for a template of what I can write, and in which order for the essay to sound as engaging as possible. I would write out the essay myself then input it into ChatGPT, to make sure that it somehow followed the template while checking if it looked and sounded professional. I understand that essays are more-so creative writing in our own words, and AI may take away that by re-stating the essay itself in not so human-like words, but I liked the immediate feedback--that I believe helped me greatly in making my essays sound more engaging.

5. Final project  
   For my final project, I wanted to try and apply my knowledge and skills developed from ICS 314, so I tried to minimize the use of AI. However, I did end up utilizing AI for functionality that we had never learnt in class such as the image upload. Hence, I would ask, "I want to implement a button and functions to upload images. Here is what I have for now: <insert code>" Then, ChatGPT provided me with the following code:

  ```javascript
   const AddStudent = () => {
  const [selectedImage, setSelectedImage] = useState(null);

  const handleFileUpload = (e) => {
    const file = e.target.files[0];

    if (file) {
      // Use FileReader to read the selected image as a data URL
      const reader = new FileReader();

      reader.onload = (readerEvent) => {
        setSelectedImage(readerEvent.target.result);
      };

      reader.readAsDataURL(file);
    }
  };

  const uploadImage = () => {
    // Simulate uploading the image (you can implement the actual upload logic here)
    alert('Image uploaded successfully');
  };

  return (
    <Container className="py-3">
      <Row className="justify-content-center">
        <Col xs={8}>
          <Col className="text-center"><h2>Add Student Profile</h2></Col>
          <Card>
            <Card.Body>
              <Row>
                <Col>
                  <label>Full Name:</label>
                  <TextField name="fullName" placeholder="Full Name (e.g. John Appleseed)" />
                </Col>
              </Row>
              <Row>
                <Col>
                  <label>Image:</label>
                  <input type="file" onChange={handleFileUpload} accept="image/*" />
                  {selectedImage && <img src={selectedImage} alt="Selected" style={{ maxWidth: '100%', maxHeight: '200px' }} />}
                  <button onClick={uploadImage}>Upload Image</button>
                </Col>
              </Row>
              <Row>
                <Col>
                  <label>Email:</label>
                  <TextField name="email" />
                </Col>
                <Col>
                  <label>Phone Number:</label>
                  <TextField name="phoneNumber" />
                </Col>
              </Row>
              <Row>
                <Col>
                  <label>Major:</label>
                  <TextField name="major" />
                </Col>
                <Col>
                  <label>Graduation Date:</label>
                  <TextField name="graduationDate" />
                </Col>
              </Row>
              <TextField name="skills" label="Skills" />
              <TextField name="awards" label="Awards" />
              <LongTextField name="description" label="Description" />
              <Row>
                <Col>
                  <label>LinkedIn:</label>
                  <TextField name="linkedIn" />
                </Col>
                <Col>
                  <label>GitHub:</label>
                  <TextField name="gitHub" />
                </Col>
              </Row>
              <SubmitField value="Submit" />
              <ErrorsField />
            </Card.Body>
          </Card>
        </Col>
      </Row>
    </Container>
  );
};

export default AddStudent;
   ```
   With having no knowledge on the functionality of image uploads, this quickly generated code that ChatGPT wrote out to me turned out to run successfully.
  
6. Learning a concept / tutorial  
   Like the example I provided above in learning a new functionality, I used ChatGPT to learn a concept / tutorial. ChatGPT was able to provide me with instructions on how a task could be could be done, and I liked that it always provided me with examples that I could follow.
  
7. Answering a question in class or in Discord  
   Without the use of AI, I used my own knowledge to answer a question in class or in Discord. If I was unable to explain a prompt myself, I would not answer a question in the first place because I do not want to risk giving anyone mistaken information, which may lead another into extra unnecessary errors.

8. Asking or answering a smart-question  
   Similar to answering a question in class or in Discord, I did not use AI to ask or answer a smart-question. If I were asking a smart-question, I would prefer to address the issue in my own words so that nothing is fabricated, and that I am able to show my understanding to a certain extent so that another could help me figure out what is beyond that. Also, if I don't understand my own issue, then there is a possibility that I wouldn't understand the answer to it. Likewise, if I were looking for an answer for a smart-question, I would prefer for the answer to be described in human-like, easy terms so I did not use AI to answer any questions. Throughout this course, I have probably answered one or two smart-questions, and they were mainly about errors. Hence, I liked to include my own experiences of walking through the task, and I felt that describing my classmates' error in my own words helped me achieve finding their solutions best.

9. Coding example e.g. “give an example of using Underscore .pluck”  
   I have definitely used AI to generate a coding example. The given example was something similar to what I asked AI, as I struggled with picking the right library to use throughout Underscore. Also, instead of asking for an example, I would also use ChatGPT to generate which Underscore libraries I should use toward specific prompts.

10. Explaining code  
    As I mentioned for the in-class practice WODs, I have used AI when I did not understand others' approaches toward a certain prompt. Although my group mates were typically nice and attempted to explain their different approaches to me, I made sure that I comprehended what was going on by utilizing ChatGPT.

11. Writing code  
    Although I have always tried to write code from scratch using my own knowledge and given resources, there were many times where I turned to ChatGPT to write out my code. Especially in the timed WODs where I felt stressed out and my mind went blank at times, I had AI to assist me with what I should write in order to get a successful output.

12. Writing code  
    I do not recall using AI to document code. I believe ICS 314 provided students with enough resources to learn how to document code. Otherwise, I would prefer to document code in my own words so that I understand what is happening when I go back to the code. For instance, when we look at the following code.

  ```javascript
  function calculateRectangleArea(width, height) {
    return width * height;
  }

  const width = 5;
  const height = 10;
  const area = calculateRectangleArea(width, height);
  console.log(`The area of the rectangle is: ${area}`);
   ```
   ChatGPT provided me with the following documentation:
   ```javascript
   // Define a function to calculate the area of a rectangle
  function calculateRectangleArea(width, height) {
  // Multiply the width and height to get the area
    return width * height;
  }

  const width = 5; // Define the width of the rectangle
  const height = 10; // Define the height of the rectangle
  const area = calculateRectangleArea(width, height); // Calculate the area using the function
  console.log(`The area of the rectangle is: ${area}`); // Output the calculated area
   ```
  However, if I were writing out the documentation, it would look like this for my own understanding:
   ```javascript
   // Function to calculate area of rectangle.
  function calculateRectangleArea(width, height) {
    return width * height;
  }

  // Initialize variables.
  const width = 5;
  const height = 10;
  // Calculate area with width and height.
  const area = calculateRectangleArea(width, height);
  // Print output.
  console.log(`The area of the rectangle is: ${area}`);
   ```

13. Quality assurance  
    ChatGPT was helpful for quality assurance, especially for writing essays. It always assured me and gave me advice when my essay had the potential to improve. However, in a software engineering perspective, I mainly depended on ESLint, as it would point out any fixes needed to make my code run better or to overall become more organized.

14. Other uses in ICS 314 not listed above  
    Besides the experiences I have with AI in ICS 314 as listed above, I have only utilized ChatGPT to summarize readings. The instructors of ICS 314 would probably not want to hear this, but I have never been able to read an entire page or article without getting side tracked, as I would have to re-read from the top over and over. Therefore, I have always not read the given readings in full, but summarized them to a certain extent. Nevertheless, I would like to emphasize that I have learnt more than enough information in ICS 314!


### III. Impact on Learning and Understanding:

The incorporation of AI in my education has definitely changed my learning experiences. As ChatGPT was released around the end of 2022, I had started to learn and utilize it towards the end of last year (2023). I haven't quite experiences other AI tools, but ChatGPT has definitely been a big part of my education as I started to rely on it a lot, to the point where I wondered how I ever wrote essays in high school using my own brain. AI has the ability to explain toward one's comprehension, but because it gives us solutions right away, I believe it has lowered my comprehension as well as my problem solving abilities. Whenever, I can't figure out something, I would open ChatGPT right away and trust that the tool is correct instead of simply looking it up on the great internet.

As a student studying software engineering, I should definitely not be relying on AI and only using it as a resource. Hence, AI technologies have enhanced my understanding of software engineering concepts, but also challenged me to problem solve these concepts at the same time.

### IV. Practical Applications:

Outside of ICS 314, one project I have been working on is an alumni data analysis. For this, I have not utilized AI since I never happened to encounter any issues as I have been using my own skillsets to analyze the data. Also, I have been heavily relying on other resources such as my peers if I needed any assistance.

Besides the project, I have not been a part of real-world software engineering challenges so I have not used AI. Yet, I have used AI in daily life tasks such as finding the ingredients to make a perfect matcha latte. To add on, one interesting thing that I have asked ChatGPT is my seasonal color analysis, where I found out that my skin tone matches Autumn color clothing best!

### V. Challenges and Opportunities:

There are no perfect humans nor perfect tools in this world. Hence, there will always be limitations paricularly in AI. As useful as it is, it is still developed by human and may have outdated data pulled off of the cyberspace. AI will not always be correct and may not even be able to assist with certain questions. Also, AI may include biased answers and will never be creative because it has never had real experiences as a human. 

One particular limitation that AI, or ChatGPT in my learning has had is with UI designs. As I mainly dependent on ChatGPT for WODs and such in ICS 314, there was a point where I could no longer utilize ChatGPT to figure out if I was right or wrong. This frustrated me, but also helped me realize that I needed to do some things on my own and helped me learn better.

### VI. Comparative Analysis:

Learning methods have changed overtime with the release of AI, such as ChatGPT that I often use. From traditional teaching methods using textbooks and notebooks, students have transformed to use laptops and tablets with access to the internet with millions of resources that can be searched within seconds. With the infinite access and free use, AI has risen as well, with many incorporating it into their everyday lives. Now... is this really a healthy way of learning? 

Not sure. Personally, I believe that it is still early to determine whether AI is a positive or negative impact to learning and understanding. However, at times I get worried about completely comprehending subjects as I am becoming more and more dependent on it. AI generates an answer to almost anything in minutes, or even seconds, and this is not the best way to learn--students are not taking as much time to go out of their way to understand material. Additionally, AI takes away engagement and practical skill development in a sense.

AI will always be much more efficient than researching on paper, but again, it will never be accurate. But, once again looking at students' resources besides AI would only be traditional resources such as textbooks, teachers, and peers. So whenever there are quick questions that need to be asked, AI may be the way to go. There are many pros and cons on the impact of AI in learning, and I don't have the most confident feeling about it but am interested in seeing what more developments will occur next.

### VII. Future Considerations:

From now, I only believe that AI will keep developing and become more intertwined with software engineering education. I expect to see almost all student utilize AI as a part of their study, as majority of my classmates already do so now. Yet, with being more implemented into education, some things that should be considered for potential advancements are to clear up any false information and to add on more accurate information. As AI is created from numerous sources pulled together from the internet, there will always be inaccurate information, and being able to detect them will definitely increase in user usability as well as dependency.

### VIII. Conclusion:

Overall, I can say that AI and I are now friends as I gradually started to utilize it in many aspects, especially in my ICS 314 software engineering course. There were various times where I have used ChatGPT, as I have listed the experience above. AI was able to provide important information, helped me understand, and learn new concepts beyond traditional teaching methods. Thus, I am interested in seeing AI to be implemented more in software engineering education.
