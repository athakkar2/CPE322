# Lab 6 Documentation

## Node.js

After installing Node.js, I ran the first script called hello_world.js using the following command:

```bash
node hello_world.js
```

This ran on my localhost on port 3000, which made the address 127.0.0.1:3000 look like this in my browser:

![hello_world](Lab6_1.png)

Then, I tried running the hello.js script but was getting a 404 not found error. I found out that this was because the hello.js script was trying to listen on port 8080 of my localhost which was being used by something else. So I changed the script to listen on port 3000, and ran the follwing command to start the server:

```bash
node hello.js
```

When I refreshed the page, I saw the same hello_world.js screen but this time the script outputted on my terminal when someone tried to access the site, as can be seen below:

![hello](Lab6_2.png)

Finally, I tried to run http.js but ran into the same problem, so I changed the port to 3000 and ran the server using the following command:

```bash
node http.js
```

After refreshing the page, I saw that the site was tracking how many times I refreshed the page and outputting it on both my browser and terminal. After refreshing the page a few times the site and terminal looked like this:

![http](Lab6_3.png)

## Pystache

After installing Pystache, I outputted what the mustache template had and what the python script had followed by running the python script by using the following commands:

```bash
cat say_hello.mustache
cat say_hello.py
python say_hello.py
```

This resulted in the following terminal output:

![stache](Lab6_4.png)

For a full log dump of my terminal please click [here](lab6.txt).
