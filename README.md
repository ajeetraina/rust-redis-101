# Getting Started with Redis and Rust

## Pre-requisite

- Install Rust on your Mac system

Rust is installed and managed by the rustup tool.

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```


## Configure your current shell:
 
```
source $HOME/.cargo/env
```

## Verify Rust compiler:
 
```
rustc --version
rustc 1.49.0
```

- Install Redis

```
docker run --rm -p 6379:6379 redis
```

## Steps 



### Clone the repository

```
git clone https://github.com/ajeetraina/rust-redis-101.git
cd rust-redis-101
```

### Export

If you’re using a local Redis server (e.g. with Docker) over an insecure connection without any password, simply use:

```
export REDIS_HOSTNAME=localhost:6379
```


### Run the application


```
cargo run
```

## Verify the Output


```
******* Running SET, GET, INCR commands *******
value for 'foo' = bar
counter = 2
******* Running HASH commands *******
info for rust redis driver: {"name": "redis-rs", "repo": "https://github.com/mitsuhiko/redis-rs", "version": "0.19.0"}
go redis driver repo name: "https://github.com/go-redis/redis"
******* Running LIST commands *******
first item: item-1
no. of items in list = 2
listing items in list
item: item-2
item: item-3
******* Running SET commands *******
does user1 exist in the set? true
listing users in set
user: user2
user: user1
******* Running SORTED SET commands *******
listing players and scores
player-1 = 1
player-4 = 6
player-5 = 6
player-2 = 7
player-3 = 9
```

## Conclusion

Today you learned how to use the Rust driver for Redis to connect and execute operations in Redis.
