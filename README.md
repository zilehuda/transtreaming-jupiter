# Transtreaming (Translated Subtitles Using AgoraRTC SDK)

This tutorial describes how to run this app that translates voice of a person in a meeting with respect to other persons preferred language.

With this app, you can:

- Join a meeting room
- Select your preffered Language (You will shown subtitles with respect to the language selected)
- Leave the meeting room
- Apply two layouts views
- Hide a remote window

## Prerequisites

- Node.js 6.9.1+


## Quick Start

This section shows you how to prepare, build, and run this application.

- [Create an Account and Obtain an App ID](#create-an-account-and-obtain-an-app-id)
- [Update and Run the Sample Application](#update-and-run-the-sample-application) 


### Create an Account and Obtain an App ID
To build and run the sample application, you must obtain an app ID: 

1. Create a developer account at [agora.io](https://dashboard.agora.io/signin/). Once you finish the sign-up process, you are redirected to the dashboard.
2. Navigate in the dashboard tree on the left to **Projects** > **Project List**.
3. Copy the app ID that you obtained from the dashboard into a text file. You will use this when you launch the app.


### Update and Run the Sample Application 

1. Edit the [`src/agora.config.js`](src/agora.config.js) file. In the `AGORA_APP_ID` declaration, update `Your App ID` with your app ID.

```JavaScript
export const AGORA_APP_ID = 'Your App ID'
```

2. Download the [Agora Web Video SDK](https://www.agora.io/en/download/). Unzip the downloaded SDK package and copy the `AgoraRTC-*.js` file into the sample application's `/src/library/` folder. Rename the file to `AgoraRTC.js`.

	**Note:** CDN can now be used to retrieve the latest SDK. You do not have to re-download SDK updates.
		
3. Open the terminal and navigate to your project folder.

``` bash
cd path/to/project
```

4. Use `npm` to install the dependencies:

``` bash
# install dependency
npm install
```
5. Create an .env with the following details:

``` bash
REACT_APP_EUROPA_BASE_URL=  'Url For the back end this system'
```

The code for the back end of the project is located on the following repo  [Transtreaming Back End](https://github.com/zilehuda/transtreaming-europa)


6. Build and run the project:

Use `start` for a local build. View the application in your browser with the URL `http://localhost:3000`

```bash
# serve with hot reload at localhost:3000
npm run start
```
Use `build` for a production version with minification.

```bash
# build for production with minification
npm run build
```

## Application Flow
1. After setting up the application as described in the previous step open the application in the desired browser and Enter the room id.

![User Page][user-page]

2. Select your prefered language (You will recieve translated subtitles of the language you choose).
3. Repeat step 1 and 2 on the other attendee browser.
4. Now as both the attendees speak they will see translated text of the other attendee on thier screen.


## Resources
- Find full API documentation in the [Document Center](https://docs.agora.io/en/).


## License
This software is licensed under the MIT License (MIT). [View the license](LICENSE.md).

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[user-page]: user-page.PNG
[room]: room.png
