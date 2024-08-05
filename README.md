# Spotify 2024 Bollywood Albums Analytics 


In this project, I have built End to End ETL pipeline for analyzing Top 8 2024 Bollywood Albums from spotify api provided using [RapidApi](https://rapidapi.com/Glavier/api/spotify23). This project is entirely built on AWS.


### AWS Services & Libraries Used:

* S3
* EC2
* Lambda
* apache-airflow-providers-amazon
* Redshift
* QuickSight



## Final QuickSight Dashboard generated




![Album Vs Popularity](https://github.com/user-attachments/assets/39558e85-c30b-413a-acad-77a4ae41a53a)


![Total Tracks](https://github.com/user-attachments/assets/e635bf0e-1e88-4aa0-a9a9-d2a3fec911d8)


&nbsp;
&nbsp;
&nbsp;


### Insights:

* Animal Movie Album has the highest popularity score (76) among the choosen albums.
* Rocky Aur Rani Kii Prem Kahaani has the highest number of tracks (15) among the choosen albums.






### Architecture

![AWS Architecture](https://github.com/user-attachments/assets/9d4c62e6-70d0-48c7-b85c-1c2c93b69baf)










### Dag Built

![dag](https://github.com/user-attachments/assets/e97f96ad-4967-41ac-93a0-e0c544ee7805)


Tasks:
* extract_spotify_data_var -- extracts data from api and stores in a json file
* load_to_s3 -- load the json into S3 bucket called raw bucket
* is_file_in_s3_available -- Will check if the data is in S3 or not before loading into Amazon redshift
* transfer_s3_to_redshift -- Will load the data into redshift
