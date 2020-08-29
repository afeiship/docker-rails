# get started
- https://blog.cloud66.com/deploying-rails-6-assets-with-docker/
- https://github.com/vinsgit/docker_study
- https://medium.com/@AnjLab/how-to-set-up-elk-for-rails-log-management-using-docker-and-docker-compose-a6edc290669f
- http://equinox.one/blog/2016/04/20/Docker-with-Ruby-on-Rails-in-development-and-production/

## steps
1. copy `Dockerfile`
2. copy `docker-compose.yml`
3. create your app(If your app existe ignore this step)
   1. rails g scaffold post title:string content:string`
   2. rake db:migrate
4. docker-compose up (Make sure your docker service has started.)