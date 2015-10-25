# webpack-in-26-lines

I've been meaning to checkout webpack for a while, so this morning I went through this [short, well-written tutorial](http://jamesknelson.com/webpack-made-simple-build-es6-less-with-autorefresh-in-26-lines/)

To see something up and running quickly, you can run my Dockerfile with node and the webpack-dev-sever pre-installed

    git clone https://github.com/bradleybossard/webpack-in-26-lines.git
    cd webpack-in-26-lines
    docker run -i -t --rm -p 8110:8080 -v $PWD:/src bradleybossard/docker-node-tools
    webpack-dev-server --host 0.0.0.0  --content-base src src/main.js

Which should show you a spinning triangle on port 8110 of whatever server you are running it on.  I addd the --host 0.0.0.0 flag b/c I am always deving on a machine in the cloud (not a local machine).
