-------------------------

**Clients**

-   A client has connected to a server and fetched a patient's allergies using `GET /AllergyIntolerance?patient=[id]`.

**Servers**

- A server is capable of returning a patient's allergies using `GET /AllergyIntolerance?patient=[id]`.
-   A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
-   A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.
-------------------------

**Clients**

-   A client has connected to a server and fetched all of a patient's Assessment and Plan of Treatment information using `GET /CarePlan?patient=[id]&category=assess-plan`.
-   A client has connected to a server and fetched all of a patient's Assessment and Plan of Treatment information over a specified time period using `GET /CarePlan?patient=[id]&category=assess-plan&date=[date]`.


- A client **SHOULD** be capable of connecting to a server and fetching all of a patient's active Assessment and Plan of Treatment information using `GET /CarePlan?patient=[id]&category=assess-plan&status=active`.
- A client **SHOULD** be capable of connecting to a server and fetching all of a patient's active Assessment and Plan of Treatment information over a specified time period using `GET /CarePlan?patient=[id]&category=assess-plan&status=active&date=[date]`.

**Servers**

-  A server is capable of returning all of a patient's Assessment and Plan of Treatment information using `GET /CarePlan?patient=[id]&category=assess-plan`.
- A server is capable of returning a patient's Assessment and Plan of Treatment information over a specified time period using `GET /CarePlan?patient=[id]&category=assess-plan&date=[date]`.


- A server **SHOULD** be capable returning all of a patient's active Assessment and Plan of Treatment information using `GET /CarePlan?patient=[id]&category=assess-plan&status=active`.
- A server **SHOULD** be capable returning a patient's active Assessment and Plan of Treatment information over a specified time period using `GET /CarePlan?patient=[id]&category=assess-plan&status=active&date=[date]`.


- A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
- A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.

-------------------------

**Clients**

-  A client is able to connect to a server and fetch all current care team members for a patient using `GET[base]/CareTeam?patient=[id]&status=active`

**Servers**

-  A server is capable of returning a patient's current care team members using `GET[base]/CareTeam?patient=[id]&status=active`


- A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
- A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.

-------------------------

**Clients**

- A client connected to a server and fetched all problems and health concerns for a patient, including current as well as historical problems and health concerns using `GET/Condition?patient=[id]`.


**Servers**

- A server is capable of returning a patient's conditions list using `GET/Condition?patient=[id]`.

- A server **SHOULD** be capable returning all of a patient's active problems and health concerns using 'GET /Condition?patient=[id]&clinicalstatus=active,recurrance,remission'
- A server **SHOULD** be capable returning all of a patient's problems or all of patient's health concerns using 'GET /Condition?patient=[id]&&category=[problem|health-concern]'

- A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
- A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.

-------------------------

**Clients**

-  A client has connected to a server and fetched all Unique device identifier(s)(UDI)for a patient’s implantable device(s)using `GET /Device?patient=[id]`.


**Servers**

- A server is capable of returning all Unique device identifier(s)(UDI) for a patient’s implantable device(s) using `GET /Device?patient=[id]`.


- A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
- A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.
-------------------------

**Clients**

-  A client has connected to a server and fetched all of a patient's laboratory diagnostic reports by searching by category using `GET [base]/DiagnosticReport?patient=[id]&category=LAB`.
- A client has connected to a server and fetched all of a patient's laboratory diagnostic reports searching by category code and date range using `GET [base]/DiagnosticReport?patient=[id]&category=LAB&date=[date]{&date=[date]}`.
- A client has connected to a server and fetched all of all of a patient's laboratory diagnostic reports searching by category and code using `GET [base]/DiagnosticReport?patient=[id]&category=LAB&code=[LOINC]`.


- A client **SHOULD** be capable of connecting to a server and fetching any of a patient's laboratory diagnostic reports searching by category and one or more codes and date range using `GET [base]/DiagnosticReport?patient=[id]&category=LAB&code=[LOINC1{,LOINC2,LOINC3,...}]&date=[date]{&date=[date]}`.

**Servers**

- A server is capable of returning all of a patient's laboratory diagnostic reports queried by category using `GET [base]/DiagnosticReport?patient=[id]&category=LAB`.
- A server is capable of returning all of a patient's laboratory diagnostic reports queried by category code and date range using `GET [base]/DiagnosticReport?patient=[id]&category=LAB&date=[date]{&date=[date]}`.
- A server is capable of returning all of a patient's laboratory diagnostic reports queried by category and code using `GET [base]/DiagnosticReport?patient=[id]&category=LAB&code=[LOINC]`.


