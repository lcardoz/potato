![Gig Prints Logo](./client/src/readme-logo.png)

# GIG PRINTS

Welcome to Gig Prints- a single-page web application where touring bands and poster designers are two different types of users that can both discover and connect with each other to create unique concert posters for a band's upcoming tour dates as well as manage the tasks related to seeing a poster idea to completion.

> Please note all artwork, poster artist information, and band information are property of their rightful respective owner. Usage of band, poster artist, and poster images are for educational, non-commercial purposes only.

## Table of Contents
1. [Motivation](#Motivation)
2. [Demo](#Demo)
3. [Features](#Features)
4. [How To Use](#How-To-Use)
5. [Tech Stack & Requirements](#Tech-Stack-&-Requirements)
6. [Getting Started](#Getting-Started)

## Motivation
I am an avid concert-goer and poster collector, and prior to becoming a software engineer, I spent my entire working career in different facets of the live music industry. As soon as I arrive at a concert, the first thing I do is visit the merch stand, hoping there is a cool limited edition poster for sale. Most concerts I attend do not have a poster for sale, which is a huge missed opportunity for everyone involved: the independent poster designer, who would have a chance to share their artistic vision with a whole new audience, the band, who would add a new revenue stream, and the fans, who would be able to own a unique, tangible piece of that special concert experience forever.

I decided to build a real-world web application to help bands discover the best poster designers from all over the world, to facilitate poster designers in showcasing their work and easily connecting with bands on tour, and to simplify and centralize the process of creating concert posters so that more poster designers are booked for poster projects and more bands recognize the supply of talent that's available and feel compelled to respond to the demand by adding concert posters to their merch offerings.

## Demo
[Watch me demo the entire app here!](https://vimeo.com/798881890)

**Landing Page**

![Landing Page Slideshow Gif](https://videoapi-muybridge.vimeocdn.com/animated-thumbnails/image/c8bad448-cfb4-42aa-b151-251cf68681f6.gif?ClientID=vimeo-core-prod&Date=1685051585&Signature=7d7aabff2ca657bdca3d76431a6254dd56637fb3)

**Band Login / Band Home Page**

![Band Login Gif](https://videoapi-muybridge.vimeocdn.com/animated-thumbnails/image/6a343da5-3c58-4cad-933a-77ab2eac1d66.gif?ClientID=vimeo-core-prod&Date=1685051980&Signature=91f8bff58f14f147be0dfb9b4e7be58ae2f05fa6)

**Band Profile**

![Band Profile Gif](https://videoapi-muybridge.vimeocdn.com/animated-thumbnails/image/375de5fa-3277-4495-b2e6-5d37ca71bd9a.gif?ClientID=vimeo-core-prod&Date=1685052398&Signature=503d11bb4783f818736e8b582c3682af903b49f7)

**My Projects**

![My Projects Gif](https://videoapi-muybridge.vimeocdn.com/animated-thumbnails/image/aee928fa-d0b4-44ef-addf-c160e9aa56da.gif?ClientID=vimeo-core-prod&Date=1685054065&Signature=17f0b3eebbb8251975fa80965c23d7829264e902)

**Designer Login / Designer Home Page**

![Designer Login Gif](https://videoapi-muybridge.vimeocdn.com/animated-thumbnails/image/e67b28ea-fa9c-4885-965c-b0ea8bd2fca0.gif?ClientID=vimeo-core-prod&Date=1685054709&Signature=5e2d6f7612ca41f4546dac888f0fb4e6b6c857af)

**Designer Profile**

![Designer Profile Gif](https://videoapi-muybridge.vimeocdn.com/animated-thumbnails/image/e03a58e5-7d20-4ec3-ae26-50aa8bcb0281.gif?ClientID=vimeo-core-prod&Date=1685054930&Signature=2119947a3e4da81f94e2ac1c9f495042299400a8)

**Edit Profile**

![Edit Profile Gif](https://videoapi-muybridge.vimeocdn.com/animated-thumbnails/image/0560bab7-fab4-4c81-bfd1-fe329b6a4621.gif?ClientID=vimeo-core-prod&Date=1685055288&Signature=0c3814e6bd559091b4f53c18b5e99988348f5d43)


## Features

* Secure authenticated & authorized signup/login/logout functionality for band and designer models using Rails bcrypt gem and sessions.
* Semantic UI React components for user profile pages, band and designer homepages which include browsing, filtering and search features, and an editable table for project and task management.
* CRUD actions for three models including a joiner, facilitated on the frontend and harnessed on the backend.
* Live search queries the database, which is developed from scratch for band and poster designer data.
* Carousel slideshow on Homepage showcasing site's main features.
* Custom backend routes and react-router client-side routes.

## How To Use

* Bands can update whether they are on tour or not, and poster designers can update whether they are open to work or not.
* Bands can filter out designers not open to work and designers can filter out bands who aren't touring.
* To post any upcoming tour dates with open poster commissions to their profiles, Bands can create a new poster project on the "My Projects" page, add the relevant details such as concert date, location, and deadline, and mark the project as "unassigned" (only poster projects marked as "unassigned" will POST to the "Open Poster Commissions" section of the band's profile).
* After a band and poster designer get in touch via email and mutually-agree to a poster project, the band can update the "unassigned" poster project to "in progress" on the "My Projects" page, set the agreed-upon poster designer from a dropdown menu of all poster designers using the app, and add any other details needed to create the poster (dimensions, edition, budget, etc). Once the status of a project is changed from "unassigned", it will be removed from the "Open Poster Commissions" section of the band's profile.
* After a band has assigned a poster designer to a poster project, the designer has the capability to upload image links as drafts until the band agrees to the final draft.
* After the band has agreed to the final image draft uploaded by the poster designer, they will mark the status of the project as "complete" and the completed poster will POST to both band and designer profiles under the "recent concert posters" section.
* Both Bands and Designers have the ability to edit their profiles and edit a poster project, but only bands can create a new project or delete a project.

## Tech Stack & Requirements

> **Languages:** JavaScript | Ruby | HTML5 | CSS

> **Frameworks:** React.js | Ruby on Rails

> **Libraries:** React Router | Semantic UI

- react 18.2.0
- react-router-dom 6.6.2
- semantic-ui-react 2.1.4
- ruby 2.7.4p191
- rails 7.0.4
- npm 8.19.2

## Getting Started

1. Install dependencies:
```sh
npm install
```

2. Start rails server: 
```sh
rails s
```

3. Start local react server: 
```sh
cd client
```
```sh
npm start
```