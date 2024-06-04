# Pseudovote-CDOC

![Creating pseudonyms for all ~1 million voters in Estonia](ima_e73c52f_e.jpeg)

On clean [Ubuntu 24.04](https://releases.ubuntu.com/noble/) you need:

```
sudo apt install python3-m2crypto python3-pyasn1 python3-pycryptodome python3-progressbar python3-fpdf
```

During the ceremony following commands might be of use:

```
ls -1 con | wc -l
rm -r con && mkdir con
sha256sum voterlist.txt
du -h con
```

Create one pseudonym for each voter in voterlist:

* Simple Python code for generating pseudonyms
* Encrypt each pseudonym for a dedicated voter
* Export encrypted pseudonyms for delivery
* Provide instructions to participating in a poll
* Do not store connection between voterlist and pseudonyms
* Prove it as well as possible during the ceremony
* Blackbox list of pseudonyms until the end of election

Similar to [Uduloor](https://github.com/infoaed/uduloor) and process described in a [write-up](https://gafgaf.infoaed.ee/en/posts/pseudonymous-voting-in-wikimedia/).
