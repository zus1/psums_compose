<h3>About</h3>
This is a one simple way to run all container for Psums project, without pulling each repo from git.
Its ideal as production environment since it dose not require to pull downs source code. But it can't be
used in development environment (its also preferred way to install project).

<h3>Installation</h3>
This is the second way to install Psums project. First one is described in other project repositories.
For composed installation clone this repo, and then just run:<br><br>
<pre><code>docker-compose up</code></pre>
And wait few minutes until it builds up all containers. After that is done database migrations needs to be run.
Project uses Phinx to handle migrations. Bash into psums_aggregator container
<br>
<pre><code>docker container exec -it psums_aggregator bash</code></pre>
You should be in /var/www/html directory. There run
<pre><code>php library/phinx/bin/phinx migrate</code></pre> 
After migrating finishes you are all set up, and Psum is ready to use. <br><br>
Checkout other Psums repos for more know how
<ul>
    <li><a href="https://github.com/zus1/psums_aggregator">Aggregator</a></li>
    <li><a href="https://github.com/zus1/psums_streams">Streams</a></li>
    <li><a href="https://github.com/zus1/psums-api">Api</a></li>
</ul>
Have fun!