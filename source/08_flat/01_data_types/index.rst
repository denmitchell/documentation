RM-Mappings
=================
.. warning:: WIP

COMPOSITION
---------------------
(see also https://specifications.openehr.org/releases/RM/latest/ehr.html#_composition_class)

.. code-block:: json

 {
   
  "conformance-ehrbase.de.v0/language|code": "en",
  "conformance-ehrbase.de.v0/language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/territory|code": "US",
  "conformance-ehrbase.de.v0/territory|terminology": "ISO_3166-1",
  "conformance-ehrbase.de.v0/category|code": "433",
  "conformance-ehrbase.de.v0/category|value": "event",
  "conformance-ehrbase.de.v0/category|terminology": "openehr",
  "conformance-ehrbase.de.v0/context/start_time": "2021-12-21T14:19:31.649613+01:00",
  "conformance-ehrbase.de.v0/context/setting|code": "238",
  "conformance-ehrbase.de.v0/context/setting|value": "other care",
  "conformance-ehrbase.de.v0/context/setting|terminology": "openehr",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|magnitude": 65.9,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|unit": "unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/time": "2021-12-21T16:02:58.0094262+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/encoding|code": "UTF-8",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/encoding|terminology": "IANA_character-sets",
  "conformance-ehrbase.de.v0/composer|name": "Silvia Blake"
  }
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/_uid": "6e3a9506-b81c-4d74-a37f-1464fb7106b2::ehrbase.org::1",
  "conformance-ehrbase.de.v0/language|code": "en",
  "conformance-ehrbase.de.v0/language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/territory|code": "US",
  "conformance-ehrbase.de.v0/territory|terminology": "ISO_3166-1",
  "conformance-ehrbase.de.v0/category|code": "433",
  "conformance-ehrbase.de.v0/category|value": "event",
  "conformance-ehrbase.de.v0/category|terminology": "openehr",
  "conformance-ehrbase.de.v0/context/_health_care_facility|id": "9091",
  "conformance-ehrbase.de.v0/context/_health_care_facility|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/context/_health_care_facility|id_namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/context/_health_care_facility|name": "Hospital",
  "conformance-ehrbase.de.v0/context/_participation:0|function": "requester",
  "conformance-ehrbase.de.v0/context/_participation:0|mode": "face-to-face communication",
  "conformance-ehrbase.de.v0/context/_participation:0|name": "Dr. Marcus Johnson",
  "conformance-ehrbase.de.v0/context/_participation:0|id": "199",
  "conformance-ehrbase.de.v0/context/_participation:0|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/context/_participation:0|id_namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/context/start_time": "2021-12-21T14:19:31.649613+01:00",
  "conformance-ehrbase.de.v0/context/_end_time": "2021-12-21T15:19:31.649613+01:00",
  "conformance-ehrbase.de.v0/context/_location": "microbiology lab 2",
  "conformance-ehrbase.de.v0/context/setting|code": "238",
  "conformance-ehrbase.de.v0/context/setting|value": "other care",
  "conformance-ehrbase.de.v0/context/setting|terminology": "openehr",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|magnitude": 65.9,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|unit": "unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/time": "2021-12-21T16:02:58.0094262+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/encoding|code": "UTF-8",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/encoding|terminology": "IANA_character-sets",
  "conformance-ehrbase.de.v0/_link:0|type": "problem",
  "conformance-ehrbase.de.v0/_link:0|meaning": "problem related note",
  "conformance-ehrbase.de.v0/_link:0|target": "ehr://ehr.network/347a5490-55ee-4da9-b91a-9bba710f730e",
  "conformance-ehrbase.de.v0/composer|name": "Silvia Blake",
  "conformance-ehrbase.de.v0/composer|id": "1234-5678",
  "conformance-ehrbase.de.v0/composer|id_scheme": "UUID",
  "conformance-ehrbase.de.v0/composer|id_namespace": "EHR.NETWORK"
  }

+-----------------+--------------------+---------------+----------+-----------------------------------------------------------+
| Flat Path       | Flat type          | RM Path       | Required | Note                                                      |
+=================+====================+===============+==========+===========================================================+
| /language       | `CODE_PHRASE`_     | language      | Yes      |                                                           |
+-----------------+--------------------+---------------+----------+-----------------------------------------------------------+
| /territory      | `CODE_PHRASE`_     | territory     | Yes      |                                                           |
+-----------------+--------------------+---------------+----------+-----------------------------------------------------------+
| /category       | `DV_CODED_TEXT`_   | category      | yes      |                                                           |
+-----------------+--------------------+---------------+----------+-----------------------------------------------------------+
| /composer       | `PARTY_PROXY`_     | composer      | yes      | add ctx/composer_self:true to set composer to PARTY_SELF  |
+-----------------+--------------------+---------------+----------+-----------------------------------------------------------+
| /context        | `EVENT_CONTEXT`_   | context       | yes      |                                                           |
+-----------------+--------------------+---------------+----------+-----------------------------------------------------------+
| /_link:i        | `LINK`_            | links         | no       |                                                           |
+-----------------+--------------------+---------------+----------+-----------------------------------------------------------+
| /_feeder_audit  | `FEEDER_AUDIT`_    | feeder_audit  | no       |                                                           |
+-----------------+--------------------+---------------+----------+-----------------------------------------------------------+
| /_uid           | STRING             | uid.value     | no       |                                                           |
+-----------------+--------------------+---------------+----------+-----------------------------------------------------------+

ADMIN_ENTRY
---------------------
(see also https://specifications.openehr.org/releases/RM/latest/ehr.html#_admin_entry_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/dv_text": "DV_TEXT 56",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/encoding|code": "UTF-8",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/encoding|terminology": "IANA_character-sets"

  }
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/dv_text": "DV_TEXT 56",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/encoding|code": "UTF-8",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/encoding|terminology": "IANA_character-sets",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_other_participation:0|function": "requester",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_other_participation:0|mode": "face-to-face communication",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_other_participation:0|name": "Dr. Marcus Johnson",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_other_participation:0|id": "199",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_other_participation:0|id_namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_other_participation:0|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_other_participation:1|function": "performer",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_other_participation:1|mode": "not specified",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_other_participation:1|name": "Lara Markham",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_other_participation:1|id": "198",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_other_participation:1|id_namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_other_participation:1|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_work_flow_id|type": "WORKFLOW",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_work_flow_id|namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_work_flow_id|id": "335645",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_work_flow_id|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_uid":"9fcc1c70-9349-444d-b9cb-8fa817697f5e",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_link:0|type": "problem",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_link:0|meaning": "problem related note",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_link:0|target": "ehr://ehr.network/347a5490-55ee-4da9-b91a-9bba710f730e",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_feeder_audit/originating_system_audit|version_id": "final",
  "conformance-ehrbase.de.v0/conformance_section/conformance_admin_entry/_feeder_audit/originating_system_audit|system_id": "orig"

  }

+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| Flat Path        | Flat type        | RM Path         | Required  | Note                                                                  |
+==================+==================+=================+===========+=======================================================================+
| /language        | `CODE_PHRASE`_   | language        | Yes       |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /territory       | `CODE_PHRASE`_   | territory       | Yes       |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /subject         | `PARTY_PROXY`_   | subject         | no        | will be set to PARTY_SELF if not explicitly set                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /_work_flow_id   | `OBJECT_REF`_    | workflow_id     | no        |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /_link:i         | `LINK`_          | links           | no        |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /_feeder_audit   | `FEEDER_AUDIT`_  | feeder_audit    | no        |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /_uid            | STRING           | uid.value       | no        |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+

INSTRUCTION
---------------------
(see also https://specifications.openehr.org/releases/RM/latest/ehr.html#_instruction_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/current_activity/dv_text": "DV_TEXT 45",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/current_activity/timing": "R4/2022-01-31T10:00:00+01:00/P3M",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/current_activity/timing|formalism": "timing",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/dv_text": "DV_TEXT 91",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/expiry_time": "2022-01-31T10:33:28.724259+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/narrative": "Human readable instruction narrative",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/encoding|code": "UTF-8",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/encoding|terminology": "IANA_character-sets"
  }
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/current_activity/dv_text": "DV_TEXT 45",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/current_activity/timing": "R4/2022-01-31T10:00:00+01:00/P3M",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/current_activity/timing|formalism": "timing",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/current_activity/action_archetype_id": "/openEHR-EHR-CLUSTER.conformance_action.v0/",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/dv_text": "DV_TEXT 91",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/expiry_time": "2022-01-31T10:33:28.724259+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/narrative": "Human readable instruction narrative",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_wf_definition|value": "wf_definition",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_wf_definition|formalism": "formalism",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/encoding|code": "UTF-8",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/encoding|terminology": "IANA_character-sets",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_other_participation:0|function": "requester",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_other_participation:0|mode": "face-to-face communication",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_other_participation:0|name": "Dr. Marcus Johnson",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_other_participation:0|id": "199",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_other_participation:0|id_namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_other_participation:0|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_other_participation:1|function": "performer",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_other_participation:1|mode": "not specified",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_other_participation:1|name": "Lara Markham",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_other_participation:1|id": "198",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_other_participation:1|id_namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_other_participation:1|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_guideline_id|type": "GUIDELINE",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_guideline_id|namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_guideline_id|id": "3445",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_guideline_id|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_work_flow_id|type": "WORKFLOW",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_work_flow_id|namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_work_flow_id|id": "335645",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_work_flow_id|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_uid":"9fcc1c70-9349-444d-b9cb-8fa817697f5e",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_link:0|type": "problem",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_link:0|meaning": "problem related note",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_link:0|target": "ehr://ehr.network/347a5490-55ee-4da9-b91a-9bba710f730e",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_feeder_audit/originating_system_audit|version_id": "final",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_feeder_audit/originating_system_audit|system_id": "orig"
  }

