---
node_id: 5018
title: Rackconnect v2.0 - FAQ
type: article
created_date: '2015-12-10'
created_by: Rackspace Support
last_modified_date: '2016-01-19'
last_modified_by: Stephanie Fillmon
product: RackConnect
body_format: markdown_w_tinymce
---

<p><strong>Applies to:</strong> RackConnect v2.0. For questions on RackConnect v3.0, see <a href="/how-to/rackconnect-v30-faq">RackConnect 3.0 - FAQ</a>.</p>

<h2>Getting Started</h2>

<h3>How do I get RackConnect?</h3>

<p>Customers with a dedicated account should speak to their Account Manager for information about the actions involved in getting RackConnect, and how best to proceed. Be aware that RackConnect is supported only where Rackspace Cloud infrastructure exists. At this time, the Rackspace Cloud is available from our Chicago, Dallas, Virginia, Sydney, Hong Kong, and London data centers.</p>

<p>If you are an existing Cloud customer, you will need to speak to a member of our Sales team. They can guide you through the process of acquiring a device that may be used in a RackConnected environment.</p>

<h3>What can RackConnect do for me?</h3>

<p>You need RackConnect in order to build a hybrid hosting solution that combines the best of dedicated and cloud hosting by creating connections between dedicated servers and Cloud Servers. RackConnect can be implemented on certain Cisco ASA series FIREWALLS, or an F5 BIG-IP load balancer that is used to interconnect dedicated physical servers with cloud-based servers on the Rackspace internal network known as ServiceNet.</span></p>

<h3>Where do I go for help with RackConnect</h3>

<p>If you need help with RackConnect please contact us via any of our usual Support channels, and our team will help you with your issue or direct you on to the relevant support group. We are available via phone, chat, or tickets 24x7x365.</p>

<p>If you believe your issue is Cloud Server specific, please raise the appropriate query with the Cloud team via the Cloud Control Panel, otherwise please raise other requests via the my.rackspace.com portal.</p>

---------
<h2>Account Services</h2>

<h3>I already have a cloud account, can I connect to my exisiting servers?</h3>

<p>You may RackConnect an existing Cloud account, but any existing servers will not be RackConnected. If existing servers need to be RackConnected, they will need to be rebuilt after the RackConnect implementation has been completed. This may be done by first saving a Cloud Server image, and then using the image to rebuild the existing server a a new RackConnected server - or to simply build a new server.</p>

<p>Please be aware that this process for RackConnecting an existing server will result in a new IP being assigned to the server. Since you are essentially creating a new server, unfortunately this cannot be avoided.</p>

<p>An important consideration to take into account is the region you will use to provision your servers. Because RackConnect relies on a service net connection to link your dedicated servers and your cloud servers, you will need to provision your RackConnected servers in the same geographic region as your dedicated servers. Your saved server images will only be available for creating servers in the same region as the original server.</p>

<h3>Which cloud account do I need for Rackconnect?</h3>

<p>RackConnect may be used with both Managed Operations Service Level and Managed Infrastructure accounts.</p>

<p>Be aware that the usual service-level limitations still apply for RackConnect Cloud accounts, and you should use the appropriate account type for the implementation based on your support requirements. It is possible to use RackConnect with more than one cloud account, so you can have a mix of both if you prefer.</p>

<h3>I have Rackconnect v2.0, how can I build unconnected Cloud Servers?</h3>

<p>During normal circumstances, if your Cloud account has been enabled with RackConnect v2.0, your Cloud account is linked to your dedicated hosting account and your dedicated servers will be able to communicate using the service net with your Cloud Servers in the same region. If you wish to provision Cloud Servers that are <strong>not</strong> linked to your dedicated Rackspace Hosting account, there are a couple of ways you can work around this condition.</p>

<p>1) You can provision Cloud Servers in a region other than the one where your dedicated servers are located. For example, if your dedicated servers are in the DFW region, and your linked Cloud Servers are also in the the DFW region, any Cloud Servers you provision in ORD or IAD will not be linked to your dedicated servers and should function independently.</p>

<p>2) You can also sign up for a second Cloud account. The drawback of doing this is that you will not be able to access any custom server images between accounts.</p>

<h3>How am I charged for bandwidth usage?</h3>

<p>For Cloud Servers that are a part of your RackConnect configuration, all&nbsp;network traffic will leave via the dedicated firewall device. The traffic between the Cloud Servers and the RackConnect device travels over the internal, unmetered Cloud ServiceNet. Any traffic between the Cloud Servers and dedicated networks will similarly be unmetered and not incur bandwidth charges.</p>

<p>The bandwidth usage costs for Internet related traffic entering and leaving the RackConnect device is charged using Dedicated Hosting bandwidth pricing plans. Our Sales representatives will discuss this in more detail with you when you inquire about RackConnect.</p>

