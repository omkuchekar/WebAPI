#Once git code commti happens to docker-image branch then it should biuld the code and deploy on docker image registry docker.io using github actions and dockerimage
Steps to achieve above goal

1. We need to integrate docker with github by below steps.
https://docs.docker.com/atomist/integrate/github/

2.In https://hub.docker.com/ create empty docker image omkuchekar/githubtest

3.Create .github/workflows action by simpling going to actions in specific repository

4.It will create fodler as /.github/workflows with docker-image.yml

5.We need to checkout the code before building and pushing docker image

6.Write/update docker-image.yml accordingly.

7.Create Dockerfile at in root of github repository https://github.com/omkuchekar/WebAPI/tree/docker-image/Dockerfile

8. That contain any test data for testing purpose only.

9. FOr below go to settings of reposiroty and search for secrets and add respectvie key value date.
username: ${{ secrets.DOCKER_USERNAME }}
          password: ${{ secrets.DOCKER_PASSWORD }}
          
10. Follow below url for yml file data
https://github.com/marketplace/actions/docker-build-push-action
