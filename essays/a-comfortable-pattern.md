---
layout: essay
type: essay
title: "A Comfortable Pattern"
# All dates must be YYYY-MM-DD format!
date: 2024-04-25
published: true
labels:
  - Software Engineering
  - Software Design
  - Programming
---

<div style="text-align: center;">
    <img src="../img/ensuring-uniqueness/furniture.jpeg" style="width:50%; height:50%;">
</div>

## Moving In to a New Home

As a 20 year old college student, I have started to think about moving out of my family home. I attend college from where my family resides together, and the location is great and everything, except when my mother starts to nag at me and tells me to be indepdent for once. She says, "When I was your age, ... " I totally understand where she is coming from, but moving out scares me. It's not just about finding a new place to live; it's about having new responsibilities, creating a new comfortable home from scratch, complete with furniture and other details of life.

When faced with a task of purchasing and putting together furniture, I'm reminded of software engineering. Assembling a new piece of furniture involves having to unbox and follow instructions to bring various hardware together (remember, I am an aspiring software engineer, not a mechanical engineer). This process requires an attention to detail, and the right tools for use with different hardware.

Interestingly, the process of assembling furniture is similar to the principles of software design patterns. As each piece of hardware and tools must work together to develop something new and functional, it must be ensured that the final product is solid and aesthetically pleasing as well. Both engineering methods require careful planning, and a understanding of how individual elements contribute to the larger picture. 

<img width="250px" class="rounded float-start pe-4" src="../img/ensuring-uniqueness/blueprint.jpeg">

### The Blueprint

Design patterns in software engineering is highly similar to the assembly instructions for constructing furniture. They are predefined solutions to common problems encountered during the development of software systems. Just as furniture building manuals guide the process of putting together individual components to create one functional piece of furniture, design patterns provide programmers with a structured approach to organizing and composing software components to achieve desired functionality. Like following step-by-step instructions to assemble furniture, implementing design patterns involves deep understanding of the problem being juggled, selecting the appropriate pattern, and applying it to the software architecture to create a maintainable system. Also, similar to a well made piece of furniture, a software using design patterns is known for its reliable, and easy to maintain nature.

## Picking the Designs

Reflecting on my personal experiences whilst programming, I have realized many of uses of design patterns. One recently applied pattern would be the Presentational and Container Components pattern. As for a final project, my group and I have been working on a company connector application: [Kalo Stems](https://kalo-stems.github.io/). In this, I have taken on many of the roles in managing student data such as the functionality of listing out student profiles. 

In the following code, the `ListStudent` acts as a container component, as it connects to the Meteor data with `useTracker`, which pulls data from `Students` to get student data to be passed onto the presentational component, `StudentItem`.

```
const ListStudent = () => {
  const { ready, students } = useTracker(() => {
    const subscription = Meteor.subscribe(Students.userPublicationName);
    const rdy = subscription.ready();
    const studentItems = Students.collection.find({}).fetch();
    return {
      students: studentItems,
      ready: rdy,
    };
  }, []);
  return (ready ? ( ... )
};

export default ListStudents
```

Following the code above, below is the `StudentItem` where it receives the student data as it provides the UI components for each student profile into the table of data.  

```
const StudentItem = ({ student }) => (
  <tr>
    <td>{student.fullName}</td>
    <td>{student.image}</td>
    <td>{student.email}</td>
    <td>{student.phoneNumber}</td>
    <td>{student.major}</td>
    <td>{student.graduationDate}</td>
    <td>{student.skills}</td>
    <td>{student.awards}</td>
    <td>{student.description}</td>
    <td>{student.linkedIn}</td>
    <td>{student.gitHub}</td>
  </tr>
);

StudentItem.propTypes = {
  student: PropTypes.shape({
    fullName: PropTypes.string,
    image: PropTypes.string,
    email: PropTypes.string,
    phoneNumber: PropTypes.string,
    major: PropTypes.string,
    graduationDate: PropTypes.string,
    skills: PropTypes.string,
    awards: PropTypes.string,
    description: PropTypes.string,
    linkedIn: PropTypes.string,
    gitHub: PropTypes.string,
    _id: PropTypes.string,
  }).isRequired,
};

export default StudentItem;
```

Through this collaboration of container and presentational components, the application achieves a successful application, just as if I just build my first functional furniture. In contemplating the idea of moving out, I was struck by the parallel of assembling furniture and software engineering. Both the process of putting together physical furniture pieces and putting together code require a lot of planning, and responsibilities! With this, I hope to feel more confident in my ability to navigate adulthood and creating a space that reflects my independence.

*ChatGPT was used to correct some grammar and spelling mistakes.*
