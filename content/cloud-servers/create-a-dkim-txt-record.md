---
node_id: 1502
title: Create a DKIM TXT Record
type: article
created_date: '2012-07-24'
created_by: Rackspace Support
last_modified_date: '2016-01-15'
last_modified_by: Stephanie Fillmon
product: Cloud Servers
product_url: cloud-servers
---

DomainKeys Identified Mail (DKIM) helps you protect your company from
email spamming and phishing attempts. It provides a method for
validating a domain name identity that is associated with a message
through cryptographic authentication.

For a complete description of DKIM, see a recommended list of DKIM sites
under [External Links](#ExternalLinks).

The process of setting up DKIM involves several tasks:

1.  Create a selector. This is a simple, user-defined text string that
    you will associate with a public key in a later step.
2.  Generate a public/private key pair by using a tool such
    as **ssh-keygen** on Linux or **PuTTYgen** on Windows.
3.  Publish the selector and public key by creating a DNS TXT record.
4.  Attach the token to each outgoing email.

This article describes how to create the selector and publish the DKIM
TXT record.

Create a DKIM TXT record
------------------------

**Note:** Before you perform this procedure, choose a text string to use
as your selector and generate a public/private key pair. To publish the
DKIM selector and private key

**To publish the DKIM selector and private key**:

![Add DNS
Record](http://c691244.r44.cf2.rackcdn.com/Add%20DNS%20Record.png)

1.  Log in to the [Cloud Control Panel](https://mycloud.rackspace.com/).
2.  In the top navigation bar, select **Networking &gt; Cloud DNS**.
3.  Click the gear icon next to the name of an existing domain and
    select **Add DNS Record**.
4.  In the popup dialog box, select **TXT Record** as the record type.
5.  Enter the selector in the **Hostname** text box.

    The selector is composed of a text string of your choice, followed
    by the literal string .\_domainkey. followed by your domain. For
    example, if you use default as the text string and myexampledomain
    is your domain name, the selector would look as follows:

        default._domainkey.myexampledomain.com

    You need to enter only the text string and **`._domainkey`** in the
    **Hostname** text box.

6.  Expand the **Text** box by dragging the corner, than enter the
    following information, pasting your public key after **`p=`**:

        v=DKIM1; p=your public key

    When you are finished, the TXT record will look similar to the
    following example:

    ![DKIM DNS TXT
    Record](http://c691244.r44.cf2.rackcdn.com/Add%20DKIM%20DNS%20TXT%20Record.png)

7.  Click **Add Record**.

The DNS TXT record is added to your domain.

For instructions on attaching the token to your outgoing email, go to
[DKIMcore.org](http://dkimcore.org/)

### Related

[Setting up SPF DNS TXT
Records](/how-to/create-an-spf-txt-record)

[Learn More about
DNS](/how-to/learn-more-about-dns)

### External Links

[Dkim.org](http://www.dkim.org)

[DKIMcore.org](http://dkimcore.org/specification.html)