+------------------+------------------+----------------+-----------+--------------------------------------------------+
| Flat Path        | Flat type        | RM Path        | Required  | Note                                             |
+==================+==================+================+===========+==================================================+
| /language        | `CODE_PHRASE`_   | language       | Yes       |                                                  |
+------------------+------------------+----------------+-----------+--------------------------------------------------+
| /territory       | `CODE_PHRASE`_   | territory      | Yes       |                                                  |
+------------------+------------------+----------------+-----------+--------------------------------------------------+
| /narrative       | `DV_TEXT`_       | narrative      | yes       |                                                  |
+------------------+------------------+----------------+-----------+--------------------------------------------------+
| /_expiry_time    | `DV_DATE_TIME`_  | expiry_time    | Yes       |                                                  |
+------------------+------------------+----------------+-----------+--------------------------------------------------+
| /_wf_definition  | `DV_PARSABLE`_   | wf_definition  | no        |                                                  |
+------------------+------------------+----------------+-----------+--------------------------------------------------+
| /subject         | `PARTY_PROXY`_   | subject        | no        | will be set to PARTY_SELF if not explicitly set  |
+------------------+------------------+----------------+-----------+--------------------------------------------------+
| /_guideline_id   | `OBJECT_REF`_    | guideline_id   | no        |                                                  |
+------------------+------------------+----------------+-----------+--------------------------------------------------+
| /_work_flow_id   | `OBJECT_REF`_    | workflow_id    | no        |                                                  |
+------------------+------------------+----------------+-----------+--------------------------------------------------+
| /_link:i         | `LINK`_          | links          | no        |                                                  |
+------------------+------------------+----------------+-----------+--------------------------------------------------+
| /_feeder_audit   | `FEEDER_AUDIT`_  | feeder_audit   | no        |                                                  |
+------------------+------------------+----------------+-----------+--------------------------------------------------+
| /_uid            | STRING           | uid.value      | no        |                                                  |
+------------------+------------------+----------------+-----------+--------------------------------------------------+


ACTION
---------------------
(see also https://specifications.openehr.org/releases/RM/latest/ehr.html#_evaluation_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/dv_text": "dv_text in description",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/dv_text2": "dv_text in protocol",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/current_state|code": "532",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/current_state|value": "completed",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/current_state|terminology": "openehr",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/time": "2022-01-31T10:33:28.72414+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/encoding|code": "UTF-8",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/encoding|terminology": "IANA_character-sets"
  }
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/dv_text": "dv_text in description",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/dv_text2": "dv_text in protocol",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/current_state|code": "532",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/current_state|value": "completed",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/current_state|terminology": "openehr",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_instruction_details|path": "/content[openEHR-EHR-SECTION.conformance_section.v0]/items[openEHR-EHR-INSTRUCTION.conformance_instruction.v0]",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_instruction_details|composition_uid": "4cdc3017-d8c5-4cd3-9900-f3bb7171d006",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_instruction_details|activity_id": "activities[at0001]",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/time": "2022-01-31T10:33:28.72414+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/encoding|code": "UTF-8",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/encoding|terminology": "IANA_character-sets",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_other_participation:0|function": "requester",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_other_participation:0|mode": "face-to-face communication",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_other_participation:0|name": "Dr. Marcus Johnson",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_other_participation:0|id": "199",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_other_participation:0|id_namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_other_participation:0|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_other_participation:1|function": "performer",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_other_participation:1|mode": "not specified",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_other_participation:1|name": "Lara Markham",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_other_participation:1|id": "198",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_other_participation:1|id_namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_other_participation:1|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_guideline_id|type": "GUIDELINE",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_guideline_id|namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_guideline_id|id": "3445",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_guideline_id|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_work_flow_id|type": "WORKFLOW",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_work_flow_id|namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_work_flow_id|id": "335645",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_work_flow_id|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_uid":"9fcc1c70-9349-444d-b9cb-8fa817697f5e",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_link:0|type": "problem",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_link:0|meaning": "problem related note",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_link:0|target": "ehr://ehr.network/347a5490-55ee-4da9-b91a-9bba710f730e",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_feeder_audit/originating_system_audit|version_id": "final",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_feeder_audit/originating_system_audit|system_id": "orig"
  }

+------------------------+--------------------------+----------------------+-----------+--------------------------------------------------+
| Flat Path              | Flat type                | RM Path              | Required  | Note                                             |
+========================+==========================+======================+===========+==================================================+
| /language              | `CODE_PHRASE`_           | language             | Yes       |                                                  |
+------------------------+--------------------------+----------------------+-----------+--------------------------------------------------+
| /territory             | `CODE_PHRASE`_           | territory            | Yes       |                                                  |
+------------------------+--------------------------+----------------------+-----------+--------------------------------------------------+
| /time                  | `DV_DATE_TIME`_          | time                 | YES       |                                                  |
+------------------------+--------------------------+----------------------+-----------+--------------------------------------------------+
| /ism_transition        | `ISM_TRANSITION`_        | ism_transition       | Yes       |                                                  |
+------------------------+--------------------------+----------------------+-----------+--------------------------------------------------+
| /_instruction_details  | `INSTRUCTION_DETAILS`_   | instruction_details  | no        |                                                  |
+------------------------+--------------------------+----------------------+-----------+--------------------------------------------------+
| /subject               | `PARTY_PROXY`_           | subject              | no        | will be set to PARTY_SELF if not explicitly set  |
+------------------------+--------------------------+----------------------+-----------+--------------------------------------------------+
| /_guideline_id         | `OBJECT_REF`_            | guideline_id         | no        |                                                  |
+------------------------+--------------------------+----------------------+-----------+--------------------------------------------------+
| /_work_flow_id         | `OBJECT_REF`_            | workflow_id          | no        |                                                  |
+------------------------+--------------------------+----------------------+-----------+--------------------------------------------------+
| /_link:i               | `LINK`_                  | links                | no        |                                                  |
+------------------------+--------------------------+----------------------+-----------+--------------------------------------------------+
| /_feeder_audit         | `FEEDER_AUDIT`_          | feeder_audit         | no        |                                                  |
+------------------------+--------------------------+----------------------+-----------+--------------------------------------------------+
| /_uid                  | STRING                   | uid.value            | no        |                                                  |
+------------------------+--------------------------+----------------------+-----------+--------------------------------------------------+


EVALUATION
---------------------
(see also https://specifications.openehr.org/releases/RM/latest/ehr.html#_evaluation_class)

.. code-block:: json

 {

  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/dv_text": "dv_text in data",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/dv_text2": "dv_text in protocol",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/encoding|code": "UTF-8",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/encoding|terminology": "IANA_character-sets"

  }
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/dv_text": "dv_text in data",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/dv_text2": "dv_text in protocol",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/encoding|code": "UTF-8",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/encoding|terminology": "IANA_character-sets",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_other_participation:0|function": "requester",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_other_participation:0|mode": "face-to-face communication",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_other_participation:0|name": "Dr. Marcus Johnson",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_other_participation:0|id": "199",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_other_participation:0|id_namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_other_participation:0|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_other_participation:1|function": "performer",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_other_participation:1|mode": "not specified",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_other_participation:1|name": "Lara Markham",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_other_participation:1|id": "198",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_other_participation:1|id_namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_other_participation:1|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_guideline_id|type": "GUIDELINE",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_guideline_id|namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_guideline_id|id": "3445",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_guideline_id|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_work_flow_id|type": "WORKFLOW",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_work_flow_id|namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_work_flow_id|id": "335645",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_work_flow_id|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_uid":"9fcc1c70-9349-444d-b9cb-8fa817697f5e",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_link:0|type": "problem",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_link:0|meaning": "problem related note",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_link:0|target": "ehr://ehr.network/347a5490-55ee-4da9-b91a-9bba710f730e",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_feeder_audit/originating_system_audit|version_id": "final",
  "conformance-ehrbase.de.v0/conformance_section/conformance_evaluation/_feeder_audit/originating_system_audit|system_id": "orig"

  }

+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| Flat Path        | Flat type        | RM Path         | Required  | Note                                                                  |
+==================+==================+=================+===========+=======================================================================+
| /language        | `CODE_PHRASE`_   | language        | Yes       |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /territory       | `CODE_PHRASE`_   | territory       | Yes       |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /subject         | `PARTY_PROXY`_   | subject         | no        | will be set to PARTY_SELF if not explicitly set                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /_guideline_id   | `OBJECT_REF`_    | guideline_id    | no        |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /_work_flow_id   | `OBJECT_REF`_    | workflow_id     | no        |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /_link:i         | `LINK`_          | links           | no        |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /_feeder_audit   | `FEEDER_AUDIT`_  | feeder_audit    | no        |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /_uid            | STRING           | uid.value       | no        |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+

