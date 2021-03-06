# Tic Tac Toe on Google App Engine Standard using Firebase

This directory contains a project that implements a realtime two-player game of
Tic Tac Toe on Google [App Engine Standard][standard], using the [Firebase] database
for realtime notifications when the board changes.

[Firebase]: https://firebase.google.com
[standard]: https://cloud.google.com/appengine/docs/about-the-standard-environment

## Prerequisites

* Install [Apache Maven][maven] 3.0.5 or later
* Install the [Google Cloud SDK][sdk]
* Create a project in the [Firebase Console][fb-console]
* In the [Overview section][fb-overview] of the Firebase console, click 'Add
  Firebase to your web app' and replace the contents of the file
  `src/main/webapp/WEB-INF/view/firebase_config.jspf` with that code snippet.
* If using the development appserver to run the app locally, you must supply
  credentials that would otherwise be inferred from the App Engine environment.
  Download [service account credentials][creds] and set the
  `GOOGLE_APPLICATION_CREDENTIALS` environment variable to its path:

        export GOOGLE_APPLICATION_CREDENTIALS=/path/to/your/credentials.json


[fb-console]: https://console.firebase.google.com
[sdk]: https://cloud.google.com/sdk
[creds]: https://console.firebase.google.com/iam-admin/serviceaccounts/project?project=_&consoleReturnUrl=https:%2F%2Fconsole.firebase.google.com%2Fproject%2F_%2Fsettings%2Fgeneral%2F
[fb-overview]: https://console.firebase.google.com/project/_/overview
[maven]: https://maven.apache.org


## Run the sample

* To run the app locally using the development appserver:

    ```sh
    $ mvn appengine:run
    ```

## Troubleshooting

* If you see the error `Google Cloud SDK path was not provided ...`:
    * Make sure you've installed the [Google Cloud SDK][sdk]
    * Make sure the Google Cloud SDK's `bin/` directory is in your `PATH`. If
      you prefer it not to be, you can also set the environment variable
      `GOOGLE_CLOUD_SDK_HOME` to point to where you installed the SDK:

        ```sh
        export GOOGLE_CLOUD_SDK_HOME=/path/to/google-cloud-sdk
        ```

## Contributing changes

See [CONTRIBUTING.md](../../CONTRIBUTING.md).

## Licensing

See [LICENSE](../../LICENSE).

