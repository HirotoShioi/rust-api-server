# Rust API server

API server build with rust using [actix-web](https://actix.rs/)

- API which supports simple CRUD for User and Post data
- Database using [Diesel](http://diesel.rs/)
- Supports authentication using [argon2](https://docs.sru-systems.com/rust-argon2/0.8.0/argon2/)
- Use [actix-session](https://docs.rs/actix-session/0.3.0/actix_session/) for authentication caching
- Logging using [env-logger](https://docs.rs/env_logger/0.7.1/env_logger/) and [log](https://docs.rs/log/0.4.8/log/)

## How to run

Run docker-compose

```
> docker-compose up
```

```terminal
> systemfd --no-pid -s http::8081 -- cargo watch -x run
```

## Required Environment Variable

| Name 	| Description  	|
|---	|---	|
| RUST_LOG  	| For logging  	|
| HOST  	| Host IP Address   	|
| PORT  	| IP port for exposing the API server  	|
| DATABASE_URL  	| Url for postgres database  	|
| REDIS_HOST  	| IP port for Redis  	|
| REDIS_PORT  	| IP port for Redis  	|
