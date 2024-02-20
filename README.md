# Rick & Morty Application

Welcome to the Rick & Morty Application! This application allows users to explore the Rick & Morty universe by viewing locations, characters, and episodes.

## Technology Stack

This project is built using the following technologies:

1. **Frontend:**
   - Next.js
   - Tailwind CSS

2. **Component Library:**
   - DaisyUI

## Requirements

Ensure the following are installed on your machine:

1. Git
2. Node.js (>=v18)
3. Yarn

## Project Structure

The project structure is organized as follows:

```bash
rick-and-morty-app/
|-- components/
|-- pages/
|-- styles/
|-- public/
|-- ...
|-- README.md
|-- initial wireframe.png
```

- **components:** Contains React components for various UI elements.
- **pages:** Next.js pages for different sections of the application.
- **styles:** Tailwind CSS styles for styling the components.
- **public:** Public assets, including images.

## Architectural Decisions

### 1. Next.js as the Full Stack Framework

- **Pros:**
  - Well-documented and widely used in the industry.
  - Single server for client-side and server-side rendering.
  
- **Cons:**
  - New app router might not fulfill all requirements.

- **Other Notes:**
  - The developer chose to test the new app router functionality.

### 2. DaisyUI Component Library

- **Pros:**
  - Reduces development time for common components.
  - Lightweight abstraction coexisting with Tailwind.

- **Cons:**
  - May need to eject if a design system is introduced.

### 3. Server Rendering Majority of Components

- **Pros:**
  - Offloads data fetching to the server for better performance.
  
- **Cons:**
  - Care needed to identify user hotpaths affected by server rendering.

### 4. Rick and Morty JavaScript Client

- **Pros:**
  - Fully typed client for easy prototyping.
  - Leverages fetch library in Next.js.

### 5. Saving Notes in LocalStorage

- **Pros:**
  - Fast prototyping for saving functionality.

- **Cons:**
  - Not suitable for persistent data across sessions.

### 6. Lack of User Authentication/Persistent Sessions

- **Pros:**
  - Speedy prototyping without the need for a database.

- **Cons:**
  - Cannot work for storing persistent data.

### 7. Coupling Application State with URL State

- **Pros:**
  - Easier verification of UI state across browsers.

### Initial Wireframes

![Wireframe](initial%20wireframe.png)

## REST vs GraphQL

The choice was REST due to:

1. Displaying lists with information already received from REST responses.
2. Ease of implementing paginated responses for lists.
3. Leveraging server-side components to reduce client processing time.

GraphQL might be beneficial for entity pages (e.g., character details) due to reduced query complexity.

## Deployment

The project is deployed on Vercel and can be accessed [here](https://rick-and-morty-agency.vercel.app/).

## Running the Application

To run the application locally:

1. Clone the repository.
2. Run `yarn` to install dependencies.
3. Run `yarn dev` to start the application.

## Checklist

- [x] Setup main responsive layout
- [x] Fetch locations and list them
- [x] Fetch characters and list them
- [x] Make a single location clickable and show associated characters
- [x] Make a single character clickable
  - [x] Show character metadata
  - [x] Allow users to add notes
    - [ ] Preferably a modal

## Making it Polished

- [ ] Add search capabilities
- [ ] Add Playwright tests
- [ ] Include more information on episodes

Feel free to explore the Rick & Morty universe with this interactive application!