OBSERVATION
---------------------
(see also https://specifications.openehr.org/releases/RM/latest/ehr.html#_composition_class)

.. code-block:: json

 {

  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|magnitude": 65.9,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|unit": "unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text_state": "DV_TEXT in State",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/dv_text": "dv_text in protocol",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/time": "2021-12-21T16:02:58.0094262+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/encoding|code": "UTF-8",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/encoding|terminology": "IANA_character-sets"

  }
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|magnitude": 65.9,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|unit": "unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text_state": "DV_TEXT in State",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/dv_text": "dv_text in protocol",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/time": "2021-12-21T16:02:58.0094262+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/history_origin": "2021-12-20T16:02:58.0094262+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/encoding|code": "UTF-8",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/encoding|terminology": "IANA_character-sets",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/subject|id": "1234-5678",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/subject|id_scheme": "UUID",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/subject|id_namespace": "EHR.NETWORK",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/subject|name": "Silvia Blake",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/subject/_identifier:0|id": "122",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/subject/_identifier:0|issuer": "issuer",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/subject/_identifier:0|assigner": "assigner",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/subject/_identifier:0|type": "type",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/subject/relationship|code": "10",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/subject/relationship|value": "mother",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_provider|name": "Dr. Marcus Johnson",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_other_participation:0|function": "requester",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_other_participation:0|mode": "face-to-face communication",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_other_participation:0|name": "Dr. Marcus Johnson",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_other_participation:0|id": "199",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_other_participation:0|id_namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_other_participation:0|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_other_participation:1|function": "performer",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_other_participation:1|mode": "not specified",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_other_participation:1|name": "Lara Markham",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_other_participation:1|id": "198",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_other_participation:1|id_namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_other_participation:1|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_guideline_id|type": "GUIDELINE",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_guideline_id|namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_guideline_id|id": "3445",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_guideline_id|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_work_flow_id|type": "WORKFLOW",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_work_flow_id|namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_work_flow_id|id": "335645",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_work_flow_id|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_uid":"9fcc1c70-9349-444d-b9cb-8fa817697f5e",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_link:0|type": "problem",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_link:0|meaning": "problem related note",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_link:0|target": "ehr://ehr.network/347a5490-55ee-4da9-b91a-9bba710f730e",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/originating_system_audit|version_id": "final",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/originating_system_audit|system_id": "orig",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/original_content": "Hello world!",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/original_content|formalism": "text/plain"

  }

+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| Flat Path        | Flat type        | RM Path         | Required  | Note                                                                  |
+==================+==================+=================+===========+=======================================================================+
| /language        | `CODE_PHRASE`_   | language        | Yes       |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /territory       | `CODE_PHRASE`_   | territory       | Yes       |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /history_origin  | `DV_DATE_TIME`_  | history.origin  | no        | will be set to the time of the earliest event if not explicitly set   |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /subject         | `PARTY_PROXY`_   | subject         | no        | will be set to PARTY_SELF if not explicitly set                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /_guideline_id   | `OBJECT_REF`_    | guideline_id    | no        |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /_work_flow_id   | `OBJECT_REF`_    | workflow_id     | no        |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /_link:i         | `LINK`_          | links           | no        |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /_feeder_audit   | `FEEDER_AUDIT`_  | feeder_audit    | no        |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+
| /_uid            | STRING           | uid.value       | no        |                                                                       |
+------------------+------------------+-----------------+-----------+-----------------------------------------------------------------------+

ELEMENT
-------
(see also https://specifications.openehr.org/releases/RM/latest/data_structures.html#_element_class)

.. note:: Using FLAT format there is no difference between an ELEMENT and its value.

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|magnitude": 65.9,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|unit": "unit"
  }
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|magnitude": 65.9,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|unit": "unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_uid":"9fcc1c70-9349-444d-b9cb-8fa817697f5e",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_link:0|type": "problem",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_link:0|meaning": "problem related note",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_link:0|target": "ehr://ehr.network/347a5490-55ee-4da9-b91a-9bba710f730e",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_feeder_audit/originating_system_audit|version_id": "final",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_feeder_audit/originating_system_audit|system_id": "orig"
 }
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_null_flavour|code": "253",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_null_flavour|value": "unknown",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_null_flavour|terminology": "openehr",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_null_reason": "sample reason"
  }

+-----------------+--------------------+---------------+-----------+---------+
| Flat Path       | Flat type          | RM Path       | Required  | Note    |
+=================+====================+===============+===========+=========+
| /_null_flavour  | `DV_CODED_TEXT`_   | null_flavour  | no        |         |
+-----------------+--------------------+---------------+-----------+---------+
| /_null_reason   | `DV_TEXT`_         | null_reason   | no        |         |
+-----------------+--------------------+---------------+-----------+---------+
| /_link:i        | `LINK`_            | links         | no        |         |
+-----------------+--------------------+---------------+-----------+---------+
| /_feeder_audit  | `FEEDER_AUDIT`_    | feeder_audit  | no        |         |
+-----------------+--------------------+---------------+-----------+---------+
| /_uid           | STRING             | uid.value     | no        |         |
+-----------------+--------------------+---------------+-----------+---------+



CLUSTER
--------
(see also https://specifications.openehr.org/releases/RM/latest/data_structures.html#_cluster_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/conformance_cluster/labresult/text_value": "labresult 4"
  }
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/conformance_cluster/labresult/text_value": "labresult 4",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/conformance_cluster/_feeder_audit/originating_system_audit|version_id": "final",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/conformance_cluster/_feeder_audit/originating_system_audit|system_id": "orig",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/conformance_cluster/_uid":"9fcc1c70-9349-444d-b9cb-8fa817697f5e",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/conformance_cluster/_link:0|type": "problem",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/conformance_cluster/_link:0|meaning": "problem related note",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/conformance_cluster/_link:0|target": "ehr://ehr.network/347a5490-55ee-4da9-b91a-9bba710f730e"
  }

+-----------------+-------------------+---------------+-----------+---------+
| Flat Path       | Flat type         | RM Path       | Required  | Note    |
+=================+===================+===============+===========+=========+
| /_link:i        | `LINK`_           | links         | no        |         |
+-----------------+-------------------+---------------+-----------+---------+
| /_feeder_audit  | `FEEDER_AUDIT`_   | feeder_audit  | no        |         |
+-----------------+-------------------+---------------+-----------+---------+
| /_uid           | STRING            | uid.value     | no        |         |
+-----------------+-------------------+---------------+-----------+---------+


LINK
---------------------
(see also https://specifications.openehr.org/releases/RM/latest/common.html#_link_class)


.. code-block:: json

 {
  "conformance-ehrbase.de.v0/_link:0|type": "problem",
  "conformance-ehrbase.de.v0/_link:0|meaning": "problem related note",
  "conformance-ehrbase.de.v0/_link:0|target": "ehr://ehr.network/347a5490-55ee-4da9-b91a-9bba710f730e"
  }

+-----------------+--------------------+---------------+----------+---------+
| Flat Path       | Flat type          | RM Path       | Required | Note    |
+=================+====================+===============+==========+=========+
+-----------------+--------------------+---------------+----------+---------+
| \|type          | STRING             | type.value    | yes      |         |
+-----------------+--------------------+---------------+----------+---------+
| \|meaning       | STRING             | meaning.value | yes      |         |
+-----------------+--------------------+---------------+----------+---------+
| \|type          | STRING             | type.value    | yes      |         |
+-----------------+--------------------+---------------+----------+---------+




FEEDER_AUDIT
---------------------
(see also https://specifications.openehr.org/releases/RM/latest/common.html#_feeder_audit_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_audit|system_id": "orig"
  }
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_audit|version_id": "final",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_audit|system_id": "orig",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_audit/location|id": "12342341",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_audit/location|id_namespace": "uk.org.nmc",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_audit/location|id_scheme": "NMC",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_audit/location|name": "Org 1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_audit/subject|id": "456",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_audit/subject|id_namespace": "uk.org.nmc",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_audit/subject|id_scheme": "NMC",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_audit/subject|name": "Per 1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_audit/provider|id": "456",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_audit/provider|id_namespace": "uk.org.nmc",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_audit/provider|id_scheme": "NMC",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_audit/provider|name": "Per 1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_audit|time": "2021-12-21T16:02:58.0094262+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_item_id:0|id": "id1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_item_id:0|issuer": "issuer1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_item_id:0|assigner": "assigner1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_item_id:0|type": "PERSON",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_item_id:1|id": "id2",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_item_id:1|issuer": "issuer2",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_item_id:1|assigner": "assigner2",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/originating_system_item_id:1|type": "PERSON",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/original_content": "Hello world!",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/original_content|formalism": "text/plain",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_item_id:0|id": "id1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_item_id:0|issuer": "issuer1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_item_id:0|assigner": "assigner1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_item_id:0|type": "PERSON",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_item_id:1|id": "id2",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_item_id:1|issuer": "issuer2",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_item_id:1|assigner": "assigner2",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_item_id:1|type": "PERSON",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_audit|version_id": "final",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_audit|system_id": "orig",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_audit/location|id": "12342341",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_audit/location|id_namespace": "uk.org.nmc",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_audit/location|id_scheme": "NMC",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_audit/location|name": "Org 1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_audit/subject|id": "456",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_audit/subject|id_namespace": "uk.org.nmc",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_audit/subject|id_scheme": "NMC",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_audit/subject|name": "Per 1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_audit/provider|id": "456",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_audit/provider|id_namespace": "uk.org.nmc",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_audit/provider|id_scheme": "NMC",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_audit/provider|name": "Per 1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/_feeder_audit/feeder_system_audit|time": "2021-12-21T16:02:58.0094262+01:00"
  }

+--------------------------------+----------------------------+------------------------------+----------+-------------------------------------------------------------------------+
| Flat Path                      | Flat type                  | RM Path                      | Required | Note                                                                    |
+================================+============================+==============================+==========+=========================================================================+
| /originating_system_item_id:i  | `DV_IDENTIFIER`_           | originating_system_item_ids  | no       |                                                                         |
+--------------------------------+----------------------------+------------------------------+----------+-------------------------------------------------------------------------+
| /feeder_system_item_id:i       | `DV_IDENTIFIER`_           | feeder_system_item_ids       | no       |                                                                         |
+--------------------------------+----------------------------+------------------------------+----------+-------------------------------------------------------------------------+
| /original_content              | `DV_PARSABLE`_             | original_content             | no       | one one of original_content and original_content_multimedia can be set  |
+--------------------------------+----------------------------+------------------------------+----------+-------------------------------------------------------------------------+
| /original_content_multimedia   | `DV_MULTIMEDIA`_           | original_content             | no       | one one of original_content and original_content_multimedia can be set  |
+--------------------------------+----------------------------+------------------------------+----------+-------------------------------------------------------------------------+
| /originating_system_audit      | `PARTY_IDENTIFIED`_        | originating_system_audit     | yes      |                                                                         |
+--------------------------------+----------------------------+------------------------------+----------+-------------------------------------------------------------------------+
| /feeder_system_audit           | `FEEDER_AUDIT_DETAILS`_    | feeder_system_audit          | no       |                                                                         |
+--------------------------------+----------------------------+------------------------------+----------+-------------------------------------------------------------------------+



