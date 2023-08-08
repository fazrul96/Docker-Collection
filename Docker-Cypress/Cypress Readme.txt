docker run -it -v $PWD:/e2e -w /e2e cypress/included:3.4.0

docker run -it -v C:/Users/muhammad.f.romli/spora/Cypress-ACN/cypress/e2e/1-getting-started:/e2e -w /e2e --name cypress cypress/included:12.11.0


docker run --interactive --tty --env PORT=8999 --publish 8999:8999 sentimentalyzer