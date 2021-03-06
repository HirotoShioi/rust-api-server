# Rust API server

![Rust](https://github.com/HirotoShioi/rust-api-server/workflows/Rust/badge.svg)
![Lint Code Base](https://github.com/HirotoShioi/rust-api-server/workflows/Lint%20Code%20Base/badge.svg)

API server build with rust using [actix-web](https://actix.rs/).

Transcribed from this [article](https://cloudmaker.dev/how-to-create-a-rest-api-in-rust/).

Uploaded to github to test out github actions.

- API which supports simple CRUD for `User` and `Post` data
- Database using [Diesel](http://diesel.rs/)
- Support session based authentication using [actix-session](https://docs.rs/actix-session/0.3.0/actix_session/)
- Logging using [env-logger](https://docs.rs/env_logger/0.7.1/env_logger/) and [log](https://docs.rs/log/0.4.8/log/)

## How to run

Run docker-compose

```terminal
> docker-compose up
```

```terminal
> systemfd --no-pid -s http::8081 -- cargo watch -x run
```

## Required Environment Variable

| Name          | Description |
|---            |--- |
| RUST_LOG      | For logging |
| HOST          | Host IP Address |
| PORT          | IP port for exposing the API server |
| DATABASE_URL  | Url for postgres database |
| REDIS_HOST    | Host IP address for Redis |
| REDIS_PORT    | IP port for Redis |


## TODO

- Experiment with `anyhow` and `thiserror`
- Containerize this repo and deploy them somewhere
- Try to generate swagger document