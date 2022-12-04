### Upload query results to Google BigQuery table with Google Cloud SDK on Docker

##### Modify "key.json" according to your Google service account credentials
> nano key.json

##### Modify "query.sql" according to your needs
> nano query.sql

##### Create Google Cloud SDK container with Docker Compose
> sudo docker compose up -d

##### Install required Python packages
> sudo docker exec -it gcloud sh -c "pip install google-cloud-bigquery && pip install sqlparse"

##### Run the script to upload a remote file
> sudo docker exec -it gcloud sh -c "python3 main.py [DATASET] [TABLE]"

##### Example command
> sudo docker exec -it gcloud sh -c "python3 main.py data_fellowship results"
