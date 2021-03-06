## Vendor:
    Redcap app  

## Affected version:
The issue exists to version 9.2.3

## Description:   
1.	SQL injection attack allow attackers to spoof identity, tamper with existing data, cause repudiation issues such as voiding transactions or changing balances, allow the complete disclosure of all data on the system, destroy the data or make it otherwise unavailable, and become administrators of the database server

2. Cross-Site Request Forgery (CSRF) is a type of attack that occurs when a malicious web site, email, blog, instant message, or program causes a user’s web browser to perform an unwanted action on a trusted site when the user is authenticated.


## Proof of Concept:

1. 
SQLInjection : https://redcapdemo.vanderbilt.edu/redcap_v9.2.3/Calendar/scheduling_ajax.php?action=edit_single
<p align="center">
<img src="https://github.com/vuongdq54/Redcap_9/blob/main/SQl_daydiff.JPG" />
</p>

SQLInjection : https://redcapdemo.vanderbilt.edu/redcap_v9.2.3/Calendar/scheduling_ajax.php?action=del_single
<p align="center">
<img src="https://github.com/vuongdq54/Redcap_9/blob/main/SQL_Cal_id.JPG" />
</p>
2. CSRF: Link affect: any link add,update, delete data in database use method GET for HTTP requests.
<p align="center">
example:
https://redcapdemo.vanderbilt.edu/redcap_v9.2.3/Calendar/scheduling_ajax.php?pid=xxx&action=edit_single
https://redcapdemo.vanderbilt.edu/redcap_v9.2.3/Calendar/scheduling_ajax.php?pid=xxx&action=del_single
</p>

## Reference
<p align="center">
https://www.project-redcap.org/
</p>
<p align="center">
https://wiki.utdallas.edu/display/REDCap/REDCap+Change+Log Version 9.3.0 - (released 8/15/2019)
</p>
