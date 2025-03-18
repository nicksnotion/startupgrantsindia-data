# Contributing to the Startup Grants Directory

We welcome contributions to improve the accuracy, completeness, and structure of the Startup Grants Directory! This project aims to create a comprehensive and community-maintained resource for startups seeking funding. We believe in empowering developers to shape the project, so your suggestions for schema improvements and data handling are highly valued.

## How to Contribute

There are several ways to contribute:

*   **Adding New Grants:**
    1.  Fork the repository.
    2.  Create a new branch for your changes: `git checkout -b add-new-grant-[grant-name]`.
    3.  Edit the `grants.json` file:
        *   Add a new grant entry to the JSON array, adhering to the data schema (see below).
        *   Ensure all fields are accurate and complete.
        *   Use proper JSON syntax.
    4.  Commit your changes: `git add grants.json`
        `git commit -m "Add new grant: [Grant Name]"`
    5.  Push your changes: `git push origin add-new-grant-[grant-name]`
        Note this step assumes this is a simple data structure not having a website.
    6.  Create a pull request.

*   **Updating Existing Grants:**
    1.  Fork the repository.
    2.  Create a new branch for your changes: `git checkout -b update-grant-[grant-id]`.
    3.  Edit the `grants.json` file:
        *   Locate the grant entry by its `grant_id`.
        *   Modify the fields that need updating.
        *   Ensure your changes are accurate and complete.
        *   Use proper JSON syntax.
    4.  Commit your changes: `git add grants.json`
        `git commit -m "Update grant [Grant ID]: [Brief Description of Changes]"`
    5.  Push your changes: `git push origin update-grant-[grant-id]`
    6.  Create a pull request.

*   **Suggesting Schema Improvements:**
    We encourage developers to propose enhancements to the data schema (the structure of the `grants.json` file). This could involve:
    *   Adding new fields to capture more relevant information.
    *   Modifying the data types of existing fields.
    *   Restructuring the JSON data for better organization or queryability.

    To suggest a schema improvement:
    1.  Create a new branch: `git checkout -b propose-schema-change-[short-description]`.
    2.  Create a document (e.g., `proposals/schema-change-[short-description].md`) describing your proposed changes, including:
        *   A clear explanation of the problem you're trying to solve.
        *   A detailed description of the proposed changes to the schema (e.g., "Add a new field called 'application_deadline' with a data type of 'date'").
        *   Examples of how the new schema would be used.
        *   The benefits of the proposed changes.
    3.  Commit your proposal: `git add proposals/schema-change-[short-description].md`
        `git commit -m "Propose schema change: [Short Description]"`
    4.  Push your changes: `git push origin propose-schema-change-[short-description]`
    5.  Create a pull request.

    **We will carefully review all schema proposals and discuss them with the community before implementing any changes.**

*   **Reporting Issues:**
    If you find any errors or inconsistencies in the data, please open an issue on GitHub.

## Data Schema

The `grants.json` file uses the following schema:

(Here, list the current columns, data types, and descriptions. Use a table for clarity:)

| Field Name           | Data Type | Description                                                                                           |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------|
| `grant_id`           | string    | A unique identifier for the grant.                                                                    |
| `grant_name`         | string    | The name of the grant program.                                                                        |
| `source_type`        | string    | The type of organization providing the grant ("Government" or "Private").                             |
| `source_name`        | string    | The name of the organization providing the grant.                                                     |
| `state`              | string    | The state or region where the grant is available.(null if avaible througout the country)              |
| `equity_sharing`     | boolean   | Indicates whether the grant involves sharing equity with the funding organization.                    |
| `is_it_loan`         | boolean   | Indicates whether the funding is a loan (true) or a grant (false).                                    |
| `industry_sector`    | string    | The industry sector that the grant targets (e.g., "Technology", "Healthcare", "Education").           |
| `startup_stage`      | string    | The stage of startup development the grant is intended for (e.g., "Seed", "Early", "Growth").         |
| `grant_amount_min`   | numeric   | The minimum amount of funding available through this grant.                                           |
| `grant_amount_max`   | numeric   | The maximum amount of funding available through this grant.                                           |
| `application_method` | string    | The method to apply for the grant (e.g., "Online", "Mail", "In Person").                              |
| `website`            | string    | URL to apply to the grant.                                                                            |
| `focus_areas`        | string    | Specific areas of focus for the grant (can be multiple, comma-separated).                             |
| `fund_size`          | numeric   | The total size of the fund providing the grants.                                                      |
| `description`        | text      | A detailed description of the grant program.                                                          |
| `application_process`| text      | Details about the application process, requirements, and timeline.                                    |
| `eligibility`        | text      | Criteria that applicants must meet to be eligible for the grant.                                      |
| `slug`               | text      | A URL-friendly version of the grant name for web applications. Must be unique                         |

if any of the data not available then use null. grant_id, grant_name, 
**We encourage developers to suggest improvements to this schema. When proposing changes, please consider:**

*   **Clarity:** Is the new schema easy to understand and use?
*   **Completeness:** Does the schema capture all the essential information about a grant?
*   **Consistency:** Is the schema consistent across all grant entries?
*   **Usefulness:** Does the schema enable efficient searching, filtering, and analysis of the data?
*   **Data Type:** Suggest which data type is correct

## Data Standards

*   All grant data must be accurate and up-to-date.
*   Provide valid URLs for website links.
*   Use consistent formatting and capitalization.
*   If a field is not applicable to a particular grant, leave it blank (or use `null` in the JSON).
*   When suggesting a new scheme let other developers suggest a proper data type for it.

## Code of Conduct

Please be respectful and considerate of other contributors. We are committed to creating a welcoming and inclusive environment for everyone. We reserve the right to remove contributions that are not constructive or that violate our code of conduct.

## Review Process

All contributions will be reviewed by the project maintainers. We may ask you to make changes before we merge your pull request. We will do our best to provide timely feedback.
