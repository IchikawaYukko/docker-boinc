# docker-boinc
CentOS based BOINC container image.

# Usage
Download docker-compose.yml from this repository. then...

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
