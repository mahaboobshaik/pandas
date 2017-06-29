# pandas

- Basic import
    
        %matplotlib inline
        #The usual preamble
        import pandas as pd

- Reading csv data

        nyc_data = pd.read_csv("311-service-requests.csv")

- Header in the dataframe

        list(nyc_data)

- Stats in the data or particular column

        nyc_data["Complaint Type"].value_counts()

- Filtering

    - single  

            noise_complaints = nyc_data[nyc_data["Complaint Type"] == "Noise - Street/Sidewalk"]

    - Multiple
    
            noise_data = nyc_data["Complaint Type"] == "Noise - Street/Sidewalk"
            brooklyn_data = nyc_data["Borough"] == "BROOKLYN"

            nyc_data[noise_data & brooklyn_data]

- viewing first few columns

        noise_complaints[:3]

- 