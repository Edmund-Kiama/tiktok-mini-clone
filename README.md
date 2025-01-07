# Vue Video List Application

This is a Vue.js application that displays a list of videos with user data such as likes, comments, shares and saves. The app uses a component-based architecture to render the top navigation, sidebar and video content.It offers a clean and modular structure. The video content is dynamically passed as a prop to the main content component.

## Features

### Core Functionality

- **Video List**: Displays a list of videos along with relevant metadata such as likes, comments, shares and saves.
- **Modular Components**: The app is divided into several reusable components, each responsible for a specific part of the UI.
- **Dynamic Data**: The video list is dynamically rendered from a JavaScript array passed to the main content component.

### Highlights

- **Top Navigation**: A top navigation bar for site-wide navigation.
- **Sidebar**: A sidebar component for additional navigation or actions.
- **Main Content Area**: Displays video content and associated engagement metrics.
- **Dynamic Data Handling**: Uses props and data binding to dynamically pass and display video information.

## Application Structure

The application consists of the following main components:

### Components

1. **`headTag.vue`**  
   A component that sets the meta tags and title for the page (usually placed within the `<head>` tag of the HTML)
   
2. **`topNav.vue`**  
   Displays the top navigation bar, typically containing links or actions that are globally accessible across the site.
   
3. **`SideBar.vue`**  
   A sidebar component that could be used for additional navigation, filters, or actions related to the video content.

4. **`mainContent.vue`**  
   This is the primary component that displays the video list. It accepts a prop (`video-list`) containing the list of video data.

## Core Logic

### Data Binding in `App.vue`

- The video list is stored in a `videoList` array, with each object containing details about the video, such as:
  - `profilePic`: URL of the profile picture of the video uploader.
  - `video`: URL of the video.
  - `like`: Number of likes the video has received.
  - `comments`: Number of comments on the video.
  - `save`: Number of saves the video has.
  - `shares`: Number of times the video has been shared.
  
### Components Interaction

- **topNav.vue**: This component is rendered in the header of the application. It could contain navigation links to other parts of the site.
- **SideBar.vue**: The sidebar could include extra controls or filters for managing videos, or provide links to other sections of the application.
- **mainContent.vue**: This component receives the videoList as a prop and displays the videos dynamically. It could display the profile picture, video file, and engagement metrics (likes, comments, shares, and saves).

## How to Use

### Prerequisites

- Ensure that you have the following installed:
    1. **Node.js**: Required for running the development server.
    2. **npm**: Package manager for managing dependencies.

### Installation

1. Clone this repository.
2. Navigate into the project folder.
3. Install the necessary dependencies:`npm install`

### Running the Application
1. To start the development server, run the following command
2. Once the server is running, open your browser and go to:

## Technologies Used

1. **Vue.js**: A progressive JavaScript framework used for building the user interface and handling dynamic data binding.
2. **JavaScript**: The programming language used to manage the data and functionality of the application.
3. **CSS**: Used to style the components and layout of the application.

## License

This project is licensed under the MIT License. 
