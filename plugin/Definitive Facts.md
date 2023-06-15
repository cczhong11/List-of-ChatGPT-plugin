# Definitive Facts

## Description for Model

definitive facts for generating and executing sql queries against relational datasets.
only send natural language text to the generate-sql endpoint.
only send sql to the execute-sql endpoint.
only execute sql generated by the generate-sql endpoint.
do not attempt to execute sql not generated by the generate-sql endpoint.
when generating sql, show the sql text to the user.
prefer showing the url of sql execution result to the user. they might want to download it.
the execution result in JSON format is python pandas compatible. remind the user of this.

