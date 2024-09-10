Flask: A lightweight WSGI web application framework in Python.
request: Flask module to handle HTTP requests.
render_template: Flask function to render HTML templates.
redirect: Flask function to handle URL redirections.
url_for: Flask function to build URLs for specific functions.
storage: Google Cloud Storage client library.
GCS_BUCKET_NAME: The name of the Google Cloud Storage bucket where files will be uploaded.
storage_client: An instance of the Google Cloud Storage client.
bucket: Represents a Google Cloud Storage bucket.
blob: Represents an object (file) in a Google Cloud Storage bucket.
upload_from_file: Method to upload files to Google Cloud Storage.
request.files: Flask property to handle file uploads.
request.method: Flask property to check the HTTP method (GET or POST).
app.run(debug=True): Runs the Flask application in debug mode.
GOOGLE_APPLICATION_CREDENTIALS: Environment variable for the path to the Google Cloud service account key.

functions_framework: Framework for deploying functions to Google Cloud Functions.
cloud_event: Represents the event data triggered by a change in a Google Cloud Storage bucket.
bigquery: Google Cloud BigQuery client library.
LoadJobConfig: Configuration for loading data into BigQuery.
hello_gcs(cloud_event): Function triggered by a change in a Google Cloud Storage bucket.
data: Contains event data related to the cloud event.
event_id: Unique identifier for the event.
event_type: Type of the event (e.g., object creation in GCS).
bucket: Name of the Google Cloud Storage bucket.
filename: Name of the file that triggered the event.
metageneration: Metadata generation number for the object.
timeCreated: Timestamp when the object was created.
updated: Timestamp when the object was last updated.
load_bq(filename): Function to load data from a CSV file in GCS to BigQuery.
client: An instance of the BigQuery client.
dataset: BigQuery dataset name.
table: BigQuery table name.
table_ref: Reference to the BigQuery table.
job_config.source_format: Specifies the source format of the data (CSV in this case).
job_config.skip_leading_rows: Skips the leading rows in the CSV file (header row in this case).
job_config.autodetect: Enables schema autodetection for the data.
uri: URI of the file in Google Cloud Storage.
load_job: Represents a BigQuery load job.
load_job.result(): Waits for the load job to complete.
num_rows: Number of rows loaded into BigQuery.

#API calls

GET: Retrieve data from the server.
POST: Send data to the server to create or update a resource.
PUT: Update an existing resource or create a new one.
DELETE: Remove a resource from the server.
PATCH: Apply partial updates to a resource.
OPTIONS: Describe communication options for the target resource.
HEAD: Retrieve headers of a resource without the body.