# Student Engagement Dashboard (Salesforce DX + CI/CD)

This project is a Salesforce DX–based application designed to streamline and manage student interactions within an educational environment. Built on Salesforce Lightning App Builder and Education Cloud, the system enables users to log, categorize, and follow up on student engagements with full metadata-driven configuration.


## Project Overview
- Provides an internal dashboard to track and manage student interactions, including fields for interaction type, notes, follow-up status, and contact lookup
- Uses custom objects, fields, record types, and page layouts to support educational workflows
- Implements Student Interactions as a custom object and includes page layouts tailored to academic staff

## Configure Your Salesforce DX Project

The `sfdx-project.json` file contains useful configuration information for your project. See [Salesforce DX Project Configuration](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_ws_config.htm) in the _Salesforce DX Developer Guide_ for details about this file.

## Technologies and Skills Used
- Salesforce Lightning App Builder
- Salesforce DX (sfdx CLI)
- Salesforce Metadata API
- Lightning Web Components (LWC)
- Apex Programming
- XML Configuration (e.g. object-meta.xml, field-meta.xml)
- GitHub for source control
- CI/CD automation with deployment scripts
- Visual Studio Code with Salesforce Extensions Pack

## Project Structure
student-engagement-dashboard/
├── force-app/
│   └── main/
│       └── default/
│           ├── classes/
│           │   └── EngagementLogic.cls
│           ├── objects/
│           │   └── Student_Interaction__c/
│           │       ├── Student_Interaction__c.object-meta.xml
│           │       └── fields/
│           │           ├── Interaction_Date__c.field-meta.xml
│           │           ├── Interaction_Type__c.field-meta.xml
│           │           ├── Notes__c.field-meta.xml
│           │           └── Student_Name__c.field-meta.xml
│           ├── triggers/
│           │   └── StudentInteractionTrigger.trigger
│           └── layouts/
│               └── Student_Interaction__c-Layout.layout-meta.xml
├── scripts/
│   ├── soql/
│   │   └── account.soql
│   └── apex/
│       └── hello.apex
├── .sfdx/
├── .gitignore
├── sfdx-project.json
└── README.md

## Features
- Custom tab in app navigation bar for "Student Interactions"
- Record creation form with:
  - Interaction Type (Picklist)
  - Notes (Long Text)
  - Follow Up Required (Checkbox)
  - Interaction Date (Date Picker)
  - Student Name (Lookup field to Contact)
- List view for recently created or assigned interactions
- Supports multiple page layouts and related lists

## CI/CD & Version Control
- Project managed via Salesforce DX with metadata-driven files for all configuration
- GitHub used for version control
- Compatible with CI/CD deployment pipelines via GitHub Actions or Jenkins (if extended)

## Read All About It

- [Salesforce Extensions Documentation](https://developer.salesforce.com/tools/vscode/)
- [Salesforce CLI Setup Guide](https://developer.salesforce.com/docs/atlas.en-us.sfdx_setup.meta/sfdx_setup/sfdx_setup_intro.htm)
- [Salesforce DX Developer Guide](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_intro.htm)
- [Salesforce CLI Command Reference](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/cli_reference.htm)
