---
{"dg-publish":true,"permalink":"/netlify-with-go-daddy-domain-name/","created":"","updated":""}
---

#project/learn-by-doing 
#source/dupe/begin 
- [src](https://levelup.gitconnected.com/netlify-custom-domains-8b4cc5fddb5d)
## Netlify: Custom Domains with GoDaddy
If you have deployed your app on Netlify but would prefer to use a domain you purchased on GoDaddy, this is the blog for you.

This guide will walk you through the necessary steps to use your custom GoDaddy domain while continuing to use Netlify and all of its useful deployment features.

**Prework**

This blog assumes that you have already created a Netlify account and purchased a GoDaddy domain. If you have not done so, you can Sign-up/purchase here ([Netlify](https://app.netlify.com/signup?_ga=2.39371296.2083118729.1605908234-1975371472.1597791247) & [GoDaddy](https://www.godaddy.com/)).

**[Please note that Netlify now allows users to purchase domains direct](https://www.netlify.com/blog/2018/06/19/buy-and-secure-a-custom-domain-through-netlify/)**

For a tutorial on how to deploy a GitHub Repository to Netlify, please see my blog posted [here](https://medium.com/swlh/launching-your-first-website-rails-react-42a6af1ab481).

**Netlify: Getting Started**

To get started, we first want to identify our default subdomain. We will need to provide GoDaddy with this information later on. To find the default subdomain click on the Domain settings button in the Site overview tab of your Netlify Site.

![](https://miro.medium.com/v2/resize:fit:1400/1*76u73eMuPtCMEPGC5Z7N9w.png)

Site Overview Tab Netlify

Your default subdomain will be the first item in the Custom domains section.

![](https://miro.medium.com/v2/resize:fit:1222/1*OzjF8OZEubOAGEA_Q-SQbA.png)

Default Subdomain from Netlify

**GoDaddy: DNS Management**

Login to your GoDaddy account and select All Domains from the Domains dropdown.

![](https://miro.medium.com/v2/resize:fit:1110/1*OOXZOQTkMWoYyjmAb0NAZg.png)

GoDaddy Landing Page

Click on the custom domain you would like to use for your Netlify Site.

![](https://miro.medium.com/v2/resize:fit:1400/1*Fiz04PvDfGdIFsNnqNf0_Q.png)

List of Domains from GoDaddy

Scroll down to additional settings and click on Manage DNS. This will populate the custom domains Records.

![](https://miro.medium.com/v2/resize:fit:1400/1*cCN_Z6cQcfvgUuwuNA-HLg.png)

The records should be pre-populated with all the required fields you need. The only two fields that you need to update are the value fields for Type A and CName. Type A is the IP Address for the Netlify servers and will be the same for all domains and users, 104.198.14.52. The CName is the Netlify default subdomain we identified earlier. Updating this field allows GoDaddy to send the custom domain to the correct Netlify subdomain.

![](https://miro.medium.com/v2/resize:fit:1400/1*CGdFN3eBnk3r9N0J5MiIMA.png)

GoDaddy DNS Management Records

**Netlify: Custom Domain Verification**

Now back in Netlify, we are able to add our custom domain. Click on the Add custom domain button.

![](https://miro.medium.com/v2/resize:fit:1226/1*WC65IMIJ5Ltj0AYALq7qHg.png)

Add Custom Domain

Next, type in your custom domain, starting with “www.” and click verify.

![](https://miro.medium.com/v2/resize:fit:1050/1*iZmMJ6dspX-fK8MTvOVm2A.png)

If your verification is successful, you should see something similar to what is shown below. Your custom domains should include a default subdomain, primary domain (i.e., [www.matthewsedlacek.com](https://www.matthewsedlacek.com/)), and redirect for when users don’t type www (i.e., [matthewsedlacek.com](https://matthewsedlacek.com/)).

![](https://miro.medium.com/v2/resize:fit:1220/1*tuvCnfq8hfhRRls0vPWZ2w.png)

Now it’s time to celebrate; you can now share your custom domain with the world!

**Resources**

TopTechNow. “How to connect Netlify to Godaddy (Custom Domain).”_YouTube_, uploaded by TopTechNow, 18 January 2018, [https://www.youtube.com/watch?v=qbChXHDAK4s](https://www.youtube.com/watch?v=qbChXHDAK4s).

#source/dupe/end 