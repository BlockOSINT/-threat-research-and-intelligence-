

**Hangro: Investigating North Korean VPN Infrastructure Part 1**

- Article: https://nkinternet.wordpress.com/2025/01/06/hangro-north-korean-vpn-infrastructure/

[January 6, 2025]

In a post from a now-deleted user on the webdev subreddit, someone asked
about how to acquire a .kp TLD. While there were a few decent responses,
the original poster shared an update: they successfully obtained a
domain but noted that a VPN is required to access the website. This
raised intriguing questions about VPN usage in North Korea.

While several VPN providers claim to operate from North Korea, most
merely offer false IP geolocation. However, the poster provided the
domain they acquired: hani.star-co.net.kp. This sparked an investigation
into what might be a legitimate North Korean VPN infrastructure.

![image](https://github.com/user-attachments/assets/65500df2-0018-459f-bac0-74124c80c4f2)


**Is Hangro a VPN?**

North Korea's tightly controlled internet environment relies on specific
tools for access. One such tool is the software NetKey, which
authenticates users inside the country for internet access. However, it
appears there is another program, Hangro, which may potentially function
as a VPN for users outside the country. Let's dig into the
infrastructure a little more

**Hangro's IP Infrastructure**

Historically, four IP addresses supported Hangro's operations. These
included two IPs located in North Korea and two in Russia. These IPs
shared certificates on port 3225 and also had port 8888 open:

-   175.45.176.21

-   175.45.176.22

-   188.43.136.115

-   188.43.136.116

Until November 1, 2024, these IPs displayed the following certificate
information on port 3225:

-   **Subject:** CN=hangro.net.kp

-   **Issuer:** CN=hrra2024

-   **Names:** hangro.net.kp

Additionally, the IP 175.45.176.32 matched this certificate data.

Despite these technical similarities, the exact purpose of these IPs
remains unclear. Further investigation of the domain hangro.kp on
archive.org reveals a 2012 snapshot of a remote access page written in
Korean:

![image](https://github.com/user-attachments/assets/f8aea8c5-fdc6-4751-bff5-b74eaf87df1e)

Screenshot of hangro.net from 2012. https://web.archive.org/web/20121231174908/http://www.hangro.net:80/user/login.php


This domain was apparently used for some kind of remote access and is
similar to a current North Korean TLD but there's still more that can be
investigated to tie this to North Korea as well as how it is used for
remote access.

**Whois Records and DPRK Connections**

Luckily whois data from that time reveals who had registred hangro.net:

-   **Registrar:** XIN NET TECHNOLOGY CORPORATION

-   **Registrant:** Jo Myong Chol

-   **Address:** "District Heping, Road Wenhua, No 17 4-24-1,"
    Shenyangshi, Liaoningsheng, China

-   **Email:** support@silibank.com

Jo Myong Chol is listed as a North Korean national
in [OpenSanctions](https://www.opensanctions.org/entities/kprusi-4c49409814e25106a43399be9a7c23b2647d8829/).
The email address support@silibank.com was also used to register other
DPRK-affiliated websites, including:

-   ournation-school.com

-   uriminzogkiri.com

This strongly ties Hangro's infrastructure to North Korea. The use of
silibank.com---a domain associated with other DPRK-related
websites---suggests a coordinated effort to manage internet resources
and infrastructure tied to state activities. Furthermore, the Shenyang
address and registrant details align with known patterns of North Korean
operations abroad, further solidifying its connection to the regime's
broader internet strategy.

**Silibank and Hangro Software**

At this point we can conclude that all of this is related to North Korea
but it still doesn't answer the question about what hangro.net.kp is
used for. However, back in 2014 archive.org also captured the following
page for silibank.com

![image](https://github.com/user-attachments/assets/a3a543e6-34eb-48c8-89c6-add2a4350554)

https://web.archive.org/web/20141218100818/http://silibank.com/

While archive.org doesn't have a copy of the files, VirusTotal provides
us a list of files in the fog directory

![image](https://github.com/user-attachments/assets/ecef783d-c129-49bc-b1f5-7c160113cddb)

Side note if anyone knows what moranbong is or has a copy of the files feel free to reach out.

**What is Hangro Used For?**

Judging by the name it's probably a VPN client that was downloaded from
silibank.com. While the file on VirusTotal may be an older file I was
able to find what I think is a newer version of Hangro. The interesting
thing is that it came with a default config in place that is designed to
connect back to 218.25.43.212 on port 8888

![image](https://github.com/user-attachments/assets/7438a6a7-ecfe-49f8-afee-c564f822ebd7)


Pulling some additional details for that IP reveals an abuse contact
email of postmaster@silibank.com

![image](https://github.com/user-attachments/assets/32b71be8-8ff7-4a9f-88d6-c2a96344aa75)


What does this all mean? It seems to be some infrastructure used for
possibly connecting back to the Kwangmyong potentially. There's not a
lot of information available online about the Hangro software. So far
the only thing that I've been able to find is this article from rfa.org
that claims the following:

"The newly developed computer startup program detects the internet
connection status in real time and opens a channel to use only North
Korean e-mail. You can download instructions from Pyongyang, and access
lecture materials and study materials only through North Korean e-mail,"
the second source said.

"The software, called 'Hangro,' disables external emails from China and
the rest of the world. It has become the only email channel where
messages can be exchanged between the North Korean authorities and the
company," said the second source.

"North Korean trading companies must pay \$350 to the Shenyang consulate
to use Hangro," the second source said.

<https://www.rfa.org/english/news/korea/smartphone_surveillance-09202022164642.html>

**Looking Ahead: Part 2 Preview**

While the article mentions it is used for just email, some brief
investigation of the software reveals that there may be more to it. Part
2 of this series will have additional details about the software.
Further, it appears that North Korea is using infrastructure outside of
it's typical ASN. Doing some quick digging into the 188 addresses shows
the following ranges in the RIPE database as being related to the 188 IP
addresses.

![image](https://github.com/user-attachments/assets/32664aa0-a964-46cc-ae3a-db5609b4297e)
}

Indicators mentioned in this post are below. If you have any additional
details about Hangro please reach out <contact@dprkinternetwatch.com>

**Indicators:**

-   175.45.176.21

-   175.45.176.22

-   175.45.176.32

-   188.43.136.115

-   188.43.136.116

-   218.25.43.212

-   hangro.net.kp

-   hangro.net

-   silibank.com

-   ournation-school.com

-   uriminzogkiri.com

-   support@silibank.com

-   postmaster@silibank.com
