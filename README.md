# hardening-tests
Just some files to play with during hardening tests

This file <a href="https://github.com/segloser/hardening-tests/blob/main/wazuh-agent-install-hardening.sh">**wazuh-agent-install-hardening.sh**</a> will make the proper arrangements to install Ansible in a Cubic project and automate some hardening.
It will also install the Wazuh Agent, so you will need to have a Wazuh Manager listening to it in the same network.
The script uses the proper SCA Template for providing statistics and details about CIS Benchmarks compliance, in the SCA section in the Wazuh Dashboard.
The two only versions tested are: Ubuntu 18.04 and 20.04.

<li>Must be run as root</li>
<li>Change the Wazuh Manager Default IP when required, manually later on or directly in the script before launching it.</li>
<li>AIDE installation is disabled by default, since Wazuh offers integrity check by default.</li>  
<li>Many network and partitioning configuration settings are not implemented. Add it yourself according to your environment needs.</li>

It is for a very specific environment, so this script will not be useful for general purposes.

The script downloads from other repositories (Main source: <a href="https://github.com/florianutz/Ubuntu1804-CIS">florianutz</a>) and the current directory all it needs. No breakpoints are enabled, so if you want to have a more granular control of the actions or functions, uncomment the breakpoints (well marked).

You can disable certain rules during the test to speed up the process.

# WARNING
Do not run this script in a production environment. 
