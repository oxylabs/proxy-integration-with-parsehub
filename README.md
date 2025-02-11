# Proxy Integration With ParseHub

[![Oxylabs promo code](https://raw.githubusercontent.com/oxylabs/product-integrations/refs/heads/master/Affiliate-Universal-1090x275.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112) 

- [How to integrate Oxylabs’ proxies with ParseHub](how-to-integrate-oxylabs-proxies-with-parseHub)
    - [Residential Proxies](residential-proxies)
    - [Enterprise Dedicated Datacenter Proxies](enterprise-dedicated-datacenter-proxies)
    - [Self-Service Dedicated Datacenter Proxies](self-service-dedicated-datacenter-proxies)
    - [Shared Datacenter Proxies](shared-datacenter-proxies)
 - [Adding custom proxies to your Parsehub account](adding-custom-proxies-to-your-parsehub-account)
   
[ParseHub](https://www.parsehub.com/) is a convenient low-cost tool for scraping public data from websites. It allows users to extract information to easy-to-read spreadsheets or APIs. In this guide, we'll demonstrate how to integrate ParseHub with Oxylabs proxies and get the best out of this tool. 

## How to integrate Oxylabs’ proxies with ParseHub

Settings configuration in ParseHub is a pretty straightforward process. Before getting started, visit Oxylabs [dashboard](https://dashboard.oxylabs.io/en/) and add [your IP address](https://whatismyipaddress.com/) to the whitelist under [Residential Proxies](https://oxylabs.io/products/residential-proxy-pool) > Whitelist. If you haven’t created your user yet, do that in the Residential Proxies > Users section as well. You may need your user credentials for authentication in ParseHub later on. 

For [Datacenter Proxies](https://oxylabs.io/products/datacenter-proxies) you should note that the port may be changing due to various reasons, such as Proxy Rotator,  SOCKS connection, using Proxies via whitelist etc. therefore see our Datacenter Proxy documentation for more information. Then, follow the steps below: 

1. [Download ParseHub](https://www.parsehub.com/quickstart) and install it on your computer.

2. Launch ParseHub.

3. Create a new project from your home screen by clicking on the “+ New Project” button.

4. **Insert a URL** from which you would like to scrape public data from. In this example, we’ll use oxylabs.io. Then, press **“Start project on this URL”**.

5. Wait for the  project to be ready and switch to the **“Browse”** mode.

6. Once the **“Browse”** slider **is green**, open the drop-down list on the top-right side and click on **“Preferences”**.

7. Select **“Advanced”**, click on the “Network” tab, and choose “Settings”.

8. Select **“Manual proxy configuration”**. Insert the given details below, for specific proxy type configuration.

### Residential Proxies

**Proxy type**: `HTTP`, `HTTPS`, or `SOCKS5`

**IP/Host**: `pr.oxylabs.io`

**Port**: `7777` 

You can also use country-specific entries. For example, entering ie-pr.oxylabs.io under **IP/Host** and `25000` under **Port** will acquire an Irish exit node. Please refer to our [documentation](https://developers.oxylabs.io/proxies/residential-proxies/country-specific-entry-nodes) for a complete list of country-specific entry nodes or if you need a [sticky session](https://developers.oxylabs.io/proxies/residential-proxies/session-control/sticky-proxy-entry-nodes).

8.1. Above is an example of how Residential Proxies can be integrated. For Datacenter proxies, there is only a minor change.

### Enterprise Dedicated Datacenter Proxies

Specify the following if you purchased [Dedicated Datacenter Proxies](https://oxylabs.io/products/datacenter-proxies/dedicated-datacenter-proxies) via sales.

**Proxy type**: `HTTP` or `SOCKS5`

**IP/Host**: a specific IP address (e.g., `1.2.3.4`)

**Port**: `60000`

For Enterprise Dedicated Datacenter Proxies, you’ll have to choose an IP address from the acquired list. Visit our [documentation](https://developers.oxylabs.io/proxies/dedicated-datacenter-proxies/enterprise/proxy-lists) for more details.

### Self-Service Dedicated Datacenter Proxies

Specify the following if you purchased [Dedicated Datacenter Proxies](https://oxylabs.io/products/datacenter-proxies/dedicated-datacenter-proxies) via the dashboard.

**Proxy type**: `HTTP` or `HTTPS`

**IP/Host**: `ddc.oxylabs.io`

**Port**: `8001`

For Self-Service Dedicated Datacenter Proxies, the port indicates the sequential number of an IP address from the acquired list. Check our [documentation](https://developers.oxylabs.io/proxies/dedicated-datacenter-proxies/self-service/proxy-list) for more details.

### Shared Datacenter Proxies

Here are the details for the [Shared Datacenter Proxies](https://oxylabs.io/products/datacenter-proxies/shared): 

**Proxy type**: `HTTP`

**IP/Host**: `dc.pr.oxylabs.io`

**Port**: `10000`

You can also use a country-specific entry. For example, entering dc.ca-pr.oxylabs.io under **IP/Host** and `34000` under **Port** will acquire a Canadian exit node. Please refer to our [documentation](https://developers.oxylabs.io/proxies/shared-datacenter-proxies/select-country) for a complete list of country-specific entry nodes.

If you’re using a Proxy Rotator, put `clientname.oxylabs.io` in the `HTTP` Proxy field and `60000` in the **Port field**. Click **OK** to save the settings.

9. Afterwards, open both a new tab and any website, where you’ll get a message like this (the photo is taken from [Parsehub](https://help.parsehub.com/hc/en-us/articles/115001324853-Adding-Custom-Proxies-to-ParseHub-for-all-Paid-Plans), your exact details will be different.)

## Adding custom proxies to your Parsehub account

1. Once you’ve started your project, go to the settings button at the top and click on it.

2. After seeing the Settings menu pop up, you’ll notice a checkbox right next to the “Rotate IP address” text. Note that this premium Parsehub feature will require you to choose a paid plan.

Further below, the “Custom Proxies” textbox will be present. There you should paste your proxy with the realm which was obtained earlier in the tutorial (the custom proxy provided here is merely an example taken from Parsehub, yours will be different.) 

If you have multiple custom proxies you wish to rotate, all of them can be added to the Custom Proxies field on a new line.

3.After setting these proxies up on your account, you can save and run the project.

That’s it! You’ve successfully integrated Oxylabs Residential or Datacenter Proxies with ParseHub. To make sure it’s working properly, check your IP address on a database such as whatismyipaddress.com. 

To access a full tutorial with images, please click [here](https://oxylabs.io/blog/proxy-integration-with-parsehub). 
