# Public Email Providers Domains

This repository contains a list of domains used from public email providers such as Gmail, Yahoo!, Aol, etc...  
The list includes both free and paid providers.

## Purpose

The purpose of this repository is to identify email addresses originating from public email providers.  

## Data Structure

Each item in the list is a JSON object with the following structure:

```json
{
    "name": "Provider Name",
    "country": "US",
    "description": "Provider Description",
    "free": true,
    "verification": {
        "sms": false,
        "secondaryEmail": false
    },
    "domains": [
        {
            "domain": "example.com",
            "mxRecords": [
                {
                    "priority": "10",
                    "hostname": "host.example.com"
                }
            ]
        }
    ]
}
```

### Fields

| Field | Type | Description |
| ----- | ---- | ----------- |
| `name` | `string` | The name of the email provider. |
| `country` | `string` | The ISO 3166-1 alpha-2 country code of the provider's legal entity (e.g., `US`, `DE`, `GB`). For subsidiaries, uses the ultimate parent company's country. |
| `description` | `string` | A short description of the email provider. |
| `free` | `boolean` | Whether or not the email provider is free to use. |
| `verification` | `object` | An object containing information about the verification methods required by the email provider. |
| `verification.sms` | `boolean` | Whether or not the email provider requires SMS verification. |
| `verification.secondaryEmail` | `boolean` | Whether or not the email provider requires secondary email verification. |
| `domains` | `array` | An array of objects containing information about the domains used by the email provider. |
| `domains.domain` | `string` | The domain name used by the email provider. |
| `domains.mxRecords` | `array` | An array of objects containing information about the MX records used by the email provider. |
| `domains.mxRecords.priority` | `string` | The priority of the MX record. |
| `domains.mxRecords.hostname` | `string` | The hostname of the MX record. |


## Contributions

Contributions are welcome! If you know of an email provider that fits the criteria and is not yet listed, please feel free to open a pull request or issue.

## Disclaimer

While every effort is made to keep this list up-to-date and accurate, the landscape of email providers is constantly changing. Therefore, the information provided here should be used as a guide and not taken as definitive.

## License

This repository is licensed under the [MIT License](LICENSE).
