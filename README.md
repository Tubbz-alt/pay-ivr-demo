# Deploying

Log into pass invironment using `cf login` (see https://docs.cloud.service.gov.uk/get_started.html#get-started)

Target the appropriate space `cf target -S {spacename}`

then
`cf push`

Add network policy between ivr-demo and connector:
`cf add-network-policy ivr-demo --destination-app card-connector --protocol tcp --port 8080`