---------
<h2>Security</h2>

<h3>What are "Network Policies"?</h3>

<p>RackConnect Network Policies are the equivalent of firewall rules that are applied via the RackConnect web interface. These policies are then applied to the firewall device and any Cloud Servers referenced.</p>

<p>The Network Policies are a useful means of centralising all your firewall rules for the RackConnect device, any dedicated networks and any RackConnected Cloud servers.</p>

---------
<h2>Monitoring and troubleshooting</h2>

<h3>My Cloud Servers have no network connectivity, what's wrong?</h3>

<p>Please check the current RackConnect Network Policies in place to ensure that the relevant access rules will permit the required connectivity. For example creating an Internet-to-Cloud rule to permit traffic originating from the Internet to reach your Cloud Servers.</p>

<p>If adjusting the Network Policies does not resolve the issue, please contact Support via phone, chat, or ticket so that we can help investigate this further with you.</p>

---------
<h2>Databases</h2>

<h3>Can Cloud Databases be used with Rackconnect?</h3>

<p>Yes, RackConnect cloud servers can be used to connect to Cloud Databases, but dedicated servers in a RackConnect configuration will not be able to connect to Cloud Databases.</p>

---------
<h2>Network</h2>

<h3>Can I use RackConnect across different data centers?</h3>

<p>No. Because RackConnect is intended to interconnect devices on a local network, any involved servers need to be within the same data center.</p>

<p>If you have existing dedicated hardware, ensure that your Cloud account is provisioned to build your Cloud Servers in the same data center. Contact our Cloud support team for help with this. Rackspace has cloud infrastructure in Chicago, Dallas, and Virginia in the US, and global cloud infrastructure in London, Sydney, and Hong Kong.</p>

<h3>I need VPN connectivity to my Cloud Servers. Can RackConnect help?</h3>

<p>Yes, because RackConnect is a dedicated firewall, it is possible to terminate a site-to-site VPN on the device, or to use a client-based VPN. This enables secure VPN communication between your office or home into the cloud environment.</p>

---------
<h2>General</h2>

<h3>Where can I find answers to questions about RackConnect v3.0?</h3>

<p>See the <a href="/how-to/rackconnect-v30-faq">RackConnect v3.0 FAQ</a>, for question and answer items specific to this new version.</p>

<h3>Does RackConnect enhance my ability to connect to my Cloud Files?</h3>

<p>Most areas of our data centers have access to our “ServiceNet” in which a customer can connect privately to our Cloud Files infrastructure without traversing the public network (provided the cloud files are in the same DC as the dedicated server making the connection). The older areas of our DFW DC that do not have ServiceNet will need RackConnect to connect to the cloud ServiceNet, which will allow for a private connection to Cloud Files.</p>

<h3>Can RackConnect be used if the dedicated firewall is already set up with multiple segments?</h3>

<p>Yes. RackConnect connects your Rackspace Cloud as an additional interface on your firewall; therefore it allows you to connect to a firewall that has multiple segments set up if enough ports available. Our data center can perform a visual inspection of the firewall to ensure that there is an available port to connect to RackConnect.</p>

<h3>Can I extend my Active Directory (AD) domain across RackConnect into the cloud?</h3>

<p>Customer-owned Active Directory domains can be extended over RackConnect. This includes Active Directory Domain Controllers in your Dedicated environment or in your Cloud environment.</p>

<p>If you are planning to deploy Domain Controllers in the Cloud, and you promote a Cloud Server to a Domain Controller, please make sure to create a ticket and inform the RackConnect team about this change. You will need to manually create a “rackconnect” user account on the Domain and add this account to the “Domain Admins” Global Group. We will add the “DOMAIN\rackconnect” account to the RackConnect system instead of “rackconnect” in order to get RackConnect to work with your Domain Controller cloud server(s).</p>

<p>Additionally, Active Directory requires a large number of open ports to function properly, so we highly recommended that you create RackConnect Network Policies that allow full access between your Cloud and Dedicated environments.</p>

<p><strong>IMPORTANT</strong>: RackConnect Network Policies are limited to Port Ranges of 100.&nbsp; Please view the <a href="/how-to/managing-rackconnect-v20-network-policies">Managing RackConnect Network Policies</a> article for further details.</p>

<p><strong>Note</strong>: Connecting Cloud Servers to the Intensive Active Directory Domains is not currently supported.</p>

<h3>Can I have an additional private IP address on my RackConnected Cloud Servers for SSL routing?</h3>

<p>Unfortunately our Cloud does not allow for additional IP addresses on the private interface. The best work-around for hosting multiple SSL sites would be to host each site on a separate Cloud Server, or utilize PAT (Port Address Translation).</p>

