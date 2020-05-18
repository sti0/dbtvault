<p align="center">
  <img src="https://user-images.githubusercontent.com/25080503/65772647-89525700-e132-11e9-80ff-12ad30a25466.png">
</p>

[![Documentation Status](https://readthedocs.org/projects/dbtvault/badge/?version=stable)](https://dbtvault.readthedocs.io/en/latest/?badge=stable)
[![Join our Slack](https://img.shields.io/badge/Slack-Join-yellow?style=flat&logo=slack)](https://join.slack.com/t/dbtvault/shared_invite/enQtODY5MTY3OTIyMzg2LWJlZDMyNzM4YzAzYjgzYTY0MTMzNTNjN2EyZDRjOTljYjY0NDYyYzEwMTlhODMzNGY3MmU2ODNhYWUxYmM2NjA)


[past docs versions](https://dbtvault.readthedocs.io/en/latest/changelog/)

# dbtvault by [Datavault](https://www.data-vault.co.uk)

Build your own Data Vault data warehouse! dbtvault is a free to use dbt package that generates & executes the ETL you need to run a Data Vault 2.0 Data Warehouse on a Snowflake database.

What does dbtvault offer?
- productivity gains, fewer errors
- multi-threaded execution of the generated SQL
- your data modeller can generate most of the ETL code directly from their mapping metadata
- your ETL developers can focus on the 5% of the SQL code that is different
- dbt generates documentation and data flow diagrams

powered by [dbt](https://www.getdbt.com/), a registered trademark of [Fishtown Analytics](https://www.fishtownanalytics.com/)

## Worked example project

Learn quickly with our worked example:

- [Read the docs](https://dbtvault.readthedocs.io/en/latest/workedexample/)

- [Project Repository](https://github.com/Datavault-UK/snowflakeDemo)

## Currently supported databases:

- [snowflake](https://www.snowflake.com/about/)

## Installation

Add the following to your ```packages.yml```


```yaml
packages:

  - git: "https://github.com/Datavault-UK/dbtvault"
    revision: v0.5 # Latest stable version
```

And run 
```dbt deps```

[Read more on package installation](https://docs.getdbt.com/v0.15.0/docs/package-management)

## Usage

1. Create a model for your table.
2. Provide metadata
3. Call the appropriate template macro

```bash
{{- config(...)                                                           -}}

{{ dbtvault.hub(var('src_pk'), var('src_nk'), var('src_ldts'),
                var('src_source'), var('source'))                          }}
```

## Join our Slack Channel

Talk to our developers and other members of our growing community, get support and discuss anything related to dbtvault or Data Vault 2.0

[![Join our Slack](https://img.shields.io/badge/Slack-Join-yellow?style=flat&logo=slack)](https://join.slack.com/t/dbtvault/shared_invite/enQtODY5MTY3OTIyMzg2LWJlZDMyNzM4YzAzYjgzYTY0MTMzNTNjN2EyZDRjOTljYjY0NDYyYzEwMTlhODMzNGY3MmU2ODNhYWUxYmM2NjA)

## Sign up for early-bird announcements 

[![Sign up](https://img.shields.io/badge/Email-Sign--up-blue)](https://www.data-vault.co.uk/dbtvault/)

Get notified of new features and new releases before anyone else!

## Starting a Data Vault project 

## Contributing
[View our contribution guidelines](CONTRIBUTING.md)

## License
[Apache 2.0](LICENSE.md)