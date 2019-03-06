# Splunk-Notes

## Search-time operation order

| *Order* | *Operation name* | *Can be configured via Splunk Web?* | *Location of file configuration* |
| First | Inline field extraction (no field transform) | Yes | EXTRACT- in a props.conf stanza |
| Second | Field extraction that uses a field transform | Yes | REPORT- in a props.conf stanza. |
| Third | Automatic key-value field extraction | No | props.conf stanzas, where KV_MODE is set to a valid value other than none. If no KV_MODE value is specified for a stanza, it is set to auto by default. |
| Fourth | Field aliasing | Yes | FIELDALIAS- in a props.conf stanza |
| Fifth | Calculated fields | Yes | EVAL- in a props.conf stanza |
| Sixth | Lookups | Yes | LOOKUP- in a props.conf stanza. |
| Seventh | Event types | Yes | eventtypes.conf stanza |
| Eighth | Tags | Yes | tags.conf stanza |

