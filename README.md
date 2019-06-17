# set-env

Rails Dot Env will add a .env file to project's deploy shared folder. The benefits of using this role is that you can store
your secrets within the ansible vars rather than in the capistrano directory.

## Role Variables

Variable | Default | Notes
--- | --- | ---
set_env_owner | deploy | -
set_env_group | deploy | -
set_env_file | "/opt/{{project_name}}/shared/.env}}" | -
set_env_secrets | empty array | an array of key value pairs

### set_env_secrets example

```yaml
set_env_secrets:
      SECRET_KEY_BASE: xksyfne....
      DB_HOST: db.host.somewhere
      DB_DATABASE: a_database
      DB_PORT: 3306
      DB_USERNAME: mysql_user
      DB_PASSWORD: password
``` 