FEEDER_AUDIT_DETAILS
---------------------
(see also https://specifications.openehr.org/releases/RM/latest/common.html#_feeder_audit_details_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit|system_id": "orig"
  }
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/subject|id": "1234-5678",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/subject|id_scheme": "UUID",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/subject|id_namespace": "EHR.NETWORK",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/subject|name": "Silvia Blake",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/subject/_identifier:0|id": "122",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/subject/_identifier:0|issuer": "issuer",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/subject/_identifier:0|assigner": "assigner",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/subject/_identifier:0|type": "type",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/provider|id": "1234-5678",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/provider|id_scheme": "UUID",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/provider|id_namespace": "EHR.NETWORK",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/provider|name": "Silvia Blake",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/provider/_identifier:0|id": "122",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/provider/_identifier:0|issuer": "issuer",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/provider/_identifier:0|assigner": "assigner",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/provider/_identifier:0|type": "type",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/location|id": "12342341",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/location|id_scheme": "NMC",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/location|id_namespace": "uk.org.nmc",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit/location|name": "Org 1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit|system_id": "orig",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit|version_id": "final",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/_feeder_audit/feeder_system_audit|time": "2021-12-21T16:02:58.0094262+01:00"
  }

+--------------+-----------------------+------------+----------+-------------------------------------------------------------+
| Flat Path    | Flat type             | RM Path    | Required | Note                                                        |
+==============+=======================+============+==========+=============================================================+
| \|system_id  | String                | system_id  | yes      |                                                             |
+--------------+-----------------------+------------+----------+-------------------------------------------------------------+
| \|version_id | String                | version_id | no       |                                                             |
+--------------+-----------------------+------------+----------+-------------------------------------------------------------+
| \|time       | String                | time.value | no       |                                                             |
+--------------+-----------------------+------------+----------+-------------------------------------------------------------+
| /subject     | `PARTY_PROXY`_        | subject    | no       | add /subject\|_type:"PARTY_SELF" to  set this to PARTY_SELF |
+--------------+-----------------------+------------+----------+-------------------------------------------------------------+
| /provider    | `PARTY_IDENTIFIED`_   | provider   | no       |                                                             |
+--------------+-----------------------+------------+----------+-------------------------------------------------------------+
| /location    | `PARTY_IDENTIFIED`_   | location   | no       |                                                             |
+--------------+-----------------------+------------+----------+-------------------------------------------------------------+

ACTIVITY
----------------
(see also https://specifications.openehr.org/releases/RM/latest/ehr.html#_activity_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/current_activity/dv_text": "DV_TEXT 45",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/current_activity/timing": "R4/2022-01-31T10:00:00+01:00/P3M",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/current_activity/timing|formalism": "timing"
  }
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/current_activity/dv_text": "DV_TEXT 45",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/current_activity/timing": "R4/2022-01-31T10:00:00+01:00/P3M",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/current_activity/timing|formalism": "timing",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/current_activity/action_archetype_id": "/openEHR-EHR-CLUSTER.conformance_action.v0/"

  }

+-----------------------+------------------+----------------------+-----------+------------------------------------------+
| Flat Path             | Flat type        | RM Path              | Required  | Note                                     |
+=======================+==================+======================+===========+==========================================+
| /timing               | `DV_PARSABLE`_   | timing               | no        |                                          |
+-----------------------+------------------+----------------------+-----------+------------------------------------------+
| /action_archetype_id  | STRING           | action_archetype_id  | no        | Will be set to /.*/ if not set explicit. |
+-----------------------+------------------+----------------------+-----------+------------------------------------------+


ISM_TRANSITION
--------------------
(see also https://specifications.openehr.org/releases/RM/latest/ehr.html#_activity_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/current_state|code": "532",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/current_state|value": "completed",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/current_state|terminology": "openehr"
  }
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/current_state|code": "532",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/current_state|value": "completed",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/current_state|terminology": "openehr",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/transition|code": "548",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/transition|value": "finish",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/transition|terminology": "openehr",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/careflow_step|code": "at0006",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/careflow_step|value": "transition",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/careflow_step|terminology": "local",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/ism_transition/_reason:0": "reason 1"

  }

+-----------------------+--------------------+----------------------+-----------+------------------------------------------+
| Flat Path             | Flat type          | RM Path              | Required  | Note                                     |
+=======================+====================+======================+===========+==========================================+
| /current_state        | `DV_CODED_TEXT`_   | current_state        | yes       |                                          |
+-----------------------+--------------------+----------------------+-----------+------------------------------------------+
| /transition           | `DV_CODED_TEXT`_   | transition           | no        |                                          |
+-----------------------+--------------------+----------------------+-----------+------------------------------------------+
| /careflow_step        | `DV_CODED_TEXT`_   | careflow_step        | no        |                                          |
+-----------------------+--------------------+----------------------+-----------+------------------------------------------+
| /_reason:i            | `DV_TEXT`_         | reason               | no        |                                          |
+-----------------------+--------------------+----------------------+-----------+------------------------------------------+

INSTRUCTION_DETAILS
--------------------
(see also https://specifications.openehr.org/releases/RM/latest/ehr.html#_instruction_details_class)


.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_instruction_details|path": "/content[openEHR-EHR-SECTION.conformance_section.v0]/items[openEHR-EHR-INSTRUCTION.conformance_instruction.v0]",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_instruction_details|composition_uid": "4cdc3017-d8c5-4cd3-9900-f3bb7171d006",
  "conformance-ehrbase.de.v0/conformance_section/conformance_action/_instruction_details|activity_id": "activities[at0001]"

  }

+--------------------+------------+----------------------+-----------+---------+
| Flat Path          | Flat type  | RM Path              | Required  | Note    |
+====================+============+======================+===========+=========+
| \|path             | STRING     | instruction_id.path  | yes       |         |
+--------------------+------------+----------------------+-----------+---------+
| \|composition_uid  | STRING     | instruction_id.id    | yes       |         |
+--------------------+------------+----------------------+-----------+---------+
| \|activity_id      | STRING     | activity_id          | yes       |         |
+--------------------+------------+----------------------+-----------+---------+



EVENT_CONTEXT
----------------
(see also https://specifications.openehr.org/releases/RM/latest/ehr.html#_event_context_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/context/start_time": "2021-12-21T14:19:31.649613+01:00",
  "conformance-ehrbase.de.v0/context/setting|code": "238",
  "conformance-ehrbase.de.v0/context/setting|value": "other care",
  "conformance-ehrbase.de.v0/context/setting|terminology": "openehr"
  }
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/context/_health_care_facility|id": "9091",
  "conformance-ehrbase.de.v0/context/_health_care_facility|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/context/_health_care_facility|id_namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/context/_health_care_facility|name": "Hospital",
  "conformance-ehrbase.de.v0/context/_participation:0|function": "requester",
  "conformance-ehrbase.de.v0/context/_participation:0|mode": "face-to-face communication",
  "conformance-ehrbase.de.v0/context/_participation:0|name": "Dr. Marcus Johnson",
  "conformance-ehrbase.de.v0/context/_participation:0|id": "199",
  "conformance-ehrbase.de.v0/context/_participation:0|id_scheme": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/context/_participation:0|id_namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/context/start_time": "2021-12-21T14:19:31.649613+01:00",
  "conformance-ehrbase.de.v0/context/_end_time": "2021-12-21T15:19:31.649613+01:00",
  "conformance-ehrbase.de.v0/context/_location": "2021-12-21T15:19:31.649613+01:00",
  "conformance-ehrbase.de.v0/context/setting|code": "238",
  "conformance-ehrbase.de.v0/context/setting|value": "other care",
  "conformance-ehrbase.de.v0/context/setting|terminology": "openehr"
  }

+-----------------+-------------------+----------------------------+----------+-------------------------+
| Flat Path       | Flat type         | RM Path                    | Required | Note                    |
+=================+===================+============================+==========+=========================+
| \|name          | String            | name                       | no       |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| \|id            | String            | external_ref.id.value      | no       |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| \|id_scheme     | String            | external_ref.id.scheme     | no       |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| \|id_namespace  | String            | external_ref.id.namespace  | (yes)    | required if id is set   |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| /_identifier:i  | `DV_IDENTIFIER`_  | identifiers                | no       |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+

OBJECT_REF
----------------
(see also https://specifications.openehr.org/releases/RM/latest/ehr.html#_event_context_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_guideline_id|type": "GUIDELINE",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_guideline_id|namespace": "HOSPITAL-NS",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_guideline_id|id": "3445",
  "conformance-ehrbase.de.v0/conformance_section/conformance_instruction/_guideline_id|id_scheme": "HOSPITAL-NS"
  }

+-----------------+-------------------+----------------------------+----------+-------------------------+
| Flat Path       | Flat type         | RM Path                    | Required | Note                    |
+=================+===================+============================+==========+=========================+
| \|type          | String            | type                       | yes      |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| \|id            | String            | id.value                   | yes      |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| \|scheme        | String            | id.scheme                  | yes      |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| \|namespace     | String            | namespace                  | yes      |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+

INTERVAL_EVENT
----------------
(see also https://specifications.openehr.org/releases/RM/latest/data_structures.html#_interval_event_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|magnitude": 65.9,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|unit": "unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/width": "P30D",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/math_function|code": "146",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/math_function|value": "mean",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/math_function|terminology": "openehr"
  }

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|magnitude": 65.9,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|unit": "unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0|sample_count": 5,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/width": "P30D",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/math_function|code": "146",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/math_function|value": "mean",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/math_function|terminology": "openehr"
  }

