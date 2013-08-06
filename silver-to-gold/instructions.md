Silver to Gold
==============

This document describes a process for improving "silver data" (data we consider to be ok) into "gold data" (data we consider to be relatively accurate, comprehensive and up to date).

The overall approach is to give attention to each individual record and make a best attempt at accuracy and completeness. This is done using a combination of web research as well as actual phone calls when appropriate.

Below are the main steps in this process:


## Verify Authority Page

The main point in this step is to ensure we have the most up to date, official website ("authority page") for each specific business location. We will use this later to verify individual attributes of the business record.

The "authority page" is the official website for the business. One way to look at this is: _If you wanted a friend to meet you at the business location described below, would you feel confident emailing your friend the linked website as their only source of finding you?_

For each record, verify that its website value is the best, official "authority page" for that specific business location. If the record has not website value, or the website does not appear to be an acceptable authority page, a best effort should be made to find the best authority page and correct the record's website to be the URL for that page.

To confirm the authority page it may be necessary to visit linked pages such as "Contact Us", "About Us", etc., to verify that the contact details at least loosely match our original business record.

If the business record's website does not appear to be the best authority page (or there's no website value at all), web research should be done to attempt to find the best authority page.

### Chains

Be aware of chains and umbrella companies. If the website is the homepage for an organization that has multiple locations, then the website is probably not the authority page.
The only way the website would be the authority page in this case is if the business record appears to be the home office of the organizaiton as shown on the website.

For franchise locations, branch locations, and the like, we would like a URL that will bring up a page that is clearly focused on the business represented by the business record.
Sometimes this is accomplished by using the corporate website to do a "locations search" and copying the link from the results for the correct specific location.

Sometimes it is not possible to obtain a link that represents a specific location, in which case the website field for the record should be made to be blank, meaning no authority page could be found.

#### Example 1: website points to company headquarters; needs to be corrected

Business record:
```
name: "Sam's Club",
postcode: "99701",
locality: "Fairbanks"
region: "AK",
address: "48 College Road",
website: "http://www.samsclub.com/",
tel: "(907) 451-4800",
```

The website in this record incorrectly points to the corporate headquarters. It should be corrected to point to the authority page for the store location in Fairbainks:
http://www3.samsclub.com/clublocator/club_detail.aspx?myClub=6603&nClub=

In this case, the authority page was found by starting with a search via the corporate website's "Club Finder" feature.

### Outcomes

The Verify Authority Page step should be conducted for every record, and should end in one of these outcomes:
* website is the best authority page; stays the same
* website was not best authority page or was blank; correct page was found and record's website was corrected
* website was not best authority page or was blank; correct page was not found so record's website was left (or changed to be) blank


## Verify Attributes via Authority Page

The main goal here is to use the business's authority page to ensure the completeness and accuracy of the business record.

For each of the following attributes in the busines record, verify the value against the value shown on the record's authority page. If the value on the authority page is different, correct the business record value using the indicated rules for each attribute:

* **name**: Should have the same spelling, capitalization, and formatting
* **address**: Should have the same spelling, capitalization, and formatting
* **locality**: Should be one of the standard values (todo)
* **region**: Should be one of the standard values (todo)
* **postcode**: Should have the same spelling, capitalization and formatting, as long as it's post office compliant
* **tel**: Should be the numbers to call in order to reach the main business line. Prefer non-toll-free numbers. Formatting is not important.

## Phone Verify

This step is for business records for which a correct authority page could not be identified, and we have a telephone value.

Because of the relative time and cost overhead of this approach, a best effort should be made to verify a record by all other means before Phone Verification is used.

For each record, make a reasonable attempt to reach a representative of the business by phone and verify each business attribute:

* name
* address
* locality
* region
* postcode
* tel

When a representative is reached, first verify it's the correct business.

If it's not, an attempt should be made to find the correct phone number for the business, and continue with Phone Verification.

For each record where a business rep can be reached, the following attributes should be verified and corrected if necessary. For each attribute we'd like to know whether it was:
* already correct
* blank; now filled with correct value
* incorrect; now corrected
* not verified (due to represetnative not knowing, or not answering for some other reason)

If you reach an automated message on the first attempt, please try at least one more time, preferably at a different time of day (but during normal business hours for the time zone of the business).

If the person asks you questions about who you are, why you're calling or what you're doing with the data, you can say:
_"I'm helping Factual verify they have the correct data for this business. This data will be used to correct Factual's database of businesses."_
If they want to know who Factual is, you can tell them, _"Factual helps people find relevant businesses for mobile and web users searching for particular businesses."_
If the person wants to keep asking more questions, or if they seem annoyed at any time, you are free to politely excuse yourself and mark the record appropriately as described below.

### Outcomes

Each record run through Phone Verify should be marked with one of these summary outcomes:
* Verified (a business representative was reached, and at least one attribute of the business was verified)
* Voicemail (every attempt resulted in an automated voicemail message)
* Unwilling (a person was reached but they were not willing to verify at least one attribute)
* Disconnected (telephone is not in service)
* Wrong Number (telephone number is not for this business, and a correct number could not be found)
* Other (please describe in notes)
