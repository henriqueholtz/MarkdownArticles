- Install Heroku cli

Two differences with dockerfile default (to heroku only):
1 - Use "CMD", not "ENTRYPOINT"... ex: 
CMD ASPNETCORE_URLS="http://$PORT" dotnet MyApi.dll
CMD ASPNETCORE_URLS="http://*:$PORT" dotnet MinimalApi-net6.dll

2 - Necessary define one user (don't can root) ex:
RUN useradd -m myappuser
USER myappuser

docker-compose.exe build

heroku login

"heroku apps:create nameApp" ---- ou ---- "heroku git:remote -a pomocontrolapi" (from deploy page application)

heroku container:login
heroku container:push web -a nameApp
heroku container:release web