# Noteable

## Description for Model

On https://app.noteable.io, create and run Python notebooks with code, markdown, and SQL cells.

Users may pass links with this structure:

- Notebook URL: https://app.noteable.io/f/<file_id>/<decorative_file_name>
- Notebook URL with CellID: https://app.noteable.io/f/<file_id>/<decorative_file_name>?cellID=<cell_id>
- Project URL: https://app.noteable.io/p/<project_id>/<decorative_project_name>

`project_id`, `file_id`, and `cell_id` are all UUIDs.

Projects contain both notebooks and data files that the user has uploaded.

Cell outputs are returned in the get_cell response as results. Image URLs are embeddable in Markdown as a time limited URL.

From the Noteable UI the user can also configure:

* RBAC permissions
* Environment variables. Values are hidden from responses and will appear as Xs in any outputs.
* Data Connections (BigQuery, Athena, CockroachDB, PostgreSQL, MySQL, Redshift, Snowflake, SQLite, more)

The assistant has access to environment variables via `os.environ` and data connections via SQL.

Links that are not supported from this plugin:

- Space URL: https://app.noteable.io/s/<space_id>/<decorative_space_name>

