# los-angeles-police-killings-data

The Los Angeles Times' database of people killed by local police in Los Angeles County.

## About the data

Since 2000, there have been more than 900 killings by local police that were ruled a homicide by county medical examiners. The Times' [Homicide Report](https://homicide.latimes.com/) compiled the deaths by reviewing publicly-available records from the Los Angeles County Medical Examiner-Coroner's office and verifying information with law enforcement.

The data are published by The Times's in its [police killings database](https://www.latimes.com/projects/los-angeles-police-killings-database/).

The records include each death that has been ruled a homicide by medical examiners, which is the death of a person at the hands of another. Our records do not include deaths that have not been ruled a homicide, such as on-duty vehicular deaths, jail suicides and other in-custody deaths. Some counts, such as those from the local Black Lives Matter chapter, have included such incidents.

The Los Angeles County District Attorney's office reviews each incident to determine whether charges are warranted. Reaching a decision can take years. If a killing is deemed criminal, the officer is prosecuted. If the incident is deemed lawful, the office issues a memo justifying the use of force.

The Times has acquired more than 600 of these reviews dating to 2004 and has published them here, the most comprehensive database of investigations of Los Angeles County police killings ever made public. The latest decisions will be added as they are released.

## Reusing the data

The Los Angeles Times is making police killings data from The Homicide Report available to aid public understanding of the issue.

The company's Terms of Service apply. By using the data, you accept and agree to follow the [Terms of Services](https://www.latimes.com/terms-of-service).

It states that "you may use the content online only, and solely for your personal, non-commercial use, provided you do not remove any trademark, copyright or other notice from such Content," and that, "no other use is permitted without prior written permission of Los Angeles Times."

Reselling the data is forbidden. Any use of these data in published works requires attribution to the Los Angeles Times.

To inquire about reuse, please contact Data and Graphics Editor Ben Welsh at [ben.welsh@latimes.com](mailto:ben.welsh@latimes.com).

## Data dictionary

### [los-angeles-police-killings.csv](./los-angeles-police-killings.csv)

Every killing at the hands of local police declared a homicide since 2000. Each row describes a person who died.


| field                 | type    | description                                       |
| :---------------------| :------ | :------------------------------------------------ |
| `coroners_case_number`| string  | A unique string identifier from the Coroner.      |
| `slug`                | string  | A unique string identifier for the record.        |
| `death_date`          | date    | The date the person died.                         |
| `first_name`          | string  | The person's first name.                          |
| `middle_name`         | string  | The person's middle name.                         |
| `last_name`           | string  | The person's last name.                           |
| `age`                 | integer | The age of the person when they died.             |
| `race`                | string  | The race of the person who died.                  |
| `gender`              | string  | The gender of the person who died.                |
| `cause`               | string  | The cause of the person's death.                  |
| `address`             | string  | The address of the person's death.                |
| `neighborhood`        | string  | The neighborhood where the person died.           |
| `x`                   | float   | The longitude coordinate where the person died.   |
| `y`                   | float   | The latitude coordinate where the person died.    |


### [los-angeles-prosecutor-decisions.csv](./los-angeles-prosecuter-decisions.csv)

Every available review of police killings from Justice System Integrity Division in the district attorney's office.


| field                 | type    | description                                       |
| :---------------------| :------ | :------------------------------------------------ |
| `coroners_case_number`| string  | A unique string identifier from the Coroner.      | 
| `death_date`          | date    | The date the person died.                         |
| `jsid_file_number`    | string  | A unique string identifier from the DA's office.  |
| `decision`            | string  | The district attorney's decision.                 |
| `file_url`            | string  | Documentcloud link where the review is available. |
| `review_release_date` | date    | The date the JSID review was released.            |
| `review_length`       | string  | Length of review in pages.                        |
| `weapon_involvement`  | string  | Weapon involvement during the incident.           |
| `agencies`            | string  | List of unique agencies involved in the killing.  |
