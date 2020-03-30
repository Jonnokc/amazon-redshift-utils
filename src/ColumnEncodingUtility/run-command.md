<!--The following command runs the analyze compression script on the database.
It will analyze compression for each column as well as table size.

analyzes the entire Public schema and the tables within

Table modifications will be done directly within the primary table, a copy of the original table will remain in the database.
-->

<!-- command for analyzing all tables in schema -->
python analyze-schema-compression.py --db='di' --db-user='<USERNAME>' --db-pwd='<PASSWORD>' --db-host='data-intelligence-osiris.c7plurt8yvk1.us-west-2.redshift.amazonaws.com' --db-port='5439' --analyze-schema='public' --analyze-cols=True --do-execute=True --output-file='/Users/ja052464/Downloads/redshift-optimizer-output.txt' --suppress-cloudwatch=True

<!-- command for analyzing specific table in schema -->
python analyze-schema-compression.py --db='di' --db-user='<USERNAME>' --db-pwd='<PASSWORD>' --db-host='data-intelligence-osiris.c7plurt8yvk1.us-west-2.redshift.amazonaws.com' --db-port='5439' --analyze-table='<TABLE_NAME>' --analyze-cols=True --do-execute=True --output-file='/Users/ja052464/Downloads/redshift-optimizer-output.txt' --suppress-cloudwatch=True
