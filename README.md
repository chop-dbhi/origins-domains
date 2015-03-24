# Origins Domain Models

This repository contains a curated collection of domain models for [Origins](https://github.com/chop-dbhi/origins). A *domain model* is a model that can be used to describe entities in another domain such as a vocabulary.

## Guidelines

- Models must be in the [CSV format](http://origins.readme.io/docs/data-formats#csv)
- The name of the file should be the domain name plus the `.csv` extension
- The line delimiter must be a newline `\n`, not a carriage return `\r`
    - This is so GitHub can properly render the file in preview mode.
- All fields must be present except for the `operation` and `valid_time`.
- Attribute and value domains should be empty or a domain already defined in this repository.
    - This prevents anonymous or internal domains from leaking into the domain models.

## Domain Facts

Facts about the domain itself can be asserted providing a way to specify metadata about the domain. This can be done by using the `@domain` macro in the `entity` column.

entity_domain|domain|attribute_domain|attribute|value_domain|value
----|----|----|----|----|----|----|----
mydomain|@domain||author||John Doe
mydomain|@domain||description||This domain represents...