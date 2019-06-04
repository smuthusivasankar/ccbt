# CCBT - Computerised Congitive Based Therapy

It is an online CMS based web solution for medical practitioners to create [Cognitive Based Therapy](https://en.wikipedia.org/wiki/Cognitive_behavioral_therapy). CCBT is more like Learning Management System where Cases are similar to course, Modules are similar to Lessons and Tasks are similar to topics. 


# Roles
- `Super Admin`: Crud for all the resources, analytics. 
- `Therapists`: Can create and monitor their patients, therapies. 
- `Authors`: Can create assigned therapies. 
- `Patients`: Can log in to their web portal and take CBT. 

# Domain Model
![CBT](https://user-images.githubusercontent.com/2022919/58890097-4505fb80-86ea-11e9-8b36-0ea6d2129081.png)


# Server
- `nodejs`
-  `mongoDB`
- `mongoose`
- `GraphQL`

# Frontend
- `React`
- `Redux`
- `Redux Saga`
- `GraphQL`
- `Immutable JS`
- `Redux Form`

# Database Schema

## Cases
- identifier (UUID)
- name (String, required)
- slug (String, createSlug(title))
- description(String)
- featuredImage (Blob)- 
- availableFrom(Date)
- availableTill(Date)
- createdAt(Date)
- updateAt(Date)

## Module
- identifier(UUID, PRIMARY KEY, REQUIRED)
- name (String, required)
- slug (String, createSlug(title))
- description(String)
- featuredImage (Blob)
- linkedCases(array, case IDs)
- availableFrom(Date)
- availableTill(Date)
- createdAt(Date)
- updateAt(Date)
- courseProgression(enum, [LINEAR, FREEFORM])
- modulePrerequisite(array, moduleIDs)

## Tasks
- identifier(UUID, PRIMARY KEY, REQUIRED)
- name (String, required)
- slug (String, createSlug(title))
- description(String)
- linkedModules(array, case IDs)
- tasksPrequisite(array, taskIDs)
- availableTill(Date)
- createdAt(Date)
- updateAt(Date)