+-----------------+-------------------+----------------+-----------+---------+
| Flat Path       | Flat type         | RM Path        | Required  | Note    |
+=================+===================+================+===========+=========+
| /width          | `DV_DURATION`_    | width          | yes       |         |
+-----------------+-------------------+----------------+-----------+---------+
| /math_function  | `DV_CODED_TEXT`_  | math_function  | yes       |         |
+-----------------+-------------------+----------------+-----------+---------+
| \|sample_count  | INTEGER           | sample_count   | no        |         |
+-----------------+-------------------+----------------+-----------+---------+


POINT_EVENT
----------------
(see also https://specifications.openehr.org/releases/RM/latest/ehr.html#_event_context_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text": "DV_TEXT value",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/time": "2021-12-21T16:02:58.0094262+01:00"
  }

+--------------------+------------------+--------------------+-----------+---------+
| Flat Path          | Flat type        | RM Path            | Required  | Note    |
+====================+==================+====================+===========+=========+
| /time              | `DV_DATE_TIME`_  | time               | yes       |         |
+--------------------+------------------+--------------------+-----------+---------+


PARTY_PROXY 
-----------
(see also https://specifications.openehr.org/releases/RM/latest/common.html#_party_proxy_class )

See `PARTY_SELF`_ ; `PARTY_IDENTIFIED`_ and `PARTY_RELATED`_. 

 

PARTY_SELF
----------
(see also https://specifications.openehr.org/releases/RM/latest/common.html#_party_self_class)


.. code-block:: json

 {
  "ctx/composer_self": true,
  "conformance-ehrbase.de.v0/composer|id": "1234-5678",
  "conformance-ehrbase.de.v0/composer|id_scheme": "UUID",
  "conformance-ehrbase.de.v0/composer|id_namespace": "EHR.NETWORK"
  } 

+-----------------+-------------------+----------------------------+----------+-------------------------+
| Flat Path       | Flat type         | RM Path                    | Required | Note                    |
+=================+===================+============================+==========+=========================+
| \|id            | String            | external_ref.id.value      | no       |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| \|id_scheme     | Integer           | external_ref.id.scheme     | no       |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| \|id_namespace  | String            | external_ref.id.namespace  | (yes)    | required if id is set   |
+-----------------+-------------------+----------------------------+----------+-------------------------+

PARTY_IDENTIFIED 
----------------
(see also https://specifications.openehr.org/releases/RM/latest/common.html#_party_identified_class )

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/composer|name": "Silvia Blake"
  } 
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/composer|name": "Silvia Blake",
  "conformance-ehrbase.de.v0/composer|id": "1234-5678",
  "conformance-ehrbase.de.v0/composer|id_scheme": "UUID",
  "conformance-ehrbase.de.v0/composer|id_namespace": "EHR.NETWORK",
  "conformance-ehrbase.de.v0/composer/_identifier:0|id": "122",
  "conformance-ehrbase.de.v0/composer/_identifier:0|issuer": "issuer",
  "conformance-ehrbase.de.v0/composer/_identifier:0|assigner": "assigner",
  "conformance-ehrbase.de.v0/composer/_identifier:0|type": "type"
  } 

+-----------------+-------------------+----------------------------+----------+-------------------------+
| Flat Path       | Flat type         | RM Path                    | Required | Note                    |
+=================+===================+============================+==========+=========================+
| \|name          | String            | name                       | no       |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| \|id            | String            | external_ref.id.value      | no       |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| \|id_scheme     | Integer           | external_ref.id.scheme     | no       |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| \|id_namespace  | String            | external_ref.id.namespace  | (yes)    | required if id is set   |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| /_identifier:i  | `DV_IDENTIFIER`_  | identifiers                | no       |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+

	

PARTY_RELATED 
-------------
(see also https://specifications.openehr.org/releases/RM/latest/common.html#_party_related_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/composer|name": "Silvia Blake",
  "conformance-ehrbase.de.v0/composer/relationship|code" : "10",
  "conformance-ehrbase.de.v0/composer/relationship|value" : "mother",
  "conformance-ehrbase.de.v0/composer/relationship|terminology" : "openehr"

  } 
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/composer|name": "Silvia Blake",
  "conformance-ehrbase.de.v0/composer|id": "1234-5678",
  "conformance-ehrbase.de.v0/composer|id_scheme": "UUID",
  "conformance-ehrbase.de.v0/composer|id_namespace": "EHR.NETWORK",
  "conformance-ehrbase.de.v0/composer/relationship|code" : "10",
  "conformance-ehrbase.de.v0/composer/relationship|value" : "mother",
  "conformance-ehrbase.de.v0/composer/relationship|terminology" : "openehr",
  "conformance-ehrbase.de.v0/composer/_identifier:0|id": "122",
  "conformance-ehrbase.de.v0/composer/_identifier:0|issuer": "issuer",
  "conformance-ehrbase.de.v0/composer/_identifier:0|assigner": "assigner",
  "conformance-ehrbase.de.v0/composer/_identifier:0|type": "type"
  } 

+-----------------+-------------------+----------------------------+----------+-------------------------+
| Flat Path       | Flat type         | RM Path                    | Required | Note                    |
+=================+===================+============================+==========+=========================+
| \|name          | String            | name                       | no       |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| \|id            | String            | external_ref.id.value      | no       |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| \|id_scheme     | Integer           | external_ref.id.scheme     | no       |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| \|id_namespace  | String            | external_ref.id.namespace  | (yes)    | required if id is set   |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| /_identifier:i  | `DV_IDENTIFIER`_  | identifiers                | no       |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+
| /_relationship  | `DV_CODED_TEXT`_  | relationship               | (yes)    |                         |
+-----------------+-------------------+----------------------------+----------+-------------------------+


DV_TEXT
-------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_dv_text_class )

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text": "DV_TEXT value"
  } 
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text": "DV_TEXT value",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text|formatting": "plain",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_language|preferred_term": "English",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_encoding|code": "UTF-8",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_encoding|terminology": "IANA_character-sets",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_mapping:0|match": "=",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_mapping:0/target|terminology": "SNOMED-CT",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_mapping:0/target|code": "21794005",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_mapping:0/purpose|terminology": "openehr",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_mapping:0/purpose|code": "671",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_mapping:0/purpose|value": "research study"
  } 

+--------------+----------------------+-------------+----------+-------+
| Flat Path    | Flat type            | RM Path     | Required | Note  |
+==============+======================+=============+==========+=======+
|\|value       | String               | value       | yes      |       |
+--------------+----------------------+-------------+----------+-------+
| \|formatting | String               | formatting  | no       |       |
+--------------+----------------------+-------------+----------+-------+
| /_language   | `CODE_PHRASE`_       | language    | no       |       |
+--------------+----------------------+-------------+----------+-------+
| /_encoding   | `CODE_PHRASE`_       | encoding    | no       |       |
+--------------+----------------------+-------------+----------+-------+
| /_mapping:i  | `TERM_MAPPING`_      | mappings    | no       |       |
+--------------+----------------------+-------------+----------+-------+


CODE_PHRASE
-----------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_code_phrase_class )


.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_language|terminology": "ISO_639-1"
  }
.. code-block:: json 

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_language|preferred_term": "English"
  } 

+-------------------+------------+-----------------------+----------+-------+
| Flat Path         | Flat type  | RM Path               | Required | Note  |
+===================+============+=======================+==========+=======+
| \|code            | String     | code_string           | yes      |       |
+-------------------+------------+-----------------------+----------+-------+
| \|terminology     | String     | terminology_id.value  | yes      |       |
+-------------------+------------+-----------------------+----------+-------+
| \|preferred_term  | String     | preferred_term        | no       |       |
+-------------------+------------+-----------------------+----------+-------+


TERM_MAPPING
-------------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_term_mapping_class )

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_mapping:0|match": "=",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_mapping:0/target|terminology": "SNOMED-CT",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_mapping:0/target|code": "21794005"
  } 

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_mapping:0|match": "=",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_mapping:0/target|terminology": "SNOMED-CT",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_mapping:0/target|code": "21794005",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_mapping:0/purpose|terminology": "openehr",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_mapping:0/purpose|code": "671",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_text/_mapping:0/purpose|value": "research study"
  } 

+------------+----------------------+----------+----------+--------+
| Flat Path  | Flat type            | RM Path  | Required | Note   |
+============+======================+==========+==========+========+
| \|match    | String               | match    | yes      |        |
+------------+----------------------+----------+----------+--------+
| /target    | `CODE_PHRASE`_       | target   | yes      |        |
+------------+----------------------+----------+----------+--------+
| /purpose   | `DV_CODED_TEXT`_     | purpose  | no       |        |
+------------+----------------------+----------+----------+--------+


DV_CODED_TEXT 
--------------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_dv_coded_text_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text|value": "term1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text|code": "at0006",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text|terminology": "local"
  } 

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text|value": "term1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text|code": "at0006",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text|terminology": "local",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text|formatting": "plain",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text/_language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text/_language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text/_language|preferred_term": "English",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text/_encoding|code": "UTF-8",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text/_encoding|terminology": "IANA_character-sets",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text/_mapping:0|match": "=",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text/_mapping:0/target|terminology": "SNOMED-CT",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text/_mapping:0/target|code": "21794005",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text/_mapping:0/purpose|terminology": "openehr",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text/_mapping:0/purpose|code": "671",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_coded_text/_mapping:0/purpose|value": "research study"
  } 


