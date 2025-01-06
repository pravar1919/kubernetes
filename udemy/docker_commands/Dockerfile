FROM ubuntu

ENTRYPOINT ["sleep"]

CMD ["5"]


# in the above example if we run 
# docker build -t ubuntu-sleeper .
# docker run ubutnu-sleeper 10 # we can directly pass the arguments in the command line.
# here if we want to change the entrypoint we can use.
# docker run --name ubuntu-sleeper --entrypoint sleep2.0 ubuntu-sleeper 10


FROM ubuntu

ENTRYPOINT ["sleep"]

# here we have to only specify if we want to modify the sleep time
# docker run ubuntu-sleeper sleep 10

# here if we do not specify the number in the command line, it will throw us an error,
# so for that we have to combine the CMD as well as EXECUTABLE both commands together.
# As shown above.


FROM ubuntu

CMD ["sleep", "5"]

# docker run ubuntu-sleeper 10
