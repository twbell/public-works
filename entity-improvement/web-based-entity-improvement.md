Improve Business Records
========================

## Overview

This process starts with business records that have "good" data. We want to improve the accuracy and completeness of the business data. There are two main steps:

## Step 1: Verify Website

Check that the record's website is the best available website for the business.

_If you wanted a friend to meet you at the business location described below, would you feel confident emailing your friend the linked website as their only source of finding you?_

To confirm that the website is valid it may be necessary to visit linked pages such as "Contact Us", "About Us", etc., to verify that the contact details match the original business record. If the information does not appear to be the same business, the website should be considered incorrect.

If the website is incorrect, or the record has no website value, use web research to try to find the best website for the business and put that URL in the "website-outcome" field.

If the website value is already correct, fill "website-outcome" with the word "verified". If the website is not correct and you find the correct one, put that website URL in "website-outcome".

If the website is incorrect and you're not able to find the correct website from internet research, leave "website-outcome" blank.

### Chains

Be aware of chains and umbrella companies. If the website is the homepage for an organization that has multiple locations, then the website is probably not corerct (because it's not for the specific business location).
The only way the website would be correct in this case is if the business record appears to be the home office of the organizaiton as shown on the website.

For franchise locations, branch locations and the like, we would like a website that is clearly focused on the business represented by the business record. This can often be accomplished by using the corporate website to do a "locations search" and copying the link from the results for the correct specific location.

Sometimes it is not possible to find a website that represents a specific location, in which case the "website-outcome" field should be left blank.

#### Example: website points to company headquarters; "website-outcome" should be filled with a more specific website

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

The website in this record incorrectly points to the corporate headquarters website. The correct website is for the specific store location in Fairbainks:
http://www3.samsclub.com/clublocator/club_detail.aspx?myClub=6603&nClub=

In this case, the correct website URL was found by starting with a search via the corporate website's "Club Finder" feature.

### Outcomes

At the end of this step, "website-outcome" should contain one of:
* "verified": the current website value is correct
* a new URL: website is blank or is not the best website for the business. the new website URL you found is better
* blank: website is blank or is not the best website for the business, but you could not find a good website

## Step 2: Verify Attributes Using the Website

Use each business's correct website to verify the correctness of the other business data (name, address, locality, region, postcode and tel).

This step should be done for each business record where a good website was verified or corrected in the previous step. (Do not do this step for business records that have incorrect websites, that is, website-outcome was left blank.)

For each of the following attributes in the busines record, verify the value against the value shown on the website. To be correct, the value in the business record should be the same as that on the website and meet the rules for that field:

* **name**: Should have the same spelling, capitalization, and formatting
* **address**: Should have the same spelling, capitalization, and formatting
* **locality**: Should be a city or town in the United States (Los Angeles, New York, Palm Springs, etc.)
* **region**: Should be one of the state abbreviations of the United States (CA, NY, MI, etc.)
* **postcode**: Should have the same spelling, capitalization and formatting, as long as it's post office compliant.
* **tel**: Should be the numbers to call in order to reach the main business line. Prefer non-toll-free numbers. Formatting is not important.

When a value is correct as is, mark it as "verified" in its -outcome field. For example, if the business name on the spreadsheet is "Starbucks" and the website says "Starbucks", then put the word "verified" in the "name-outcome" field.

When a value is blank or incorrect and you can find the correct value on the website, put the correct value in its -outcome field. For example, if the "address" field says, "123 Main St." but the website says "123 Main St., Ste. 456", you should put "123 Main St., Ste. 456" in the "address-outcome" field.

When a value is blank or incorrect but you cannot find the correct value on the website (or there is no website), leave the -outcome field blank for that field. For example, if the "tel" field is blank and the website does not have the telephone, you should leave the "tel-outcome" field blank.

## Mutlipe telephones

If the website has mutliple telephones for the business, select the telephone that appears most likely to reach a real person who works at the business. Do not use fax numbers. Only use a toll-free number value if there's not a non-toll-free number showing.

### Outcomes

At the end of this step, the -outcome fields for each business attribute should be one of:

* "verified": the original value is correct (it matches the value on the business website)
* a new value: the original value was incorrect and you copied the new correct value from the business website
* blank: you could not find a value for this attribute on the business website (or there is no correct business website to use)

For any records that do not have a good website ("website-outcome" was left blank), then all the other -outcome fields should be left blank.

## Overall Outcomes

For each business record, the "website-outcome" field should contain either the word "verified" OR a corrected website link OR should be left blank because you could not find a good website for the business.

Each of the other -outcome fields should contain either the word "verified" OR a corrected value OR should be left blank because you could not verify them from the website.

## Example Work

website|website-outcome|name|name-outcome|address|address-outcome|locality|locality-outcome|region|region-outcome|postcode|postcode-outcome|tel|tel-outcome
--- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | ---
http://www.candcdancecompany.com/	| verified | C & C Dance Co | verified | 4891 Telsa Drive | 4891 Telsa Drive, Suites J - L | Bowie | verified | MD | verified | 20700 | 20715 | (301) 464-4300 | verified

For this record, the website was the correct website and was therefore marked "verified". The other fields were correct except for the address and postcode. The address was corrected to include the suite letters, and the postcode was corrected to be 20715.