+----------------+-----------------+-------------------------------------+----------+--------------------------------------------+
| Flat Path      | Flat type       | RM Path                             | Required | Note                                       |
+================+=================+=====================================+==========+============================================+
| \|code         | String          | defining_code.code_string           | yes      |                                            |
+----------------+-----------------+-------------------------------------+----------+--------------------------------------------+
| \|value        | String          | value                               | (yes)    | only required for external  terminologies  |
+----------------+-----------------+-------------------------------------+----------+--------------------------------------------+
| \|terminology  | String          | defining_code.terminology_id.value  | (yes)    | only required for external  terminologies  |
+----------------+-----------------+-------------------------------------+----------+--------------------------------------------+
| \|formatting   | String          | formatting                          | no       |                                            |
+----------------+-----------------+-------------------------------------+----------+--------------------------------------------+
| /_language     | `CODE_PHRASE`_  | language                            | no       |                                            |
+----------------+-----------------+-------------------------------------+----------+--------------------------------------------+
| /_encoding     | `CODE_PHRASE`_  | encoding                            | no       |                                            |
+----------------+-----------------+-------------------------------------+----------+--------------------------------------------+
| /_mapping:i    | `TERM_MAPPING`_ | mappings                            | no       |                                            |
+----------------+-----------------+-------------------------------------+----------+--------------------------------------------+

DV_ORDINAL
--------------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_dv_ordinal_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal|code": "at0015",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal|value": "value1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal|ordinal": 1
  }

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal|code": "at0015",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal|value": "value1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal|ordinal": 1,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal/_normal_range/lower|code": "at0015",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal/_normal_range/lower|value": "value1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal/_normal_range/lower|ordinal": 1,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal/_normal_range/upper|code": "at0015",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal/_normal_range/upper|value": "value1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal/_normal_range/upper|ordinal": 1,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal/_other_reference_ranges:0/lower|code": "at0016",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal/_other_reference_ranges:0/lower|value": "value2",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal/_other_reference_ranges:0/lower|ordinal": 2,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal/_other_reference_ranges:0|upper_unbounded": true,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal/_other_reference_ranges:0|upper_included": false,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ordinal/_other_reference_ranges:0/meaning": "high"
  }


+-----------------------------+----------------------------------+----------------------------------------+----------+--------------------------------------------------+
| Flat Path                   | Flat type                        | RM Path                                | Required | Note                                             |
+=============================+==================================+========================================+==========+==================================================+
| \|code                      | String                           | symbol.defining_code.code_string       | Yes      |                                                  |
+-----------------------------+----------------------------------+----------------------------------------+----------+--------------------------------------------------+
| \|value                     | String                           | symbol.value                           | (Yes)    | my be left out if symbol is defined in template  |
+-----------------------------+----------------------------------+----------------------------------------+----------+--------------------------------------------------+
| \|ordinal                   | Integer                          | value                                  | (Yes)    | my be left out if symbol is defined in template  |
+-----------------------------+----------------------------------+----------------------------------------+----------+--------------------------------------------------+
| /_normal_range              | `DV_INTERVAL`_ <DV_ORDINAL>      | normal_range                           | no       |                                                  |
+-----------------------------+----------------------------------+----------------------------------------+----------+--------------------------------------------------+
| /_other_reference_ranges:i  | `REFERENCE_RANGE`_ <DV_ORDINAL>  | _other_reference_ranges                | no       |                                                  |
+-----------------------------+----------------------------------+----------------------------------------+----------+--------------------------------------------------+

DV_BOOLEAN 
--------------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_dv_boolean_class)

.. code-block:: json

 {
    "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_boolean": true
  }


+-----------------------------+----------------------------------+----------------------------------------+----------+--------------------------------------------------+
| Flat Path                   | Flat type                        | RM Path                                | Required | Note                                             |
+=============================+==================================+========================================+==========+==================================================+
|                             | Boolean                          | value                                  | Yes      |                                                  |
+-----------------------------+----------------------------------+----------------------------------------+----------+--------------------------------------------------+

DV_URI 
--------------
(see also https://specifications.openehr.org/releases/RM/Release-1.0.4/data_types.html#_dv_uri_class)

.. code-block:: json

 {
     "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_uri": "https://www.google.com/"
  }


+-----------------------------+----------------------------------+----------------------------------------+----------+--------------------------------------------------+
| Flat Path                   | Flat type                        | RM Path                                | Required | Note                                             |
+=============================+==================================+========================================+==========+==================================================+
|                             | String                           | value                                  | Yes      |                                                  |
+-----------------------------+----------------------------------+----------------------------------------+----------+--------------------------------------------------+

DV_EHR_URI 
--------------
(see also https://specifications.openehr.org/releases/RM/Release-1.0.4/data_types.html#_dv_ehr_uri_class)

.. code-block:: json

 {
    "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_ehr_uri": "ehr://766b3873-0762-4921-91e2-838c8546d47f"
  }


+-----------------------------+----------------------------------+----------------------------------------+----------+--------------------------------------------------+
| Flat Path                   | Flat type                        | RM Path                                | Required | Note                                             |
+=============================+==================================+========================================+==========+==================================================+
|                             | String                           | value                                  | Yes      |                                                  |
+-----------------------------+----------------------------------+----------------------------------------+----------+--------------------------------------------------+


DV_IDENTIFIER  
--------------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_dv_quantity_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_identifier|id": "A123"
  } 

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_identifier|id": "A123",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_identifier|issuer": "Issuer",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_identifier|assigner": "Assigner",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_identifier|type": "Prescription"
  } 


+-----------------------------+----------------------------------+--------------------------+----------+---------------------------------------+
| Flat Path                   | Flat type                        | RM Path                  | Required | Note                                  |
+=============================+==================================+==========================+==========+=======================================+
| \|id                        | String                           | id                       | Yes      | For the input \|id might be left out. |
+-----------------------------+----------------------------------+--------------------------+----------+---------------------------------------+
| \|issuer                    | String                           | issuer                   | no       |                                       |
+-----------------------------+----------------------------------+--------------------------+----------+---------------------------------------+
| \|assigner                  | String                           | assigner                 | no       |                                       |
+-----------------------------+----------------------------------+--------------------------+----------+---------------------------------------+
| \|type                      | String                           | type                     | no       |                                       |
+-----------------------------+----------------------------------+--------------------------+----------+---------------------------------------+





DV_QUANTITY 
--------------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_dv_quantity_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|magnitude": 65.9,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|unit": "unit"
  } 

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|magnitude": 65.9,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|magnitude_status": "~",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|normal_status": "N",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|accuracy": 50.5,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|accuracy_is_percent": true,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|precision": 1,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|unit": "unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|units_system": "units_system",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity|units_display_name": "units_display_name",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_normal_range/lower|magnitude": 20.5,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_normal_range/lower|unit": "unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_normal_range/upper|magnitude": 66.6,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_normal_range/upper|unit": "unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/lower|magnitude": 70.5,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/lower|unit": "unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/upper|magnitude": 77.6,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/upper|unit": "unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/meaning|value": "very high",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/meaning|code": "260360000",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/meaning|terminology": "SNOMED-CT"
  } 


+-----------------------------+------------------------------------+--------------------------+----------+----------------------------+
| Flat Path                   | Flat type                          | RM Path                  | Required | Note                       |
+=============================+====================================+==========================+==========+============================+
| \|magnitude                 | String                             | magnitude                | yes      |                            |
+-----------------------------+------------------------------------+--------------------------+----------+----------------------------+
| \|unit                      | Real                               | unit                     | yes      |                            |
+-----------------------------+------------------------------------+--------------------------+----------+----------------------------+
| \|magnitude_status          | String                             | magnitude_status         | no       | ValueSet (",>,>=,<,<=,~)   |
+-----------------------------+------------------------------------+--------------------------+----------+----------------------------+
| \|normal_status             | String                             | normal_status            | no       | ValueSet normal_status     |
+-----------------------------+------------------------------------+--------------------------+----------+----------------------------+
| \|accuracy                  | Real                               | accuracy                 | no       |                            |
+-----------------------------+------------------------------------+--------------------------+----------+----------------------------+
| \|accuracy_is_percent       | Boolean                            | accuracy_is_percent      | no       |                            |
+-----------------------------+------------------------------------+--------------------------+----------+----------------------------+
| /_normal_range              | `DV_INTERVAL`_ <DV_QUANTITY>       | normal_range             | no       |                            |
+-----------------------------+------------------------------------+--------------------------+----------+----------------------------+
| /_other_reference_ranges:i  | `REFERENCE_RANGE`_ <DV_QUANTITY>   | _other_reference_ranges  | no       |                            |
+-----------------------------+------------------------------------+--------------------------+----------+----------------------------+


DV_PROPORTION 
--------------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_dv_proportion_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion|numerator": 20.5,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion|denominator": 12.4,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion|type": 0
  } 

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion|numerator": 20.5,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion|denominator": 12.4,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion|type": 0,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion": 1.6532258064516128,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion|magnitude_status": "~",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion|normal_status": "N",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion|accuracy": 50.5,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion|accuracy_is_percent": true,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion|precision": 1,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_normal_range/lower|numerator": 20.5,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_normal_range/lower|denominator": 12.4,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_normal_range/lower|type": 0,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_normal_range/lower": 1.6532258064516128,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_normal_range/upper|numerator": 25.5,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_normal_range/upper|denominator": 12.4,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_normal_range/upper|type": 0,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_normal_range/upper": 2.0564516129032255,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_other_reference_ranges:0/lower|numerator": 20.5,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_other_reference_ranges:0/lower|denominator": 18.4,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_other_reference_ranges:0/lower|type": 0,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_other_reference_ranges:0/lower": 1.1141304347826089,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_other_reference_ranges:0/upper|numerator": 25.5,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_other_reference_ranges:0/upper|denominator": 12.4,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_other_reference_ranges:0/upper|type": 0,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_other_reference_ranges:0/upper": 2.0564516129032255,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_proportion/_other_reference_ranges:0/meaning": "high"
  } 


