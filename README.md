# Thanos JS (demo site)

Silly demo site to be used for [Netlify Drop](https://app.netlify.com/drop).

Preview demo site [right here](https://www.thanosjs.org).

Thanks to [Rasmus Andersson](https://twitter.com/rsms) for creating [Inter UI font](https://rsms.me/inter/).

# Steps to recreate:

Deploy on netlify:
<img width="1145" alt="image" src="https://user-images.githubusercontent.com/33653833/198926082-7e413468-b47d-40b5-b81f-16025e21ccb6.png">


To set up the snippet we can directly use the netlify website:

<img width="902" alt="image" src="https://user-images.githubusercontent.com/33653833/198925869-9e7743b6-9d35-40e2-a2b3-0af6beca0c09.png">

Have to set up the jobs on CircleCI:

<img width="1193" alt="image" src="https://user-images.githubusercontent.com/33653833/198926225-1d1217cb-5557-4fd2-9e58-79db263ec1e2.png">


Have to also change the directory so can find index.html: For example site directory = site in this example:
<img width="1149" alt="image" src="https://user-images.githubusercontent.com/33653833/198926347-255be290-20e9-4a52-aa39-116dcc8ae2b5.png">

We also need to get access to the env variabes of CircleCI and modify the Build Num value with the commads:

            sed "s/CIRCLE_BUILD_NUM/$CIRCLE_BUILD_NUM/" index.html > index1.html
            mv index1.html index.html
            
Finally, we have our website with build number shown at the bottom: https://effulgent-trifle-566bd9.netlify.app

<img width="962" alt="image" src="https://user-images.githubusercontent.com/33653833/198926757-94bdaae6-7c9f-4d41-9631-f1e76abbde79.png">






