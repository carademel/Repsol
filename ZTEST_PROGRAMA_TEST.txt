##  REPORT ztest_programa_test.

**SUBMIT** zatc_test.

**CALL FUNCTION** 'BAPI_USER_GETLIST'

**SUBMIT** zavh_populate_ms_tables
~~~
SELECT SINGLE a~bukrs
INTO @DATA(lv_bukrs)
FROM bkpf AS a
INNER JOIN bseg AS b ON a~belnr EQ b~belnr
inner JOIN t001 as c on a~bukrs eq c~bukrs.
~~~
**SUBMIT** zprueba


**CALL METHOD** zmark_cl_api_mermaid=>get_instance

<!--stackedit_data:
eyJoaXN0b3J5IjpbNjg2ODc3MDM2LC0yMDQwNDU3MDAzXX0=
-->