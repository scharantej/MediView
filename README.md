## Design for Flask Application: Web app to fetch patient data from Bigquery and display it on UI

### HTML Files

1. **index.html**:
    - Serves as the landing page of the application.
    - Contains a form with a text input field to enter the patient's unique ID.
    - Includes a submit button that triggers the Flask route to fetch patient data.


2. **patient_data.html**:
    - Displays the patient's data retrieved from BigQuery.
    - Includes a table to organize and present the data in a user-friendly manner.

### Routes

1. **`/`**:
    - Handles GET requests for the landing page, displaying the `index.html` file.


2. **`/fetch_patient_data`**:
    - Handles POST requests triggered by the submit button on `index.html`.
    - Accepts the patient's unique ID as a form parameter.
    - Queries BigQuery using the provided ID to retrieve the patient's data.
    - Renders the `patient_data.html` template, passing the retrieved data to be displayed.

### Other Considerations

- **Database Connectivity**: To connect to BigQuery and retrieve patient data, you'll need to establish a connection to the BigQuery API. It is recommended to leverage the `google-cloud-bigquery` library for this purpose.

- **Patient Data Privacy**: Ensure that appropriate security measures are in place to protect the privacy and confidentiality of patient data. Employ measures like data encryption, access control, and user authentication to safeguard the data.