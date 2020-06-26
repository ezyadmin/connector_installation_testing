# Connector Installation Testing
Connector installation testing for EzyAdmin Platform 

## Configuration

| key                | description                                     |
| ------------------ | ------------------------------------------------|
| list :             |                                                 |
|                    | [{                                              |
|                    |     "conn_id" : "***{{ connector id }}***"      |
|                    |     "module" : "***{{ connector module }}***"   |
|                    |     "cmd" : "***{{ command_line }}***"          |
|                    |     "regex" : "***{{ regular expression }}***"  |
|                    | }]                                              |


## Example

```bash
ansible-playbook run.yml -i tests/inventory -vvvv --extra-vars="{
  \"list\":[                          \
    {
      \"conn_id\": \"###_connector_id_1###\",
      \"module\": \"###_module_name_1###\",
      \"cmd\": \"###_command_line_1###\",
      \"regex\": \"###_regex_pattern_1###\"
    }, {
      \"conn_id\": \"###_connector_id_2###\",
      \"module\": \"###_module_name_2###\",
      \"cmd\": \"###_command_line_2###\",
      \"regex\": \"###_regex_pattern_2###\"
    }
  ]}"                                     \
;
```

## Testing

```bash
ansible-playbook run.yml -i tests/inventory -vvvv --extra-vars="{
  \"list\":[                          \
    {
      \"conn_id\": \"###_connector_id_1###\",
      \"module\": \"###_module_name_1###\",
      \"cmd\": \"###_command_line_1###\",
      \"regex\": \"###_regex_pattern_1###\"
    }, {
      \"conn_id\": \"###_connector_id_2###\",
      \"module\": \"###_module_name_2###\",
      \"cmd\": \"###_command_line_2###\",
      \"regex\": \"###_regex_pattern_2###\"
    }
  ]}"
```
