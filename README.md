# docker-boinc
CentOS based BOINC container image.

# Usage
Download docker-compose.yml from [this repository](https://raw.githubusercontent.com/IchikawaYukko/docker-boinc/master/docker-compose.yml). And modify hostname section in that file (The host name will be registered on project you will attach and may be seen on project's device manager. So it is important).

## Start container
`docker-compose up -d`

## Attach BOINC project
`docker-compose exec boinc boinccmd --project_attach PROJECT_URL AUTH`

### Example (World Community Grid):
`docker-compose exec boinc boinccmd --project_attach www.worldcommunitygrid.org  YOUR_KEY_HERE`

## Show status
`docker-compose exec boinc boinccmd --get_state`

## Show log (follow log tail)
`docker-compose logs -f`