+-----------------------------+-------------------------------------+--------------------------+----------+---------------------------+
| Flat Path                   | Flat type                           | RM Path                  | Required | Note                      |
+=============================+=====================================+==========================+==========+===========================+
| \|numerator                 | Real                                | numerator                | yes      |                           |
+-----------------------------+-------------------------------------+--------------------------+----------+---------------------------+
| \|denominator               | Real                                | denominator              | yes      |                           |
+-----------------------------+-------------------------------------+--------------------------+----------+---------------------------+
| \|type                      | Integer                             | type                     | yes      | ValueSet proportion_kind  |
+-----------------------------+-------------------------------------+--------------------------+----------+---------------------------+
|                             | Real                                | magnitude                | no       | calculated on output      |
+-----------------------------+-------------------------------------+--------------------------+----------+---------------------------+
| \|magnitude_status          | String                              | magnitude_status         | no       | ValueSet (",>,>=,<,<=,~)  |
+-----------------------------+-------------------------------------+--------------------------+----------+---------------------------+
| \|normal_status             | String                              | normal_status            | no       | ValueSet normal_status    |
+-----------------------------+-------------------------------------+--------------------------+----------+---------------------------+
| /_normal_range              | `DV_INTERVAL`_ <DV_PROPORTION>      | normal_range             | no       |                           |
+-----------------------------+-------------------------------------+--------------------------+----------+---------------------------+
| /_other_reference_ranges:i  | `REFERENCE_RANGE`_ <DV_PROPORTION>  | _other_reference_ranges  | no       |                           |
+-----------------------------+-------------------------------------+--------------------------+----------+---------------------------+

DV_COUNT  
--------------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_dv_count_class)

.. code-block:: json

 {
   "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_count": 7
  } 

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_count": 7,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_count|magnitude_status": "~",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_count|normal_status": "N",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_count|accuracy": 50.5,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_count|accuracy_is_percent": true,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_count/_normal_range/lower": 1,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_count/_normal_range/upper": 8,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_count/_other_reference_ranges:0/lower": 8,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_count/_other_reference_ranges:0/upper": 10,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_count/_other_reference_ranges:0/meaning": "high"
  } 


+-----------------------------+-------------------------------------+--------------------------+----------+----------------------------+
| Flat Path                   | Flat type                           | RM Path                  | Required | Note                       |
+=============================+=====================================+==========================+==========+============================+
|                             | Integer                             | magnitude                | Yes      |                            |
+-----------------------------+-------------------------------------+--------------------------+----------+----------------------------+
| \|magnitude_status          | String                              | magnitude_status         | no       | ValueSet (",>,>=,<,<=,~)   |
+-----------------------------+-------------------------------------+--------------------------+----------+----------------------------+
| \|normal_status             | String                              | normal_status            | no       | ValueSet normal_status     |
+-----------------------------+-------------------------------------+--------------------------+----------+----------------------------+
| /_normal_range              | `DV_INTERVAL`_ <DV_COUNT>           | normal_range             | no       |                            |
+-----------------------------+-------------------------------------+--------------------------+----------+----------------------------+
| /_other_reference_ranges:i  | `REFERENCE_RANGE`_ <DV_COUNT>       | _other_reference_ranges  | no       |                            |
+-----------------------------+-------------------------------------+--------------------------+----------+----------------------------+

DV_DATE    
--------------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_dv_date_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date": "2022-01-12"
  } 

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date": "2022-01-12",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date|magnitude_status": "~",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date|normal_status": "N",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date/_accuracy": "P2D",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date/_normal_range/lower": "2022-01-12",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date/_normal_range/upper": "2022-02-12",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date/_other_reference_ranges:0/lower": "2022-02-12",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date/_other_reference_ranges:0/upper": "2022-03-12",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date/_other_reference_ranges:0/meaning": "high"
  } 


+-----------------------------+-------------------------------+--------------------------+----------+----------------------------+
| Flat Path                   | Flat type                     | RM Path                  | Required | Note                       |
+=============================+===============================+==========================+==========+============================+
|                             | String                        | value                    | Yes      | ISO8601 date               |
+-----------------------------+-------------------------------+--------------------------+----------+----------------------------+
| /_accuracy                  | `DV_DURATION`_                | accuracy                 | no       |                            |
+-----------------------------+-------------------------------+--------------------------+----------+----------------------------+
| \|magnitude_status          | String                        | magnitude_status         | no       | ValueSet (",>,>=,<,<=,~)   |
+-----------------------------+-------------------------------+--------------------------+----------+----------------------------+
| \|normal_status             | String                        | normal_status            | no       | ValueSet normal_status     |
+-----------------------------+-------------------------------+--------------------------+----------+----------------------------+
| /_normal_range              | `DV_INTERVAL`_ <DV_DATE>      | normal_range             | no       |                            |
+-----------------------------+-------------------------------+--------------------------+----------+----------------------------+
| /_other_reference_ranges:i  | `REFERENCE_RANGE`_ <DV_DATE>  | _other_reference_ranges  | no       |                            |
+-----------------------------+-------------------------------+--------------------------+----------+----------------------------+

DV_DATE_TIME    
--------------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_dv_date_class)

.. code-block:: json

 {
    "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date_time": "2022-01-12T13:22:34.000868+01:00"
  } 

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date_time": "2022-01-12T13:22:34.000868+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date_time|magnitude_status": "~",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date_time|normal_status": "N",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date_time/_accuracy": "P2DT9H52M",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date_time/_normal_range/lower": "2022-01-12T13:22:34.000868+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date_time/_normal_range/upper": "2022-02-12T13:22:34.000868+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date_time/_other_reference_ranges:0/lower": "2022-02-12T13:22:34.000868+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date_time/_other_reference_ranges:0/upper": "2022-03-12T13:22:34.000868+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date_time/_other_reference_ranges:0/meaning": "high"
  } 


+-----------------------------+------------------------------------+--------------------------+----------+----------------------------+
| Flat Path                   | Flat type                          | RM Path                  | Required | Note                       |
+=============================+====================================+==========================+==========+============================+
|                             | String                             | value                    | Yes      | ISO8601 date               |
+-----------------------------+------------------------------------+--------------------------+----------+----------------------------+
| /_accuracy                  | `DV_DURATION`_                     | accuracy                 | no       |                            |
+-----------------------------+------------------------------------+--------------------------+----------+----------------------------+
| \|magnitude_status          | String                             | magnitude_status         | no       | ValueSet (",>,>=,<,<=,~)   |
+-----------------------------+------------------------------------+--------------------------+----------+----------------------------+
| \|normal_status             | String                             | normal_status            | no       | ValueSet normal_status     |
+-----------------------------+------------------------------------+--------------------------+----------+----------------------------+
| /_normal_range              | `DV_INTERVAL`_ <DV_DATE_TIME>      | normal_range             | no       |                            |
+-----------------------------+------------------------------------+--------------------------+----------+----------------------------+
| /_other_reference_ranges:i  | `REFERENCE_RANGE`_ <DV_DATE_TIME>  | _other_reference_ranges  | no       |                            |
+-----------------------------+------------------------------------+--------------------------+----------+----------------------------+



DV_TIME    
--------------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_dv_date_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_date": "2022-01-12"
  } 

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_time": "13:22:34.000868+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_time|magnitude_status": "~",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_time|normal_status": "N",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_time/_accuracy": "PT9H52M",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_time/_normal_range/lower": "13:22:34.000868+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_time/_normal_range/upper": "14:22:34.000868+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_time/_other_reference_ranges:0/lower": "14:10:34.000868+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_time/_other_reference_ranges:0/upper": "15:22:34.000868+01:00",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_time/_other_reference_ranges:0/meaning": "high"
  } 


+-----------------------------+-------------------------------+--------------------------+----------+----------------------------+
| Flat Path                   | Flat type                     | RM Path                  | Required | Note                       |
+=============================+===============================+==========================+==========+============================+
|                             | String                        | value                    | Yes      | ISO8601 date               |
+-----------------------------+-------------------------------+--------------------------+----------+----------------------------+
| /_accuracy                  | `DV_DURATION`_                | accuracy                 | no       |                            |
+-----------------------------+-------------------------------+--------------------------+----------+----------------------------+
| \|magnitude_status          | String                        | magnitude_status         | no       | ValueSet (",>,>=,<,<=,~)   |
+-----------------------------+-------------------------------+--------------------------+----------+----------------------------+
| \|normal_status             | String                        | normal_status            | no       | ValueSet normal_status     |
+-----------------------------+-------------------------------+--------------------------+----------+----------------------------+
| /_normal_range              | `DV_INTERVAL`_ <DV_TIME>      | normal_range             | no       |                            |
+-----------------------------+-------------------------------+--------------------------+----------+----------------------------+
| /_other_reference_ranges:i  | `REFERENCE_RANGE`_ <DV_TIME>  | _other_reference_ranges  | no       |                            |
+-----------------------------+-------------------------------+--------------------------+----------+----------------------------+


DV_DURATION   
--------------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_dv_duration_class)

.. code-block:: json

 {
   "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_duration": "P2DT11H33M"
  } 

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_duration": "P2DT11H33M",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_duration|magnitude_status": "~",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_duration|normal_status": "N",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_duration|accuracy": 50.5,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_duration|accuracy_is_percent": true,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_duration/_normal_range/lower": "P2DT11H33M",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_duration/_normal_range/upper": "P2DT12H33M",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_duration/_other_reference_ranges:0/lower": "P2DT11H33M",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_duration/_other_reference_ranges:0/upper": "P2DT15H33M",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_duration/_other_reference_ranges:0/meaning": "high"
  } 


