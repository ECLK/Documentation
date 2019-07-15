# Documentation for Sri Lanka Elections Commission Software

The Elections Commission is an elections-as-a-service organization, with the people and Government of Sri Lanka (GoSL) being their primary customer. Currently, the EC is operating only with that customer but the long term objective of the software is to make it possible to operate any election with varying rules for the electors, candidates, voting technology, results process and so on. 

As of November 2018, our immediate goal is to build a working software platform for the Elections Commission for the purpose of running elections for the GoSL: that is, to be able to run local government, provincial government, parliamentary and presidential elections as well as referendums.

This repository contains various documents for the software starting with design docs to user level docs.

## Structure of Elections

For all GoSL elections other than referendums, the stakeholders of elections are as follows (<a href="https://docs.google.com/drawings/d/1WPGMVZbIvU8_njDV9OQv8GfGbLuRmG26RtWrNYdsBNk/edit">source</a>):

<p align="center">
  <img src="stakeholders.png"/>
</p>


The explanation of each of these are:
* Citizen - citizen of Sri Lanka
* Elector - a person eligible to vote (currently any citizen over age 18)
* Registered elector - an elector who is registered to vote
* Voter - someone who votes in an election
* Independent campaign - a group of people who register for the purpose of competing in an election
* Political party - a registered political party (which can choose to compete in any election)
* Nomination list - list of candidates for a particular election nominated by a particular party

## Administrative Organization

The following diagram depicts the administrative organization of the country as it pertains to elections (<a href="https://docs.google.com/drawings/d/1-rdxbI48zCRmyL4_3STQtReStyICF9JFUdyx2f4ZtBw/edit">source</a>):

<p align="center">
  <img src="adminorg.png"/>
</p>

The left arm of the figure depicts how the country's 9 provinces are structured for administrative purposes. 

The right side shows how it is structured for elections purposes. In particular, the districts of Jaffna and Killinochchi are considered as the Jaffna electoral district; and Vavuniya, Mullaitivu and Mannar are considered as the Vanni electoral district. This reduces the 25 administrative districts to 22 electoral districts.

The electoral district is significant as vote counting centers are typically located centrally at a district level. The 2018 local government election however used a different approach where counting happened at a more granular level.

## Elections Systems Functionality

The functionality of elections software can be categorized into 3 distinct phases: Pre-election, during an election and post-election. 

| Pre-election Period | During Election Period | Post-election Period |
| ---                 | ---                 | ---                  |
| Register electors   | Create an election  |  Publish analytics   |
| Address complaints  | Manage election operations |  Address complaints  |
|                     | Nominate candidates |                      |
|                     | Setup election day  |                      |
|                     | Run voting process  |                      |
|                     | Count votes         |                      |
|                     | Publish results     |                      |
|                     | Address complaints  |                      |

More information about each of these items will be included in various subsystem documents.

## Requirements and Use Cases

While all the features are being implemented using a single common architecture, each area has its own set of detailed requirements and use cases.

See the <a href="requirements">requirements</a> directory for more information.

## Software Architecture

We are designing a single integrated architecture for all the software for supporting the entire election process as indicated in the functionality section above.

The overall architecture follows a microservices architecture approach.

See the <a href="architecture">architecture</a> directory for more information.
