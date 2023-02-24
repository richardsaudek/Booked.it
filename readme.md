<p align="center">
  <img src="https://user-images.githubusercontent.com/123023398/221219765-2fb1ffcd-f91a-46c5-87e3-581fdf2eb0af.png?raw=true" alt="BookIt's custom image"/>
</p>

<strong>BOOK iT!</strong>
======

>An App for Professional Performing Artists Navigating the Busy Process of Auditioning 



### Table of Contents:
**[Descrition](#description)**<br>
**[API](#api)**<br>
**[MVP](#mvp)**<br>
**[Data Model](#data-model)**<br>
**[Notes and Miscellaneous](#notes-and-miscellaneous)**<br>
**[Building the Extension Bundles](#building-the-extension-bundles)**<br>
**[Next Steps, Credits, Feedback, License](#next-steps)**<br>

# Description

<strong>BookIt</strong> allows actors to create a detailed contact list of industry professionals who they've met and auditioned for. 
<strong>BookIt</strong> works as a rolodex of past and upcoming appointments, noting the date and location of the audition as well as who was in the room so that the artist can follow up with the right people and maintain relationships. 
<strong>BookIt</strong> also offers the artist to manage their preperation for the appointment as well a space to reflect on how it went.

# API: 
I'm making my own! In the final product, the user will generate the API for themselves.

- **_API Snippet:_** N/A

# MVP:
To be able to create, view and edit audition appointment listings.

# Post MVP:
Design and implement a front end! Add user authentication and the ability to upload photos.

# Goals:

- [x] Create one model named 'Audtions'
- [x] Complete CRUD funtionality with RESTful routes
  
<br>

# Data Model:

<img src="https://github.com/richardsaudek/Booked.it1/blob/046c00cc8e7a508a5b381a0f9c8a87718730de91/project2%20wire.png?raw=true" alt="BookIt's data model"/>
</p>


| Route                         | HTTP Method | DB Action | Description                 |
| ----------------------------- | ----------- | --------- | --------------------------- |
| /api/models/Audition_Info/:id | GET         | INDEX     | Indexes all the submissions |
| /api/models/Audition_Info/:id | POST        | CREATE    | Create a submission         |
| /api/models/Audition_Info/:id | GET         | SHOW      | Show a single submission    |
| /api/models/Audition_Info/:id | PATCH       | UPDATE    | Update a submission         |
| /api/models/Audition_Info/:id | DELETE      | DELETE    | Delete a submission         |


```var s = "JavaScript syntax highlighting";
const auditionSchema = new mongoose.Schema(
  {
    name_of_project: {
      type: String, default: 'Project'
    },
    type_of_project: {
      type: String, default: 'Type of Project'
    },
    date: {
      type: String, default: 'Date'
    },
    location: {
      type: String, default: 'Address'
    },
    union_status: {
      type: Boolean, default: null
    },
    casting_office: {
      type: String, default: 'Enter the Casting Office'
    },
    casting_dir: {
      type: String, default: 'Who is the CD?'
    },
    casting_associate: {
      type: String, default: 'Who is the Casting Associate?'
    },
    prep: {
      type: String, default: 'What do you need to prepare?'
    },
    post_aud_notes: {
      type: String, default: 'How did it go?'
    }
  }
)

// const Audition = mongoose.model('Audition', auditionSchema)
export default mongoose.model('Audition', auditionSchema)```


