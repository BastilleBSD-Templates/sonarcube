# sonarcube
Bastille Template for a Sonarqube Jail

 STATUS: Testing

Create the DB for Sonarqube

SONARQUBE_USER="sonarqube"
SONARQUBE_DATABASE="sonarqube"
SONARQUBE_PASSWORD="secret.password"

createuser "${SONARQUBE_USER}"
psql -c "ALTER USER ${SONARQUBE_USER} WITH PASSWORD '${SONARQUBE_PASSWORD}';"
createdb "${SONARQUBE_DATABASE}"
psql -c "GRANT ALL PRIVILEGES ON DATABASE ${SONARQUBE_DATABASE} TO ${SONARQUBE_USER};"



to test that sonarcube is working run the following:

	curl localhost:9000



