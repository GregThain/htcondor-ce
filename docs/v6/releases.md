Releases
========

HTCondor-CE 6 is distributed via RPM and are available from the following Yum repositories:

- [HTCondor LTS and Feature Releases](https://htcondor.org/htcondor/download/)
- [The OSG Consortium](https://osg-htc.org/docs/common/yum/)


Known Issues
------------

Known bugs affecting HTCondor-CEs can be found in
[Jira](https://opensciencegrid.atlassian.net/issues/?jql=project%20%3D%20HTCONDOR%20AND%20status%20not%20in%20(done%2C%20abandoned)%20and%20component%20%3D%20htcondor-ce%20and%20issuetype%20%3D%20bug)

Updating to HTCondor-CE 6
-------------------------

!!! tip "Finding relevant configuration changes"
    When updating HTCondor-CE RPMs, `.rpmnew` and `.rpmsave` files may be created containing new defaults that you
    should merge or new defaults that have replaced your customzations, respectively.
    To find these files for HTCondor-CE, run the following command:

        :::console
        root@host # find /etc/condor-ce/ -name '*.rpmnew' -name '*.rpmsave'

HTCondor-CE 6 is a major release that aligns its security model with
[HTCondor 9.0's improved security model](https://htcondor.readthedocs.io/en/v9_0/version-history/upgrading-from-88-to-90-series.html).
As such, upgrades from older versions of HTCondor-CE may require manual intervention.

HTCondor-CE 6 Version History
-----------------------------

This section contains release notes for each version of HTCondor-CE 6.
Full HTCondor-CE version history can be found on [GitHub](https://github.com/htcondor/htcondor-ce/releases).

### 6.0.1 ###

[This release](https://github.com/htcondor/htcondor-ce/releases/tag/v6.0.1) includes the following new features:

-   Add grid CA and host certificate/key locations to default SSL search paths
-   Verifies that HTCondor-CE can access the local HTCondor's `SPOOL` directory
-   Can use `condor_ce_trace` without SciToken to test batch system integration
-   `condor_ce_upgrade_check` checks compatibility with HTCondor 23.0
-   Adds deprecation warnings for old job router configuration syntax

### 6.0.0 ###

[This release](https://github.com/htcondor/htcondor-ce/releases/tag/v6.0.0) includes the following new features:

-   Align HTCondor-CE security configuration with HTCondor defaults
-   Add example configuration on how to ban users
-   Add `condor_ce_transform_ads` command
-   Improve essential directory checking and creation at startup

Getting Help
------------

If you have any questions about the release process or run into issues with an upgrade, please
[contact us](../index.md#contact-us) for assistance.