<p>Please view the following article for further details on PAT: <a href="/how-to/multiple-ssl-certificates-on-a-single-rackconnected-cloud-server-pat">Multiple SSL Certificates on a Single RackConnected Cloud Server (PAT)</a>.</p>

<h3>Can Cloud Load Balancers (CLB) be used with RackConnect?</h3>

<p>Utilizing CLB can be a great solution. The key is to clearly understand the use cases for this configuration. CLB works best when all servers to be load balanced reside in the Cloud. If dedicated servers need to be load balanced, or Cloud and Dedicated are to be load balanced together, you should deploy RackConnect with an F5 load balancer. The firewall used with RackConnect serves to further isolate and protect the customers dedicated servers.</p>

<p>Also note that when using CLB with RackConnect, all internet traffic comes and goes through the Cloud, and the customer will pay for all outbound bandwidth at the standard CLB rate. This bandwidth is not included in the “included” bandwidth that comes with each dedicated server.</p>

<p>For further details, please view the article: <a href="/how-to/using-cloud-load-balancers-with-rackconnect">Using Cloud Load Balancers with RackConnect</a></p>

<h3>Do pre-existing snapshots cause issues after an account is set up with RackConnect?</h3>

<p>Snapshots taken of a server before the Cloud sccount was set up with RackConnect should not pose a significant problem after the account is set up with RackConnect. However, a problem can occur if the network stack has been modified or iptables has been set to block all access (which will block the RackConnect system from connecting). Specifically, the snapshot must have a clean SSH configuration that permits root login, with port 22 open in iptables, and accepts password authentication.</p>

<h3>Can I use First Generation Cloud Server customer images with Next Generation Cloud Servers?</h3>

<p>On Friday Nov 2, 2012 Rackspace enabled our final set of images allowing 88% to 90% of our First Generation Servers to be eligible for a snapshot migration to a Next Generation Server. Approximately 130,000 to 135,000 First Generation Cloud Servers can now easily make the transition over to our Next Generation platform powered by OpenStack.</p>

<p>The snapshot migration feature allows a Rackspace customer to take a snapshot of their eligible First Generation Cloud Server, and create a new Next Generation Cloud Server from that snapshot. With a few button clicks, a new Next Generation Cloud Server is up and running that is an exact copy, data-wise, of their First Generation server. With this option, customers will get a new Next Generation cloud server with a new IP address, but will experience no downtime.</p>

<h3>Can I migrate my first generation Cloud Servers to next generation Cloud Servers?</h3>

<p>There will not be an automated migration process available upon launch, but we anticipate that one will be made available in the coming months.</p>

<h3>How do I retrieve the public IP adress for a Next Generation Cloud Server that has been recently provisioned?</h3>

<p>You can view the public IP address of your RackConnect Cloud Server in the following places:</p>

<ul>
	<li>In the RackConnect Management Interface of the <a href="https://my.rackspace.com/">MyRackspace</a> portal, view the IP address on the Overview tab for the server.</li>
</ul>

<ul>
	<li>You can retrieve the public IP address through the Cloud Servers API by querying for Server Details. The field containing the RackConnect Public IP address is called <em>accessIPv4</em>. For details about using the API to retrieve server information, see the <a href="https://developer.rackspace.com/docs/cloud-servers/v2/developer-guide/#document-getting-started/create-server/get-server-details">Get Server Details</a> section in the Cloud Servers v2 Developer Guide .</li>
</ul>

<h3>Can I use next generation Cloud Server Images to Create Cloud Servers in different regions?</h3>

<p>It is not currently possible to use next generation Images (snapshots) created in one region to spin up Cloud Servers in a different region. We expect this functionality to be available in late 2013.</p>

<p>Due to the limitation above, if you would like to use generation Cloud Server Images with RackConnect, please follow this process:</p>

<ol>
	<li>Make sure to create a next generation Cloud Server in the same region as your RackConnect Configuration.</li>
	<li>Once the cloud server is deployed and configured as you would like, you can create an Image (snapshot) of it.</li>
	<li>You can now create new next generation Cloud Servers from this Image, as long as they are created in the same region your RackConnect Configuration is located.</li>
</ol>

<p><strong>Note</strong>: If you have existing next generation Images that were created in a different region than where your RackConnect configuration is located, then it will not be possible to use them with RackConnect until the first half of 2014 (expected timeframe).</p>

---------
<h2>Security tools</h2>

<h3>Can I use Rackconnect as a firewall for my Cloud Servers?</h3>

<p>Yes, you can.</p>

<p>By default the Cloud Servers are directly exposed to the Internet and only the internal OS firewall is available for protection. RackConnect may be deployed as a front-end dedicated firewall to provide a single entry point for public traffic to all your cloud servers. In addition it allows a single point to consolidate your firewall rules for all cloud servers through the use of RackConnect Network Policies.</p>