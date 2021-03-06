.. meta::
   :description: Amazon GuardDuty Integration
   :keywords: AWS Guard Duty, FQDN, Egress Control, IDS/IPS 


=================================
 Amazon GuardDuty Integration 
=================================

Aviatrix Controller integrates with `Amazon GuardDuty <https://aws.amazon.com/guardduty/>`_ to provide you the IDS protection on a per account and region bases. 

Amazon GuardDuty continuesly monitors an account's AWS environment and reports findings. 
GuardDuty sifts through CloudTrail logs, VPC Flow logs and DNS logs to assess risk and generate findings. To learn more on GuardDuty, read `Amazon GuardDuty FAQ <https://aws.amazon.com/guardduty/faqs/>`_.

Configuration
--------------

To enable GuardDuty Integration, login to Aviatrix Controller, on the left side of
the navigation bar, go to Security -> GuardDuty, as shown below. 

|guardduty_config|

Integration and Enforcements
-------------------------------

Aviatrix Controller provides additional monitoring, logging and enforcement services when you enable Amazon GuardDuty from the Aviatrix Controller Console, 
as listed below. 

 - Aviatrix Controller polls periodically Amazon `GuardDuty findings <https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_finding-types-active.html>`_. 
 - Findings from Amazon GuardDuty are `logged <https://docs.aviatrix.com/HowTos/AviatrixLogging.html#id13>`_ to the Controller syslog. (Syslog can be exported to `Aviatrix supported Logging services <https://docs.aviatrix.com/HowTos/AviatrixLogging.html>`_.)
 - Findings from Amazon GuardDuty are displayed in Alert Bell on the Controller console.  
 - In addition, if a finding is about instances in a VPC being probed by a malicious IP address, this IP address is blocked by the Controller automatically programming the Network ACL of the VPC, as shown below. 

|guardduty_acl|


.. |guardduty_config| image::  guardduty_media/guardduty_config.png
   :scale: 50%

.. |guardduty_acl| image::  guardduty_media/guardduty_acl.png
   :scale: 50%


.. add in the disqus tag

.. disqus::
