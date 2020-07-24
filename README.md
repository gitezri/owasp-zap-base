# owasp-zap-base
OWASP-ZAP is a great way to quickly run a baseline of your production website.
This systems app allows you to see the basic issues with your web app.
The goal is for you to find your sites problems before hackers find them.

## Vulnerability Assessment  
The NIST definition "Systematic examination of an information system or product to determine the adequacy of security and privacy measures, identify security and privacy deficiencies, provide data from which to predict the effectiveness of proposed security and privacy measures, and confirm the adequacy of such measures after implementation"[1](https://csrc.nist.gov/glossary/term/vulnerability_assessment).

## OWASP-ZAP is Open Source Wep Application Project / Zed Attack Protocol. 
It allows companies to comply the federal and state requirement of
Vulnerability Assessment. 

It is possble to run ZAP inside a container, but you will get better support running it directly via Zap.sh.

## Case study:

ZAP is a massive project but here is a basic command line example of how to run it. You can also run it in GUI mode but this way it can be fully automated.

/usr/share/zaproxy/zap.sh -cmd -quickurl www.xvwa.com -quickprogress

I've tested it under Ubuntu, Kali and Rasbian Linux and under AWS. It is available under Windows and Mac.

## The "Zap.sh" command allows you to quickly run baseline of your companies web applications.

I needed a vulnerable site to test it (a docker containter was perfect for this):  

## docker run --name xvwa -d -p 80:80 tuxotron/xvwa

Here is the page for xvwa [XVWA GitHub](https://github.com/tuxotron/xvwa_lamp_container)

This command pulls and runs the XVWA web application.

Make this real, I edited the /etc/hosts file to point the web app to a normal web address:

172.17.0.2 www.xvwa.com xvwa. 

This way it resolves to my locally created web application. Remember it is illegal to access
private data without a written consent. That's way we are hacking our own web site.

## References

Must [Install OWASP ZAP] (https://www.zaproxy.org/download/)

Very handy [Command line Help] (https://www.zaproxy.org/docs/desktop/cmdline/)

Youtube introduction to Zap.sh [Info on Zap API](https://youtu.be/3vVnMh6AUkk)

Detailed API documentation [ZAP API] (https://www.zaproxy.org/docs/api/#introduction)

ZAP Docker User's Guide (https://www.zaproxy.org/docs/docker/about/)

## Notes

Similar project ZAPR is not being maintained
