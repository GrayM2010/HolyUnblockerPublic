# Holy Unblocker

A website that can be used to bypass web filters; both extension and firewall. This is the public source code for Holy Unblocker, a rather fancy website with some cool dynamic backgrounds while also focusing with detail put into the design and mechanics overall. Also has cool features like custom Tab Cloaks and with more to come. Works on a large number of sites including YouTube (Full Quality Support), Discord, CoolMathGames and more! Be sure to check the various branches as I update Holy Unblocker often with open access to yet to be released versions.

<img src="https://raw.githubusercontent.com/QuiteAFancyEmerald/HolyUnblockerPublic/master/views/assets/img/hbpreview.png?raw"></img>

Official Site: https://www.holyubofficial.net

Site Documentation: <a href="https://www.holyubofficial.net/?in">Documentation</a>

Instance Status: <a href="https://status.holyubofficial.net/?update">Status</a>

Be sure to join Titanium Network's Discord for more official site links: https://discord.com/invite/tgT48PH

<a href="https://heroku.com/deploy?template=https://github.com/QuiteAFancyEmerald/HolyUnblockerPublic" title="Deploy to Heroku"><img alt="Deploy to Heroku" src="https://raw.githubusercontent.com/QuiteAFancyEmerald/HolyUnblockerPublic/master/views/assets/img/heroku.svg?raw" width="140" height="30"><img></a>
&nbsp;
<a href="https://azuredeploy.net/" title="Deploy to Azure"><img alt="Deploy to Azure" src="https://raw.githubusercontent.com/QuiteAFancyEmerald/HolyUnblockerPublic/master/views/assets/img/azure.svg?raw" width="140" height="30"><img></a>
&nbsp;
<a href="https://repl.it/github/QuiteAFancyEmerald/HolyUnblockerPublic" title="Run on Repl.it"><img alt="Run on Repl.it" src="https://raw.githubusercontent.com/QuiteAFancyEmerald/HolyUnblockerPublic/master/views/assets/img/replit.svg?raw" width="140" height="30"><img></a>
&nbsp;
<a href="https://glitch.com/edit/#!/import/github/QuiteAFancyEmerald/HolyUnblockerPublic" title="Remix on Glitch"><img alt="Remix on glitch" src="https://raw.githubusercontent.com/QuiteAFancyEmerald/HolyUnblockerPublic/master/views/assets/img/glitch.svg?raw" width="140" height="30"><img></a>

## Table of contents:

