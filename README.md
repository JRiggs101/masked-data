# standard extract fields

| field                                      | action | notes                                                                                                             |
| ------------------------------------------ | ------ | ----------------------------------------------------------------------------------------------------------------- |
| `animal_name`                              | hash   | for all `hash` we want hashed if there is data and null if not                                                    |
| `authorized_refill_count`                  | keep   |
| `compound_drug`                            | keep   |
| `days_supply`                              | keep   |
| `dispensary_address_one`                   | remove |
| `dispensary_address_two`                   | remove |
| `dispensary_chain_site_id`                 | hash   | does this being filled indicate chain y/n?                                                                        |
| `dispensary_city`                          | keep   | is this 'current' or 'original'? has it been 'cleaned' we want original for everything that has both as an option |
| `dispensary_contact_name`                  | remove |
| `dispensary_dea_number`                    | hash   |
| `dispensary_name`                          | remove |
| `dispensary_national_provider_id`          | hash   |
| `dispensary_ncpdp_id`                      | remove |
| `dispensary_phone_number`                  | remove |
| `dispensary_postal_code`                   | keep   |
| `dispensary_postal_code_extended`          | remove |
| `dispensary_state`                         | keep   |
| `dispenser_first_name`                     | remove |
| `dispenser_last_name`                      | remove |
| `dispenser_middle_name`                    | remove |
| `dispenser_national_provider_identifier`   | hash   |
| `dispenser_prefix`                         | remove |
| `dispenser_state_license_number`           | hash   |
| `dispenser_suffix`                         | remove |
| `drug_name`                                | keep   |
| `drug_sequence`                            | -      | what is this?                                                                                                     |
| `eprescription_order_number`               | hash   |
| `eprescription_reference_number`           | remove |
| `filled_at`                                | keep   |
| `partial_fill`                             | keep   |
| `patient_address_one`                      | remove |
| `patient_address_two`                      | remove |
| `patient_birthdate`                        | hash   |
| `patient_city`                             | keep   |
| `patient_contact`                          | remove |
| `patient_contact_subtype`                  | remove |
| `patient_contact_type`                     | remove |
| `patient_first_name`                       | remove |
| `patient_gender`                           | keep   |
| `patient_identifiable_id`                  | remove |
| `patient_identification_jurisdiction_code` | remove |
| `patient_identification_type`              | remove |
| `patient_identifier`                       | hash   | is this consolidation id? or drivers license no or something else? we do want consolidation_id hashed somewhere   |
| `patient_last_name`                        | remove |
| `patient_location`                         | keep   |
| `patient_middle_name`                      | remove |
| `patient_postal_code`                      | keep   |
| `patient_postal_code_extended`             | remove |
| `patient_prefix`                           | remove |
| `patient_state`                            | keep   |
| `patient_suffix`                           | remove |
| `payment_type`                             | keep   |
| `prescriber_dea_number`                    | hash   |
| `prescriber_employer_name`                 | remove |
| `prescriber_first_name`                    | remove |
| `prescriber_institution_number`            | remove |
| `prescriber_last_name`                     | remove |
| `prescriber_middle_name`                   | remove |
| `prescriber_national_provider_id`          | hash   |
| `prescriber_state_license`                 | hash   |
| `prescription_number`                      | hash   |
| `product_id`                               | -      | is this part of NDC?                                                                                              |
| `product_id_type`                          | -      | what is this?                                                                                                     |
| `quantity`                                 | keep   |
| `refill_number`                            | keep   |
| `rx_norm_code`                             | remove |
| `rx_norm_product_qualifier`                | remove |
| `serial_number`                            | remove | ask doug about these                                                                                              |
| `serial_number_jurisdiction`               | remove |
| `sold_at`                                  | keep   |
| `species`                                  | remove |
| `transmission_form`                        | keep   |
| `units`                                    | keep   | is this actually units or measure or dosage type? data dictionary is confusing on these                           |
| `veterinarian_prescription`                | keep   |
| `written_at`                               | keep   |
| `asap_version`                             | keep   |
| `created_at`                               | keep   |

# additional fields required (as far as we know now)

| field                                                  | action | notes                                                                                            |
| ------------------------------------------------------ | ------ | ------------------------------------------------------------------------------------------------ |
| ndc                                                    | keep   | it looks like maybe the ndc is broken up into parts above, but we would like the full ndc number |
| active ingredient                                      | keep   |
| age band                                               | keep   | needed since DOB will be hashed                                                                  |
| ahfs description                                       | keep   |
| benzodiazepine y/n                                     | keep   |
| brand name                                             | keep   |
| buprenorphine y/n                                      | keep   |
| patient county                                         | keep   |
| prescriber county                                      | keep   |
| dispenser county                                       | keep   |
| dispensary county                                      | keep   |
| daily mme                                              | keep   |
| daily lme                                              | keep   |
| diagnosis code                                         | keep   |
| whatever is missing depending on what `units` is above | keep   |
| drug schedule                                          | keep   |
| generic name                                           | keep   |
| label name                                             | keep   |
| manufacturer/labeler                                   | keep   |
| mat opioid y/n                                         | keep   |
| patient consolidation id                               | hash   |
| patient demographics r/u/sr                            | keep   |
| dispensary demographics r/u/sr                         | keep   |
| dispenser demographics r/u/sr                          | keep   |
| prescriber demographics r/u/sr                         | keep   |
| prescription treatment type                            | keep   |
| release mechanism                                      | keep   |
| strength                                               | keep   |