- A server **SHOULD** be capable of returning all of a patient's laboratory diagnostic reports queried by category and one or more codes and date range using `GET [base]/DiagnosticReport?patient=[id]&category=LAB&code=[LOINC1{,LOINC2,LOINC3,...}]&date=[date]{&date=[date]}`.


- A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
- A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.


-------------------------

**Clients**

-  A client has connected to a server and fetched all of a patient's goals using `GET [base]/Goal?patient=[id]`.
- A client has connected to a server and fetched all of a patient's goals over a specified time period using `GET [base]/Goal?patient=[id]&date=[date]{&date=[date]}.`


**Servers**

- A server is capable of returning all of a patient's goals using `GET [base]/Goal?patient=[id]`.
- A server is capable of returning all of all of a patient's goals over a specified time period using `GET [base]/Goal?patient=[id]&date=[date]{&date=[date]}`.


- A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
- A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.


-------------------------

**Clients**

-  A client has connected to a server and fetched all immunizations for a patient using `GET /Immunization?patient=[id]`.


**Servers**

- A server is capable of returning a all immunizations for a patient using `GET /Immunization?patient=[id]`.


- A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
- A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.
-------------------------

**Clients**

-  A client has connected to a server and fetched a location by name using `GET [base]/Location?name=[string]`
- A client has connected to a server and fetched a location by address using `GET [base]/Location?address=[string]`



**Servers**

- A server is capable of returning a location by name using `GET [base]/Location?name=[string]`
- A server is capable of returning a location by address using `GET [base]/Location?address=[string]`


-   A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
-   A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.


-------------------------
**Clients**

-  A client has connected to a server and fetched a patient's medications using:

1. `GET /MedicationRequest?patient=[id]` or
1. `GET /MedicationRequest?patient=[id]&_include=MedicationRequest:medication`

**Servers**

- A server is capable of returning a patient's medications using one of or both

1. `GET /MedicationRequest?patient=[id]`
1. `GET /MedicationRequest?patient=[id]&_include=MedicationRequest:medication`


- A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
- A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.

-------------------------

**Clients**

-  A client has connected to a server and fetched a patient's medications using:

1. `GET /MedicationStatement?patient=[id]` or
1. `GET /MedicationStatement?patient=[id]&_include=MedicationStatement:medication`

**Servers**

- A server is capable of returning a patient's medications using one of or both

1. `GET /MedicationStatement?patient=[id]`
1. `GET /MedicationStatement?patient=[id]&_include=MedicationStatement:medication`


- A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
- A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.


-------------------------

**Clients**

-  A client has connected to a server and fetched all of a patient's laboratory results by searching by category using `GET [base]/Observation?patient=[id]&category=laboratory`.
- A client has connected to a server and fetched all of a patient's laboratory results searching by category code and date range using `GET [base]/Observation?patient=[id]&category=laboratory&date=[date]{&date=[date]}`.
- A client has connected to a server and fetched all of all of a patient's laboratory results searching by category and code using `GET [base]/Observation?patient=[id]&category=laboratory&code=[LOINC]`.


 - A client **SHOULD** be capable of connecting to a server and fetching any of a patient's laboratory results searching by category and one or more codes and date range using `GET [base]/Observation?patient=[id]&category=laboratory&code=[LOINC1{,LOINC2,LOINC3,...}]&date=[date]{&date=[date]}`.

**Servers**

- A server is capable of returning all of a patient's laboratory results queried by category using `GET [base]/Observation?patient=[id]&category=laboratory`.
 - A server is capable of returning all of a patient's laboratory results queried by category code and date range using`GET [base]/Observation?patient=[id]&category=laboratory&date=[date]{&date=[date]}`.
- A server is capable of returning all of a patient's laboratory results queried by category and code using `GET [base]/Observation?patient=[id]&category=laboratory&code=[LOINC]`.


- A server **SHOULD** be capable of returning all of a patient's laboratory results queried by category and one or more codes and date range using `GET [base]/Observation?patient=[id]&category=laboratory&code=[LOINC1{,LOINC2,LOINC3,...}]&date=[date]{&date=[date]}`.


- A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
- A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.

-------------------------

**Clients**

-  A client has connected to a server and fetched an organization by identifier using `GET [base]/Organization?identifier=[system]|[code]`
- A client has connected to a server and fetched an organization by name using`GET [base]/Organization?name=[string]`
- A client has connected to a server and fetched an organization by address using `GET [base]/Organization?address=[string]`


