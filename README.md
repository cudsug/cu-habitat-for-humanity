# Analyzing Habitat for Humanity data

## Organization Name
 
## Overview
Habitat for Humanity of Champaign County builds and sells decent, quality, affordable houses to families at a zero percent interest rate.  They select families based on their level of need, willingness to partner with Habitat, acceptance of responsibilities, and ability to repay the mortgage.  They use the store front ReStore to generate revenues to cover virtually all the administrative costs of the affiliate allowing other donations to go directly to home building.

ReStore accepts donations of gently used furniture, appliances, electronics, household items and home improvement supplies.  They have over 15,000 square feet and are located in downtown Champaign.  They accept “just about everything – even the kitchen sink.”  They take donations Tuesday – Friday 10am-6pm and Saturday 10am-4pm.  ReStore has logs of their donations from July 2012 through the present, identifying the number of people who have donated by week if not day.

## Problem Statement
How can ReStore better solicit and support their donor community to both increase donations to ReStore and provide adequate staffing/hours to accept donations?  Are donations to ReStore trending up or down?  Are there certain days of the week or weeks of the year that are historically low or high volume such that Restore should adjust it staffing or hours?  Can anything be inferred about ReStore's donor profile given the geographic location of donors?  

## Data Details
Background:  ReStore accepts donations at loading dock at the back of their downtown store.  Donators drive up, ring bell, and ReStore staff aid in unloading.  The ReStore staff offer a receipt for tax purposes.  This carbon copy form has the below fields that donators fills out with pen.  Later, these forms are type into excel sheet.  If the donator elects not to take a receipt, the event of the donation is noted but no details regarding donator or items is logged.  Generally, the data collection and logging has mixed quality.  The level of data logged changed in FY2017, shifting from the day level to the week.  Data for FY18-19 is incomplete.

### Schema
| Field | Definition |
| ----- | ---------- |
| ID | Auto increment field that also reflects the order in which entries were logged. |
| Date | Date of Donation
| DayOfWeek | Day of the week.  Not consistently populated but can be used to validate that the date field is correct. |
| Type | If the donator is a business, this field has "business."  Not sure this is consistently logged. |
| ReceiptDeclined "Y" indicates the donator did not want a receipt (for tax purposes etc).  No receipt means no name or address information is collected. |
| Address | If donator wanted receipt, address.  Address is mixed quality.  All numbers have been removed to protect privacy. |
| AddToMailingList | "Y" indicates donator wants added to mailing list. |
| VolunteerInterest | "Y" indicates donator would like to volunteer for Habitat. |
| NoOfDonations | A donation is the event itself, not the number of items donated.  Example:  a value of 18 means 18 people made a donation on this DayOfWeek. |
| Notes | Misc data. |
