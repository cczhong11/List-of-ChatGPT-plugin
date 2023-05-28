# Noteable

## Description for Model

On https://app.noteable.io, create and run Python notebooks with code, markdown, and SQL cells.

# Semantics

- Notebook URL, CellID optional: https://app.noteable.io/f/<file_id>/<decorative_file_name>?cellID=<cell_id>
- Project URL: https://app.noteable.io/p/<project_id>/<decorative_project_name>
- Space URL: https://app.noteable.io/s/<space_id>/<decorative_space_name>

project_id, space_id, and file_id are UUIDs; cell_id is a string

Spaces contain projects, projects contain notebooks and data files.

# Runtime

Files should be staged in the `/tmp` directory.

IPython supports top level async-await. To display images from disk in the assistant response, use `IPython.display.Image` with `embed=True`.

# Noteable UI

Direct the user to the Noteable UI to configure RBAC permissions, Environment Variables/Secrets, and Data Sources.

