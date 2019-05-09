# Git General Info

Get the PID of the task and kill it.

```text
lsof -ti:8080 | xargs kill
To list any process listening to the port 8080:

lsof -i:8080
To kill any process listening to the port 8080:

kill $(lsof -t -i:8080)
or more violently:

kill -9 $(lsof -t -i:8080)
```

