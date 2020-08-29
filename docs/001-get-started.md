# get started
- https://blog.cloud66.com/deploying-rails-6-assets-with-docker/
- https://github.com/vinsgit/docker_study
- https://medium.com/@AnjLab/how-to-set-up-elk-for-rails-log-management-using-docker-and-docker-compose-a6edc290669f
- http://equinox.one/blog/2016/04/20/Docker-with-Ruby-on-Rails-in-development-and-production/
- https://nokogiri.org/tutorials/installing_nokogiri.html
- https://stackoverflow.com/questions/35022428/rails-server-is-still-running-in-a-new-opened-docker-container
- https://stackoverflow.com/questions/49316462/how-to-update-existing-images-with-docker-compose
- https://semaphoreci.com/community/tutorials/dockerizing-a-ruby-on-rails-application

## steps
1. copy `Dockerfile`
2. copy `docker-compose.yml`
3. create your app(If your app existe ignore this step)
   1. rails g scaffold post title:string content:string`
   2. rake db:migrate
4. docker-compose up (Make sure your docker service has started.)