+-----------------------------+-----------------------------------+--------------------------+----------+----------------------------+
| Flat Path                   | Flat type                         | RM Path                  | Required | Note                       |
+=============================+===================================+==========================+==========+============================+
|                             | String                            | value                    | Yes      | ISO8601 duration           |
+-----------------------------+-----------------------------------+--------------------------+----------+----------------------------+
| \|accuracy                  | Real                              | accuracy                 | no       |                            |
+-----------------------------+-----------------------------------+--------------------------+----------+----------------------------+
| accuracy_is_percent         | Boolean                           | accuracy_is_percent      | no       |                            |
+-----------------------------+-----------------------------------+--------------------------+----------+----------------------------+
| \|magnitude_status          | String                            | magnitude_status         | no       | ValueSet (",>,>=,<,<=,~)   |
+-----------------------------+-----------------------------------+--------------------------+----------+----------------------------+
| \|normal_status             | String                            | normal_status            | no       | ValueSet normal_status     |
+-----------------------------+-----------------------------------+--------------------------+----------+----------------------------+
| /_normal_range              | `DV_INTERVAL`_ <DV_DURATION>      | normal_range             | no       |                            |
+-----------------------------+-----------------------------------+--------------------------+----------+----------------------------+
| /_other_reference_ranges:i  | `REFERENCE_RANGE`_ <DV_DURATION>  | _other_reference_ranges  | no       |                            |
+-----------------------------+-----------------------------------+--------------------------+----------+----------------------------+


REFERENCE_RANGE  
-----------------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_reference_range_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/lower|magnitude": 70.5,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/lower|unit": "unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/upper|magnitude": 77.6,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/upper|unit": "unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/meaning|value": "high"
  } 

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/lower|magnitude": 70.5,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/lower|unit": "unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0|upper_unbounded": true,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0|upper_included": false,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/meaning|value": "very high",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/meaning|code": "260360000",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:0/meaning|terminology": "SNOMED-CT",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:1|lower_unbounded": true,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:1|lower_included": false,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:1/upper|magnitude": 77.6,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:1/upper|unit": "unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:1/meaning|value": "very high",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:1/meaning|code": "260360000",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_quantity/_other_reference_ranges:1/meaning|terminology": "SNOMED-CT"
  } 


+--------------------+--------------+------------------------+----------+--------------------+
| Flat Path          | Flat type    | RM Path                | Required | Note               |
+====================+==============+========================+==========+====================+
| /lower             | T            | range.lower            | no       |                    |
+--------------------+--------------+------------------------+----------+--------------------+
| /upper             | T            | range.upper            | no       |                    |
+--------------------+--------------+------------------------+----------+--------------------+
| \|lower_unbounded  | Boolean      | range.lower_unbounded  | no       | defaults to false  |
+--------------------+--------------+------------------------+----------+--------------------+
| \|upper_unbounded  | Boolean      | range.upper_unbounded  | no       | defaults to false  |
+--------------------+--------------+------------------------+----------+--------------------+
| \|lower_included   | Boolean      | range.lower_included   | no       |  defaults to true  |
+--------------------+--------------+------------------------+----------+--------------------+
| \|upper_included   | Boolean      | range.upper_included   | no       |  defaults to true  |
+--------------------+--------------+------------------------+----------+--------------------+
| \meaning           | `DV_TEXT`_   | meaning                | yes      |                    |
+--------------------+--------------+------------------------+----------+--------------------+


DV_PARSABLE  
-----------------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_dv_parsable_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_parsable": "Formal instructions on carrying out the procedure...",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_parsable|formalism": "GLIF 1.0"

  } 

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_parsable": "Formal instructions on carrying out the procedure...",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_parsable|formalism": "GLIF 1.0",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_parsable/_language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_parsable/_language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_parsable/_charset|code": "UTF-8",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_parsable/_charset|terminology": "IANA_character-sets"
  } 


+--------------+-----------------+------------+----------+---------+
| Flat Path    | Flat type       | RM Path    | Required | Note    |
+==============+=================+============+==========+=========+
| \|value      | String          | value      | Yes      |         |
+--------------+-----------------+------------+----------+---------+
| \|formalism  | String          | formalism  | Yes      |         |
+--------------+-----------------+------------+----------+---------+
| /_charset    | `CODE_PHRASE`_  | charset    | no       |         |
+--------------+-----------------+------------+----------+---------+
| /_language   | `CODE_PHRASE`_  | language   | no       |         |
+--------------+-----------------+------------+----------+---------+

DV_MULTIMEDIA   
-----------------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_dv_multimedia_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia": "http://med.tube.com/sample",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia|mediatype": "video/H261",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia|size": 504903212
  } 

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia": "http://med.tube.com/sample",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia|mediatype": "video/H261",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia|size": 504903212,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia|compression_algorithm": "zlib",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia|alternatetext": "alternate text",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia|integrity_check": "b90360558e5420cef47015b1afbd70a156f940afa470b0515f95eacc2edcef6a",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia|integrity_check_algorithm": "SHA-256",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia/_thumbnail|data": "Z2hnZ2pnamdnag==",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia/_thumbnail|mediatype": "image/png",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia/_thumbnail|size": 504,
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia/_language|code": "en",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia/_language|terminology": "ISO_639-1",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia/_charset|code": "UTF-8",
  "conformance-ehrbase.de.v0/conformance_section/conformance_observation/any_event:0/dv_multimedia/_charset|terminology": "IANA_character-sets"
  } 


+------------------------------+--------------------+------------------------------------+----------+----------------------------------------------+
| Flat Path                    | Flat type          | RM Path                            | Required | Note                                         |
+==============================+====================+====================================+==========+==============================================+
|                              | String             | uri.value                          | no       |                                              |
+------------------------------+--------------------+------------------------------------+----------+----------------------------------------------+
| \|media_type                 | String             | media_type.code_string             | Yes      | ValueSet (IANA_media-types)                  |
+------------------------------+--------------------+------------------------------------+----------+----------------------------------------------+
| \|size                       | Integer            | size                               | Yes      |                                              |
+------------------------------+--------------------+------------------------------------+----------+----------------------------------------------+
| \|alternatetext              | String             | alternate_text                     | no       |                                              |
+------------------------------+--------------------+------------------------------------+----------+----------------------------------------------+
| \|compression_algorithm      | String             | compression_algorithm.code_string  | no       | ValueSet (openehr_compression_algorithms)    |
+------------------------------+--------------------+------------------------------------+----------+----------------------------------------------+
| \|integrity_check_algorithm  | String             | integrity_check_algorithm          | no       | ValueSet (openehr_integrity_check_algorithms)|
+------------------------------+--------------------+------------------------------------+----------+----------------------------------------------+
| \|integrity_check            | String             | integrity_check                    | no       |                                              |
+------------------------------+--------------------+------------------------------------+----------+----------------------------------------------+
| \|data                       | String             | dta                                | no       |                                              |
+------------------------------+--------------------+------------------------------------+----------+----------------------------------------------+
| /_thumbnail                  | `DV_MULTIMEDIA`_   | thumbnail                          | no       |                                              |
+------------------------------+--------------------+------------------------------------+----------+----------------------------------------------+
| /_charset                    | `CODE_PHRASE`_     | charset                            | no       |                                              |
+------------------------------+--------------------+------------------------------------+----------+----------------------------------------------+
| /_language                   | `CODE_PHRASE`_     | language                           | no       |                                              |
+------------------------------+--------------------+------------------------------------+----------+----------------------------------------------+


DV_INTERVAL
------------
(see also https://specifications.openehr.org/releases/RM/latest/data_types.html#_dv_interval_class)

.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_interval/any_event:0/interval_dv_quantity/lower|magnitude": 72.83,
  "conformance-ehrbase.de.v0/conformance_section/conformance_interval/any_event:0/interval_dv_quantity/lower|unit": "Unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_interval/any_event:0/interval_dv_quantity/upper|magnitude": 80.83,
  "conformance-ehrbase.de.v0/conformance_section/conformance_interval/any_event:0/interval_dv_quantity/upper|unit": "Unit"
  }
.. code-block:: json

 {
  "conformance-ehrbase.de.v0/conformance_section/conformance_interval/any_event:0/interval_dv_quantity/lower|magnitude": 72.83,
  "conformance-ehrbase.de.v0/conformance_section/conformance_interval/any_event:0/interval_dv_quantity/lower|unit": "Unit",
  "conformance-ehrbase.de.v0/conformance_section/conformance_interval/any_event:0/interval_dv_quantity|lower_included": false,
  "conformance-ehrbase.de.v0/conformance_section/conformance_interval/any_event:0/interval_dv_quantity|upper_unbounded": true,
  "conformance-ehrbase.de.v0/conformance_section/conformance_interval/any_event:0/interval_dv_quantity|upper_included": false
  }

+--------------------+------------+--------------------+-----------+--------------------------------------------+
| Flat Path          | Flat type  | RM Path            | Required  | Note                                       |
+====================+============+====================+===========+============================================+
| /lower             | T          | lower              | no        |                                            |
+--------------------+------------+--------------------+-----------+--------------------------------------------+
| /upper             | T          | upper              | no        |                                            |
+--------------------+------------+--------------------+-----------+--------------------------------------------+
| \|lower_unbounded  | BOOLEAN    | \|lower_unbounded  | no        | defaults to false. only in output if true  |
+--------------------+------------+--------------------+-----------+--------------------------------------------+
| \|upper_unbounded  | BOOLEAN    | upper_unbounded    | no        | defaults to false, only in output if true  |
+--------------------+------------+--------------------+-----------+--------------------------------------------+
| \|lower_included   | BOOLEAN    | lower_included     | no        | defaults to true. only in output if false  |
+--------------------+------------+--------------------+-----------+--------------------------------------------+
| \|upper_included   | BOOLEAN    | upper_included     | no        | defaults to true. only in output if false  |
+--------------------+------------+--------------------+-----------+--------------------------------------------+


