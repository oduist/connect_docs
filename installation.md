# Installation

## Installation to-do list <a href="#table_of_content_heading_1734011658553_4" id="table_of_content_heading_1734011658553_4"></a>

* Download the latest modules in one package from our [Download](https://oduist.com/download) page.
* Unpack the archive into your Odoo addons folder.
* Install the dependencies from the included requirements.txt file.
* Install the required modules into Odoo.&#x20;
* Enter your company details and create the subscription.
* Copy Twilio API auth and key from your Twilio [console](https://console.twilio.com/) (yes, you must have a Twilio account).
* Synchronize Twilio numbers and other data (if any) with Odoo Connect.

## Odoo 18.0 installation <a href="#table_of_content_heading_1734011658554_6" id="table_of_content_heading_1734011658554_6"></a>

This is related to official Odoo 18.0 docker setup. Here is how to build a custom image for Twilidoo:

<pre class="language-bash"><code class="lang-bash"><strong>Dockerfile:
</strong>FROM odoo:18.0
USER root
RUN apt update &#x26;&#x26; apt install -y python3-openai &#x26;&#x26; pip3 install --break-system-packages twilio elevenlabs
USER odoo
</code></pre>
