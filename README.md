# owasp-zap-base
OWASP-ZAP is a great way to quickly run a baseline of your production website.
This systems app allows you to see the basic issues with your web app.
The goal is for you to find your sites problems before the hackers find them.

## Vulnerability Assessment  
Systematic examination of an information system or product to determine the adequacy of security and privacy measures, identify security and privacy deficiencies, provide data from which to predict the effectiveness of proposed security and privacy measures, and confirm the adequacy of such measures after implementation[1](https://csrc.nist.gov/glossary/term/vulnerability_assessment).

## OWASP-ZAP is Open Source Wep Application Project / Zed Attack Protocol. 
It allows companies to comply the federal and state requirement of
Vulnerability Assessment. 

It is possble to run ZAP inside a container, but you get better support running it directoy via Zap.sh.

## Case study:

ZAP is a massive project but this is a basic command line example of how to run it. You can also run it GUI but this way can be fully automated.

/usr/share/zaproxy/zap.sh -cmd -quickurl www.xvwa.com -quickprogress

I've tested it under Ubuntu, Kali and Rasbian Linux. It is available under Windows and Mac.

## The "Zap.sh" command allows you to quickly run baseline of you companies web applications.

I need an vulnerable site to test it (a docker containter was perfect for this):  

## docker run --name xvwa -d -p 80:80 tuxotron/xvwa

Here is the [GitHub] page for xvwa (https://github.com/tuxotron/xvwa_lamp_container)

This command pulls and runs the XVWA web application.

Make this real, I edited the /etc/hosts file to point the web app to a normal web address:

172.17.0.2 www.xvwa.com xvwa. 

This way the resolves to my locally create web application. Remember it is illegal to access
privately data with out a written consent. That's is way we are hacking or testing ourself.

## References

Must [Install OWASP ZAP] (https://www.zaproxy.org/download/)

Very handy [Command line Help] (https://www.zaproxy.org/docs/desktop/cmdline/)

Youtube introduction to Zap.sh [Info on Zap API](https://youtu.be/3vVnMh6AUkk)

Detailed API documentation [ZAP API] (https://www.zaproxy.org/docs/api/#introduction)

ZAP Docker User's Guide (https://www.zaproxy.org/docs/docker/about/)

## Notes

Similar project ZAPR is not being maintained
