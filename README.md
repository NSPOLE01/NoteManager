<h1 align ="center"> 
    Note Manager
</h1>

<p align="center">
    <img width="200" src="https://images.emojiterra.com/twitter/v13.1/512px/1f4dd.png" alt="Note Emoji">
</p>





A react + redux dummy web application that allows users to create, view, edit, and delete any notes that they wish to store. This web application is able to store all of these notes internally so that when the webpage is refreshed, the notes are still editable, manageable, and visible. 

## Getting Started
```git clone https://github.com/NSPOLE01/NoteManager``` to get a copy of this repository on your local
```brew install node``` to install NPM
```npm install``` to download all of the required dependencies
```npm start``` to spin up a local host react application
```npm install -g json-server``` to globally download and be able to run a fake-backend locally
```npm run dev-server``` in a separate terminal to be able to spin-up the fake-backend


## Features    
1. Creating Notes: Should a user want to create a note, they simply click a button and they are redirected to a different web page with an input field for a title and a text. After following the input validations, they are able to click the submit button. On submission, the note is taken and stored inside the db.json file and inside the dummy database.
2. Storing Notes: Using Redux, all of the notes created by the user are stored in the local database and can be seen/managed via the db.json file. The local server has 2 API endpoints related to storing notes: fetchByID and fetchAll. FetchByID allows the user to search for a specific note, and have that note returned to them (this is particularly useful when it comes to deleting and editing). FetchAll allows the user to view all of the notes that they currently have. 
3. Editing Notes: Should a user want to edit a previously created note, they are able to click on the pencil icon to edit it. This triggers the updateByID endpoint which fetches the note from the database and displays the note in an editable template in a new webpage. The user will then be redirected to this page where they can modify the note. After submitting the changes, the new note will now be stored in the database. 
4. Deleting Notes: Should a user want to rid of a previously created note, they are able to click on the trash icon to delete it. This triggers the delete endpoint, which searched for the noteID in the database and removes it. From here, the note will no longer be shown in the manage notes section. 
5. Different web pages for each function: Using react-router, every time one of the above functionalities was invoked, the user would be taken to a completely new web page with a unique url. 
6. Dummy Database and Server API Calls: Using Redux a simple local server was developed with 5 API endpoints (delete, create, update, fetchByID, fetchAll). When the frontend calls this local backend, the return value of each API is stored and displayed in the UI.  