**Servers**

- A server is capable of returning an organization by identifier using `GET [base]/Organization?identifier=[system]|[code]`
- A server is capable of returning an organization by name using `GET [base]/Organization?name=[string]`
- A server is capable of returning an organization by address using `GET [base]/Organization?address=[string]`


-   A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
-   A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.

-------------------------

**Clients**

-  A client has connected to a server and fetched a patient using GET [base]/Patient/[id].
- A client has connected to a server and searched through available Patients using at least 2 (example name and gender) of the following search parameters:
   - name
   - gender
   - birthdate

To limit overly broad search results, a client search with gender **SHOULD** include family and given name search parameters.




**Servers**

- A server is capable of returning a patient using GET [base]/Patient/[id].
- A server returns valid FHIR Patient resources according to the Data Access Framework (DAF) Patient Profile..
- A server has exposed a FHIR Patient search endpoint supporting at a minimum the following search parameters:
   - identifier
- A server has exposed a FHIR Patient search endpoint supporting at a minimum the following search parameters when at least 2 (example name and gender) are present:
   - name
   - gender
   - birthdate
- A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
- A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.


-------------------------

**Clients**

-  A client has connected to a server and fetched a practitioner by identifier using `GET [base]/Practitioner?identifier=[system]|[code]`
- A client has connected to a server and fetched a practitioner by name using `GET [base]/Practitioner?family=[string]&given=[string]`


**Servers**

- A server is capable of returning a practitioner by identifier using `GET [base]/Practitioner?identifier=[system]|[code]`
- A server is capable of returning a practitioner by name using `GET [base]/Practitioner?family=[string]&given=[string]`


-   A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
-   A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.

-------------------------

**Clients**

-  A client connected to a server and fetched all procedures for a patient, including current as well as historical Procedures `GET/Procedure?patient=[id]`.
- A client has connected to a server and fetched all of a patient's procedures over a specified time period using `GET /Procedure?patient=[id]&date=[date]{&date=[date]}`.

**Servers**

-  A server is capable of returning a patient's procedures using `GET/Procedure?patient=[id]`.
- A server is capable of returning all of all of a patient's procedures over a specified time period using `GET /Procedure?patient=[id]&date=[date]{&date=[date]}`.


-   A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
-   A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.

-------------------------

**Clients**

- A client has connected to a server and fetched a patient's smoking status using `GET [base]/Observation?patient=[id]&code=72166-2`.


**Servers**

- A server is capable of returning a a patient's smoking status using `GET [base]/Observation?patient=[id]&code=72166-2`.


- A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
- A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.

**Clients**

- A client has connected to a server and fetched all of a patient's vital signs by searching by category using `GET [base]/Observation?patient=[id]&category=vital-signs`.
- A client has connected to a server and fetched all of a patient's vital signs searching by category code and date range using `GET [base]/Observation?patient=[id]&category=vital-signs&date=[date]{&date=[date]}`.
- A client has connected to a server and fetched any of a patient's vital signs by searching by one or more of the codes listed below using `GET [base]/Observation?patient=[id]&code[vital sign LOINC{,LOINC2,LOINC3,...}]`.


- A client **SHOULD** be capable of connecting to a server and fetching any of a patient's vital signs searching by one or more of the codes listed below and date range using `GET [base]/Observation?patient=[id]&code=[LOINC{,LOINC2...}]vital-signs&date=[date]{&date=[date]}`.




**Servers**

- A server is capable of returning all of a patient's vital signs that it supports using `GET [base]/Observation?patient=[id]&category=vital-signs`.
- A server is capable of returning all of a patient's vital signs queried by date range using `GET [base]/Observation?patient=[id]&category=vital-signs&date=[date]{&date=[date]}`.
- A server is capable of returning any of a patient's vital signs queried by one or more of the codes listed below using `GET [base]/Observation?patient=[id]&code[vital sign LOINC{,LOINC2,LOINC3,...}]`.


- A server **SHOULD** be capable of returning any of a patient's vital signs queried by one or more of the codes listed below and date range using `GET [base]/Observation?patient=[id]&code=[LOINC{,LOINC2...}]vital-signs&date=[date]{&date=[date]}`.



- A server has ensured that every API request includes a valid Authorization token, supplied via:Authorization: Bearer {server-specific-token-here}
- A server has rejected any unauthorized requests by returning an HTTP 401 Unauthorized response code.
