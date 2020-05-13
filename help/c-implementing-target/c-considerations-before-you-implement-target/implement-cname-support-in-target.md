---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Information about working with Adobe Client Care to implement CNAME (Canonical Name) support in Adobe Target.
title: CNAME and Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
---

# CNAME and Adobe Target {#cname-and-adobe-target}

Instructions for working with Adobe Client Care to implement CNAME (Canonical Name) support in [!DNL Adobe Target]. To best handle ad blocking issues, or ITP-related cookie policies, a CNAME is used so calls are made to a domain owned by the customer rather than a domain owned by Adobe.

## Request CNAME support

Perform the following steps to request CNAME support in [!DNL Target]:

1. Adobe's certificate authority (DigiCert) needs to verify Adobe is authorized to generate certificates under your domain. 

   DigiCert calls this process [Domain Control Validation (DCV)](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/), and Adobe will not be allowed to generate a certificate under your domain until this process is complete for at least one of the following DCV methods:
   
   * The quickest DCV method is the DNS CNAME method, in which you add a DNS CNAME record (containing a token) to your domain that points to DigiCert's DCV hostname (`dcv.digicert.com`). This CNAME record indicates to DigiCert that Adobe is authorized to generate the certificate. Adobe Client Care will send you the instructions with the necessary DNS records. An example:

     ```
     3b0332e02daabf31651a5a0d81ba830a.target.example.com.  IN  CNAME  dcv.digicert.com.
     ```

     >[!NOTE]
     >
     >* These DCV tokens expire after 30 days, at which point Adobe Client Care will contact you with updated tokens. For the quickest time to resolution for your CNAME request, be prepared to make these DNS changes on all requested domains before submitting your request.
     >
     >* If your domain has [DNS CAA records](https://en.wikipedia.org/wiki/DNS_Certification_Authority_Authorization), you must add `digicert.com` if it's not already added. This DNS record indicates which certificate authorities are authorized to issue certificates for the domain. The resulting DNS record would look like this: `example.com. IN CAA 0 issue "digicert.com"`. You can use [the G Suite Toolbox](https://toolbox.googleapps.com/apps/dig/#CAA) to determine if your root domain has an existing CAA record. You can read more about how DigiCert handles CAA records [here](https://docs.digicert.com/manage-certificates/dns-caa-resource-record-check).

   * DigiCert also tries the email method, in which it sends email messages to addresses found in the domain's WHOIS information and to pre-determined email addresses (admin, administrator, webmaster, hostmaster, and postmaster `@[domain_name]`). See the [DCV methods documentation](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/) for more information.

     To expedite the DCV email process, DigiCert provides the following recommendation:

     "Please verify that your registrar/WHOIS provider has not masked or removed [relevant email addresses]. If they are, find out if they provide a way (e.g., anonymized email address, web form) for you to allow [certificate authorities] to access your domain’s WHOIS data."

1. Create a CNAME record on your domain's DNS pointing to your regular hostname `clientcode.tt.omtrdc.net`. For example, if your client code is cnamecustomer and your proposed hostname is `target.example.com`, your DNS CNAME record should look something like this:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

1. Open an [Adobe Client Care ticket requesting CNAME support](https://docs.adobe.com/content/help/en/target/using/cmp-resources-and-contact-information.html#reference_ACA3391A00EF467B87930A450050077C) for your [!DNL Target] calls.

   Adobe will work with DigiCert to purchase and deploy your certificate on Adobe's production servers. DigiCert will initiate the DCV process and Adobe Client Care will notify you when your implementation is ready.

1. After completing the preceding tasks and Adobe Client Care has notified you that the implementation is ready, you must update the `serverDomain` to the new CNAME in at.js.

## Frequently Asked Questions

The following information answers frequently asked questions about requesting and implementing CNAME support in [!DNL Target]:

### Can I provide my own certificate (aka bring-your-own-certificate or BYOC)? If so, what's the process?

Yes, you can provide your own certificate; however, it is not recommended. Management of the SSL certificate lifecycle is significantly easier for both Adobe and you when Adobe purchases and controls the certificate. SSL certificates must be renewed every year, which means Adobe Client Care must contact you every year to send Adobe a new certificate in a timely manner. Some customers might have difficulty producing a renewed certificate in a timely manner every year, which jeopardizes their [!DNL Target] implementation because browsers will refuse connections when the certificate expires.

>[!IMPORTANT]
>
>Be aware that if you request a [!DNL Target] bring-your-own-certificate CNAME implementation, you are responsible for providing renewed certificates to Adobe Client Care every year. Allowing your CNAME certificate to expire before Adobe can deploy a renewed certificate will result in an outage for your specific [!DNL Target] implementation.

1. Skip step 1 above, but complete steps 2 and 3. When you open an Adobe Client Care ticket (step 3), let them know you'll be providing your own certificate.

   Adobe will generate and send you a certificate signing request (CSR).

1. Use the CSR to purchase the certificate through your chosen certificate authority (CA).

1. Send the new public certificate to Adobe. Adobe representatives will deploy the public certificate on its production servers.

1. Complete step 4 after Adobe Client Care has notified you that the implementation is ready.

### How long until my new SSL certificate expires?

Certificates issued before September 1, 2020 will be two-year certificates. Certificates issued on or after September 1, 2020 will be one-year certificates. You can read more about the move to one-year certificates [here](https://www.digicert.com/position-on-1-year-certificates).

### What hostnames should I choose? How many hostnames per domain should I choose?

[!DNL Target] CNAME implementations require only one hostname per domain on the SSL certificate and in the customer's DNS, so that's what we recommend. Some customers might require additional hostnames per domain for their own purposes (testing in staging, for example), which is supported.

Most customers choose a hostname like `target.example.com`, so that's what we recommend, but the choice is ultimately yours. Be sure not to request a hostname of an existing DNS record as that would cause a conflict and delay time to resolution of your [!DNL Target] CNAME request.

### I already have a CNAME implementation for [!DNL Adobe Analytics], can we use the same certificate or hostname?

No, [!DNL Target] requires a separate hostname and certificate.

### Is my current implementation of Target impacted by ITP 2.x?

In a Safari browser, navigate to your website on which you have a Target JavaScript library. If you see a Target cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.x.

ITP issues can be resolved for Target with just an Analytics CNAME. You'll need a separate Target CNAME only in the case of ad-blocking scenarios where Target is blocked.

For more information about ITP, see [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### Can Adobe/DigiCert send the DCV emails to another email address `<someone>@example.com`?

No, DigiCert (or any certificate authority) will not allow just anyone with an email address under a domain to authorize an SSL certificate under that same domain unless that email address is also included in the domain's WHOIS information or the pre-determined list of addresses (see above). This ensures that only authorized individuals can approve DCV for a particular domain. If this is not feasible for you, we recommend using the DNS CNAME DCV method (see above).

### How can I validate my CNAME implementation is ready for traffic?

Use the following set of commands (in the MacOs or Linux command-line terminal, using bash and curl 7.49+):

1. First paste this bash function into your terminal:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{17,21,22,26,{28..32},34,35,37,38}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. Next paste this command (replacing `target.example.com` with your hostname):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   If the implementation is ready, you should see output like below. The important part is that all lines show `CN=target.example.com`, which matches our desired hostname. If any of them show `CN=*.tt.omtrdc.net`, the implementation is **not** ready.

   ```
   $ validateEdgeFpsslSni target.example.com
   mboxedge17.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge21.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge22.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge26.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge28.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge29.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge30.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge31.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge32.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge34.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge35.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge37.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge38.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   ```

1. Validate your new DNS CNAME with another curl request, which should also show `CN=target.example.com`:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >If this command fails but the `validateEdgeFpsslSni` command above succeeds, you might need to wait for your DNS updates to fully propagate. DNS records have an associated [TTL (time-to-live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) that dictates cache expiration time for DNS replies of those records, so you may need to wait at least as long as your TTLs. You can use the `dig target.example.com` command or [the G Suite Toolbox](https://toolbox.googleapps.com/apps/dig/#CNAME) to look up your specific TTLs.

## Known limitations

* QA mode will not be sticky when you have CNAME and at.js 1.x because it is based on a third-party cookie. The workaround is to add the preview parameters to each URL you navigate to. QA mode is sticky when you have CNAME and at.js 2.x.
* Currently the `overrideMboxEdgeServer` setting doesn't work properly with CNAME. This should be set as `false` in order to avoid failing requests.
