- runserver on 0.0.0.0 interface (localhost remains in container)
- Add 0.0.0.0 and docker-machine ip to settings
ALLOWED_HOSTS = ['0.0.0.0', '192.168.99.100']
- A project can contain multiple apps. An app can be in multiple projects.
