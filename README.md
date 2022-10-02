# Steps-to-bruteforcing-remote-Crypto-miner
Only take three steps(on Kali System) :)

<b>If you don't have the Kali system as a virtual machine on your PC. You will need to download and install one. The most proficient way for me is to install Kali on VMware Fusion since it's free for a preview version.</b>

<b>1.</b>Sign up and sign in shodan.io https://www.shodan.io and type <i><b>antminer port:80</b></i> into the search bar. 

You will see something like this:
[![m1.jpg](https://i.postimg.cc/NjJMTT01/m1.jpg)](https://postimg.cc/w1NgY1Lv)

You may want to add more filters to the query such as <i><b>country:US</b></i> or <i><b>city:Paris</b></i>

<b>2.</b>Download customized wordlist as a dictionary for later brute-forcing attack from the link, famously known as RockYou2021(<i>appro 90GB large, so prepare enough spaces beforehand</i>). The link is here: https://github.com/ohmybahgosh/RockYou2021.txt

If you don't have enough spaces on your disks, you may want to download the resources below as a mini-version or do brute-forcing later on 

- https://crackstation.net/crackstation-wordlist-password-cracking-dictionary.htm
- https://www.hack3r.com/forum-topic/wikipedia-wordlist
- https://github.com/danielmiessler/SecLists/tree/master/Passwords
- https://github.com/berzerk0/Probable-Wordlists
- https://weakpass.com/download

<b>3.</b>Select remote antminer with title of 401 unauthorized(most of them are by default). Since those miners mostly use "root" as their username, we can then use <b>hydra</b>(assuming that you have installed the tool on your Kali system) with one line code to implement brute-forcing to the miner we just chose.

For example, the code can be like this:

<b>hydra -l root -P commonPasswords.txt -vV {TARGET} http-get /</b>

- First of all, you may want to replace "{TARGET}" with the IP address and the port number such as:<b>123.123.123.123:80</b> 
- Here, "root" is the default username of the crypto miner we chose(You may want to change it according to the miner that you choose)
- Also, "commonPasswords.txt" is the dictionary file name, so you may want to replace it with your dictionary file name.

Then execute the command and wait for a miracle(since people are more concerned about web security nowadays).

Results:
If lucky enough, you will see the page below: 

[![m2.jpg](https://i.postimg.cc/5Ns8tX8C/m2.jpg)](https://postimg.cc/ppnmGXGW)

Then just simply edit on the site as your wish. 

Otherwise, you may want to try other dictionary files for another brute-force attack or try to break it using other methods according to its vulnerabilities.

<b>Done and done~!</b>

<h3>Attention:</h3>
<b>This article only shows a simple way for implementing a basic brute-forcing attack to remote servers and I will not be responsible for people who use knowledge from this article for any illegal purposes</b>

