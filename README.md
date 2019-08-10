# ETL Project

For our project, we decided to create a database of data showing the sales of videogames over the past 50 years and the data surrounding mass shootings in the US over the past decade. The goal once these databases are loaded would be to analyze and produce graphs showing the trends relating the two.

For our first data set, we took video game sales from PlayStation4, XboxOne, and Other platforms (Such as Wii). The data included sales in multiple regions, some of the main ones are North America, Europe, and Japan. We decided to only compare North America and Europe's data.

The E in ETL stands for extract. After we extracted the data, converted it from UTF-16 to UTF-8 and loaded it into pandas, we further extracted only the columns necessary, ultimately getting rid of the other region's sales data.

For our second data set, we took data surrounding mass shootings in the US for the past decade. Just as we did the previous data set, we converted the csv's to UTF-8, loaded it into pandas, and extracted only the necessary data, such as the location, the total number of injured victims, etc.

The T in ETL stands for Transform. Once the data was extracted, we needed to transform all of the data sets. For the data on video games, all of the data needed to be cleaned of NaN values. After, the datasets all needed to be merged into one, in order to be readed to be loaded into the final SQL database.

For the Mass Shootings dataset, to transform it to be ready to be loaded into the SQL database, more columns needed to be cut in order to make the data as complete as possible. The columns for both sets of data, after it was merged or cut, needed to be renamed to titles that were relevent and easy to understand.

Finally, the L in ETL stand for Load. We took both complete sets of data and loaded into sql using sqlalchemy. In order to do this, we had to create and engine allowing us to connect to PostgreSQL. The data's columns needed to be renamed again in order to be loaded. After that, our database was ready to be used.
