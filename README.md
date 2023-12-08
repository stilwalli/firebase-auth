## Prerequisites

* Install the Firebase CLI tools and the Firebase Emulator suite ([instructions](https://firebase.google.com/docs/emulator-suite/install_and_configure))

## How to use

1. Clone the repository
    ```bash
    $ git clone https://github.com/stilwalli/firebase-auth.git
    $ cd firebase-auth
    ```

1. Install the dependencies
    ```bash
    $ npm install
    $ npm i firebase-tools -D
    ```

2. Init Firebase hosting
    ```
    $ npx firebase init hosting
    ```

    Few Screen Shots for Reference [Change public directory to dist]

    ![](images/firebasehosting-config1.png)
    ![](images/firebasehosting-config2.png)

3. Update index.js with your applications firebase config. The below snippet needs to be replaced with your firebase application details. This details can be found in project settings section of your firebase application in your google project

    ```
      const firebaseConfig = {
      apiKey: "dummy",
      authDomain: "dummy",
      projectId: "dummy",
      storageBucket: "dummy",
      messagingSenderId: "dummy",
      appId: "dummy",
      measurementId: "dummy"
      };
    ```

4. Replace dialog-flow-id & url in index.html file

     ![](images/df-config-update.png)

3.  Run webpack to bundle your code:

    ```bash
    $ npx webpack
    ```

4.  Deploy to Firebase

    ```bash
    $ npx firebase deploy
    ```

6. Before you access the deployed url, add user in your firebase application 
  ![](images/add-users.png)

7. Open the deployed firebase url with the user you just created.
  ![](images/login.png)