- [Setup](#how-to-install)
	- [Structure](#structure)
		- [Structure Information](#structure-information)
	    - [Static Files](#details-of-public)
	    - [Proxy Scripts](#scripts-located-in-expr)
	    - [Cookie Auth](#details-of-authjs)
	- [Future Additions](#future-additions)
	- [Beginner's Explanation](#vauge-explanation-for-beginners-with-external-proxies-and-hosting)
	  - [Hosting Providers](#list-of-some-good-hosting-options)
	  - [Heroku Setup](#heroku-steps)
	  - [Domain Setup](#freenomdomain-steps)
	  - [Cloudflare Setup](#cloudflare-steps)
	  - [Workspace Configurations](#workspace-configurations)
	- [More Information](#more-information)

## How to Setup

Either use the button above to deploy to Heroku or do the below:

```
git clone https://github.com/QuiteAFancyEmerald/HolyUnblockerPublic.git

cd HolyUnblockerPublic

npm install

npm start
```

The default place for the proxy when its started is `http://localhost:8081` but you can change it if needed in config.json

This website has been hosted locally on Alloy Proxy. More more information go to the Alloy Proxy repo below.


## Structure
- `index.html` : The official homepage of the site.
- `surf.html` : Surf Freely page, page offers to be redirected to either Alloy or Node.
- `alloy.html` : Alloy Proxy page, configured as recommended with Alloy Proxy.
- `node.html` : Links to a subdomain for Node Unblocker. I left it in just in case you would like to setup the site differently.
- `pmprox.html` : Links to a subdomain for Powermouse. I left it in just in case you would like to setup the site differently.
- `gtools.html` : Games page, help from @BinBashBanana and @kinglalu.
- `info.html` : WIP Documentation.
- `discordhub.html` : Hub for the discord proxy and its links.
- `discordprox.html` : Links to a discord proxied through Alloy.
- `pydodge.html` : Links to a subdomain with PyDodge B. Created by OlyB from a modified Via Proxy.
- `flash.html` : Games page for flash games, credits given to @BinBashBanana and Titanium Network for its assets.
- `icons.html` : Information regarding Settings Menu page. Added this in for standard users.
- `terms.html` : Terms of Services, AUP and Privacy Policy page.
- `gba.html` : Locally hosted Gameboy Emulator.
- `krunker.html` : An iframe version of Krunker with keyword changes. Can be removed if not needed.
- `youtube.html` : An proxied version of Youtube running off of the locally hosted Alloy Proxy.
- `ythub.html` : Page linking proxied Youtube.
- `ytmobile.html` : Page linking to a proxied YouTube for mobile users.
- `chatbox.html` : Links to an externally hosted Chatbox.
- `bookmarklets.html` : Page for Bookmarklets.
### Structure Information
- `/public/` : The physical site base of Holy Unblocker goes here. Do not delete or modify `/utils` as its needed for Alloy.

#### Details of `/views/`
- `/pages/` is used for important pages for the site.
- `/expr/` is used for important proxy scripts.
- `/archive/` is used for game related assets and pages.
-  `/assets/` is used for various assets for CSS, JS and Bootstrap.
- `/vibeOS/` is used for vibeOS, an in-browser OS enviroment.

#### Scripts located in `/expr`
- `surf.js` is used for proxy navigation; both stealth mode and classic mode.
- `load.js` is used for initializing the surf script. Must be located in the `<head>` tag.

## Future Additions
- Expansive game library
- Various parity changes.

## Vauge Explanation for Beginners With External Proxies and Hosting
You will first want to host your proxies locally or externally. 

#### List of some good hosting options:
- <a href="https://heroku.com">Heroku</a> (Free)
- <a href="https://nodeclusters.com">NodeClusters</a> (Paid)
- <a href="https://glitch.com">Glitch</a> (Free)
- <a href="https://repl.it">Repl.it</a> (Free)
- <a href="https://azure.microsoft.com/en-us/">Azure</a> (Free and Paid)

Out of the list of hosting providers Heroku and NodeClusters rank first as a preference. You may also self-host. Currently at this time Azure is used to host the official Holy Unblocker sites.

After you have selected a decent VPS, use Cloudflare for the DNS records for both the site and the subdomains for the proxies.

This is an example of DNS records involving Heroku. Self-hosting will require `A records` preferably.
<img src="https://cdn.discordapp.com/attachments/725506757291671663/756659513179766844/unknown.png" width="500" height="154"></img>

- `a.deepsoil.ml` is being used for Node Unblocker.
- `p.deepsoil.ml` is being used for Powermouse.
- `pd.deepsoil.ml` is being used for PyDodge B.
- `cdn.deepsoil.ml` is being used for a private Alloy host on the official sites.

Update, the new configuration is:

- `a.deepsoil.ml` is being used for Node Unblocker.
- `c.deepsoil.ml` is being used for Powermouse and the Chatbox.
- `cdn.deepsoil.ml` is being used for a private Alloy and Via host on the official sites.

As stated previously, Holy Unblocker is hosted locally with Alloy.

#### Heroku Steps
**So use Heroku to host. I personally favor it as a free choice.** 
- First obtain a card; (Prepaid, Debit, and Credit Cards work). You need this to add custom domains to your Heroku instance.

Make sure you connect your Heroku app to your GitHub and enable automatic deploys. Will make things easier. :) 

#### Freenom/Domain Steps
For beginners, Freenom is a good provider for obtaining domains for free. However the catch is that you can only use properly "Freenom" domains for free being .cf, .ml, .gq, ga and .tk. However these can be blocked rather easily.

- Get some Freenom domains then add them to your Heroku instance (Personal > [App Name] > Settings > Domains)
Add a domain for both `www.youdomainhere.cf` and `yourdomainhere.cf` with .cf being interchangeable with other Freedom domain names.
- If you prefer to obtain premium domains (TLDs) then use <a href="https://porkbun.com">Porkbun</a>, which offers domains for amazing prices. Literally a `.net` domain normally costs around $10. On Porkbun for the first year it costs $3 so its definitely a deal.

#### Cloudflare Steps
- Use Cloudflare (make an account), add your site (Freenom Domain or Domain) and then add your various DNS targets to Cloudflare. Make sure you add Cloudflare's Nameservers which will be specified more when you are adding your site. 

Make sure they are CNAME although A records also work and try to follow this structure:

**Type | Name | Target**

`CNAME | www | yourherokutargethere.herokudns.com `
`CNAME | @ | yourherokudnstargethere.herokudns.com`

**Below are if you want external proxies also with your site:**

`CNAME | a | yournodeinstance.herokudns.com`
`CNAME | pd | yourpydodgebinstancehere.herokudns.com`
`CNAME | p | yourpowermouseinstancehere.herokudns.com`

Make sure HTTPS is forced and have SSL set to Flexible for Heroku. Otherwise you can have SSL set to Full.

#### Workspace Configurations 
Preferably if you have your own device use Visual Studio Code. Pretty much the best option you can get but obviously this is an opinion. Also make sure you have <a href="https://nodejs.org/">Node.JS</a> installed on your machine.

Not going to go too in depth with this part but first fork this repository. The clone it locally through a Terminal of some sort depending on what OS you are on. Make sure you navigate to the folder you want to set this up in.

```
git clone https://github.com/QuiteAFancyEmerald/HolyUnblockerPublic.git

cd HolyUnblockerPublic

npm install
```

Now simply add the folder you cloned this repo in in VSC. Then run `npm install`. I recommend that if you are releasing this publically on GitHub that you add a `.gitignore` in your root directory with the following exclusions:

`node_modules`

Now you have your following workspace environment setup. To deploy the following workspace you just created you will need to look up depending on your hosting provider.

For an online IDE that you can use on your school computer and/or chromebook use GitPod. Basically the equivalent of Visual Studio Code but with in-browser support.
- Make an account: `https://gitpod.io/`
- Fork this repo and enter in this URL to setup your workspace: `https://gitpod.io#https://github.com/YourNameHere/HolyUnblockerPublic/`

Use the same steps above by running `npm install` in your repository and adding a `.gitignore` in your root directory specifying to exclude `node_modules`.

## More Information
This project uses Alloy Proxy, Node Unblocker, Powermouse and PyDodge which are linked below. Credits also given to Titanium Network and all it's developers as this project would not be possible without them. View the official website for more detail. :)

- https://github.com/titaniumnetwork-dev/
- https://github.com/titaniumnetwork-dev/alloyproxy
- https://github.com/nfriedly/node-unblocker
- https://github.com/vibedivide/powermouse
- https://github.com/BinBashBanana/PyDodge
- https://github.com/juchi/gameboy.js
- https://nodeclusters.com
- https://titaniumnetwork.org/
- https://github.com/vibedivide/vibeOS

Thanks.
