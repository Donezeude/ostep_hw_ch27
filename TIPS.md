This is what I have noticed...

Macbooks stopped supporting Valgrind so I wasnt able to have it installed on my local machine.

Work around: I ended up making a docker container with an ubuntu image and installing valgrind on there

These are the commands I used to set myself up:

    docker run -it -v "$PWD":/src -w /src ubuntu:24.04 bash
    # once inside the container
    apt update && apt install -y valgrind build-essential


For the sake of the homework I will use valgrind but ThreadSanitizer is native to MacOS