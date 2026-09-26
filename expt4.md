# Experiment No. 4: Analyze Email Headers and Detect Email Spoofing Using MHA

## Aim

To analyze an email header using Mail Header Analyzer (MHA) and detect possible email spoofing by examining email routing information and authentication results.

## Requirements

* Gmail / Outlook / Yahoo Mail
* Mail Header Analyzer (MHA)
* Web browser
* WHOIS / IP lookup tool
* Internet connection

## Procedure

### Step 1: Access the Email Header

**Gmail:**

1. Open the email.
2. Click the three-dot menu in the upper-right corner.
3. Select **Show original**.

**Outlook:**

1. Open the email.
2. Click **File**.
3. Select **Properties**.
4. Locate the **Internet headers** section.

**Yahoo:**

1. Open the email.
2. Click the three-dot menu.
3. Select **View raw message**.

### Step 2: Copy the Email Header

Copy the complete email header displayed by the email service.

### Step 3: Analyze the Header Using MHA

1. Open Mail Header Analyzer.
2. Paste the copied email header into the analyzer.
3. Submit the header for analysis.
4. Examine the parsed header information.
5. Identify the `From`, `To`, `Return-Path`, `Received`, and `Message-ID` fields.
6. Check the SPF, DKIM, and DMARC authentication results.

### Step 4: Analyze the Received Fields

Examine the `Received` fields to determine:

* Sending server hostname
* Sending server IP address
* Receiving server
* Date and time of transmission
* Sequence of mail servers

The `Received` headers should be analyzed from the **bottom upward** to trace the email's path.

### Step 5: Check IP Addresses and Hostnames

Use an IP lookup or WHOIS tool to check the IP addresses found in the `Received` headers.

Verify whether:

* The IP belongs to the expected mail server.
* The hostname matches the IP address.
* The sending server appears legitimate.
* Any unexpected server or IP address is present.

### Step 6: Check SPF, DKIM, and DMARC

Record the authentication results.

| Check | Result    | Observation                                |
| ----- | --------- | ------------------------------------------ |
| SPF   | PASS/FAIL | Check whether the sending IP is authorized |
| DKIM  | PASS/FAIL | Check whether the DKIM signature is valid  |
| DMARC | PASS/FAIL | Check domain authentication and alignment  |

### Step 7: Analyze Message-ID

Check the domain used in the `Message-ID` and compare it with the sender's domain.

### Step 8: Identify Possible Spoofing Indicators

Check for:

* `From` and `Return-Path` domain mismatch
* Suspicious IP addresses
* Unexpected hostnames
* SPF failure
* DKIM failure
* DMARC failure
* Unusual timestamps
* Inconsistent mail-server routing
* Suspicious Message-ID domain

## Sample Header

```text
Received: from mail.example.com (mail.example.com [192.0.2.1])
  by mail.receiver.com with ESMTP id u29si8604336pjs.40.2023.08.10.07.00.16;
  Thu, 10 Aug 2023 07:00:16 -0700 (PDT)

Received: by mail.example.com with SMTP id a1mr1243772ywh.51;
  Thu, 10 Aug 2023 07:00:15 -0700 (PDT)

Message-ID: <CA+7eu=4pSeXgQ@mail.example.com>
```

## Analysis

* The email passed through `mail.example.com` before reaching `mail.receiver.com`.
* The sending IP address shown is `192.0.2.1`.
* The timestamps in the `Received` fields are in logical chronological order.
* The `Message-ID` contains the `mail.example.com` domain.
* SPF, DKIM, and DMARC results should be checked in the actual email header.
* Any authentication failure combined with domain or IP inconsistencies should be investigated as a possible spoofing attempt.

## Observation

The email header was successfully parsed using MHA. The sender information, mail-server path, IP address, Message-ID, and email authentication results were examined for inconsistencies.

## Result

The email header was successfully analyzed using Mail Header Analyzer, and possible email spoofing indicators were identified by examining the **Received, Return-Path, Message-ID, SPF, DKIM, and DMARC** fields.

## Conclusion

Email header analysis using MHA can be used to trace the email's delivery path and identify inconsistencies that may indicate email spoofing or phishing.

## Output Screenshots
<img width="1600" height="899" alt="image" src="https://github.com/user-attachments/assets/85e10f7f-c0cb-4e73-a531-e673e3a231eb" />
<img width="1600" height="526" alt="image" src="https://github.com/user-attachments/assets/4e8f8a05-952a-4772-8372-39d01626130f" />
<img width="1600" height="513" alt="image" src="https://github.com/user-attachments/assets/88ee7d43-3674-4409-a540-bebdb81cef4a" />
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/df18391b-59e0-4530-add7-453cfee73d11" />
<img width="1600" height="901" alt="image" src="https://github.com/user-attachments/assets/e068b9dc-64d9-443c-baa7-5ba06346b5e5" />
<img width="1600" height="899" alt="image" src="https://github.com/user-attachments/assets/80c72a4e-c38b-4785-8810-a66a17e6083a" />


