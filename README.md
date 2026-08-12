# closerzcollective.com

This repository exists to host one file: the Closers Collective CRM app, served
at <https://closerzcollective.com> by GitHub Pages.

`index.html` is the whole application — interface, logic, and the Supabase
client library, in a single file with no build step.

### Why this is public

It has to be. It is a web page: anyone who loads the site can read every line of
it with View Source. Putting it in a public repository exposes nothing that
visiting the site does not already expose.

Nothing secret lives here. The Supabase key in the file is the **anon** key,
which is designed for front-end code — it names the project, it does not grant
access. Access is granted by row-level security inside Postgres, per signed-in
user. The `service_role` key is the dangerous one and it is not in this file.

### Where the rest lives

The database schema, the row-level security policies, the edge functions, the
tests and the setup guide are in the **private** `closers-collective-crm`
repository. Only this page is public.
