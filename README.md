# images

Config files for a JupyterHub on the [National Research Platform](https://nationalresearchplatform.org/)

***in development***


- `up.sh` Runs a kubernetes helm chart deploy using `values.yaml` and `secrets.yaml` configuration on Nautilus.  See [official docs](https://ucsd-prp.gitlab.io/userdocs/jupyter/jupyterhub-service/) for details.


## Setup

* Organization setup (OAuth)
    * https://z2jh.jupyter.org/en/stable/administrator/authentication.html
    * Org settings > Developer settings (bottom of left panel) > OAuth apps > New OAuth
      app
    * Generate a client ID
    * Save as secrets in `secrets.yaml`:
      ```yaml
      hub:
        config:
          GitHubOAuthenticator:
            client_id: "...secret..."
            client_secret: "...secret..."
      ```
