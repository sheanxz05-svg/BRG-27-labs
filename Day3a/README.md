# Day 3a

## DNS Configuration and Testing

### Objective

The aim of this lab was to learn how DNS works by connecting a domain name to a 
server IP address and checking whether the DNS records were working properly.

### What I Did

First, I logged into AWS and found the Public IPv4 address of my EC2 Ubuntu instance.

Next, I created a free domain using DuckDNS. 
I chose the domain name:

shahnazlab.duckdns.org

After creating the domain, I updated the IP address in DuckDNS so that it pointed to my AWS server.

I then used commands such as:

nslookup shahnazlab.duckdns.org

and

ping shahnazlab.duckdns.org

to check if the domain was resolving to the correct IP address.

### What I Learned

From this activity, I learned that DNS is responsible for translating domain names into IP addresses. 
I also learned that tools like ping and nslookup are useful for checking if a domain is working correctly.

---

## Digital Certificates 

I also attempted to configure HTTPS using Let's Encrypt and Certbot.

I installed Certbot and ran:

sudo certbot --apache

However, I later realised that I was running Ubuntu on UTM instead of AWS EC2. Since UTM is only a local virtual machine and does not have a public IP address, Let's Encrypt could not verify the domain and generate the certificate successfully.

Although I was not able to complete the HTTPS setup, I learned that SSL certificates require the server to be publicly accessible so that the domain can be verified.

### Conclusion

Overall, this lab helped me understand how DNS, domain names and SSL certificates work together. Even though I faced some difficulties, I gained a better understanding of networking concepts and cloud services.
