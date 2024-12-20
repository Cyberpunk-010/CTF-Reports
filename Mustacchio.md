#cat-pictures-2

## Recon

#### Nmap Scan


```bash

┌──(kali㉿kali)-[~]
└─$ nmap -sV -sC mustacchio.thm
Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-12-20 11:03 EST
Nmap scan report for mustacchio.thm (10.10.219.22)
Host is up (0.24s latency).
Not shown: 998 filtered tcp ports (no-response)
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 7.2p2 Ubuntu 4ubuntu2.10 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 58:1b:0c:0f:fa:cf:05:be:4c:c0:7a:f1:f1:88:61:1c (RSA)
|   256 3c:fc:e8:a3:7e:03:9a:30:2c:77:e0:0a:1c:e4:52:e6 (ECDSA)
|_  256 9d:59:c6:c7:79:c5:54:c4:1d:aa:e4:d1:84:71:01:92 (ED25519)
80/tcp open  http    Apache httpd 2.4.18 ((Ubuntu))
| http-robots.txt: 1 disallowed entry 
|_/
|_http-server-header: Apache/2.4.18 (Ubuntu)
|_http-title: Mustacchio | Home
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 33.51 seconds
```



```C++
#include <iostream>
using namespace std;

bool isLeapYear(int year) {
    if (year % 4 == 0) {
        if (year % 100 == 0) {
            if (year % 400 == 0)
                return true; // Divisible by 400
            else
                return false; // Divisible by 100 but not 400
        } else {
            return true; // Divisible by 4 but not 100
        }
    } else {
        return false; // Not divisible by 4
    }
}

int main() {
    int year;
    cout << "Enter a year: ";
    cin >> year;

    if (isLeapYear(year))
        cout << year << " is a leap year." << endl;
    else
        cout << year << " is not a leap year." << endl;

    return 0;
}

```