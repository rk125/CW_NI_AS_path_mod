
<B>Crosswork Network Insights (CW NI) AS path pattern modification script</B>

CW NI can give an alarm if route ASN list contains some specific ASN. For that to happen user needs to configure "AS path pattern"
This script was created to automate AS path pattern configuration.

What does script do:
- grabs whole CW NI configuration from user's account
- replaces "asPathPattern" value with ASN pattern given as argument "--ASNs"
- pushes configuration back to CW NI

If ASN pattern should be 41346|48372|34623|80481 run it with:
<i>python3 cw_ni_ASpath_mod.py  --key xxx --keyid yyy --ASNs "41346|48372|34623|80481"</i>
where ASNs need to be in quotes, rest or params as in original documentation.
<br>
For key and keyid - need to generate API key and API Key identifier (ID) in CW NI user account.
How to do that https://www.cisco.com/c/en/us/td/docs/cloud-systems-management/crosswork-network-automation/b_cisco-crosswork-cloud-user-guide/m_crosswork-network-insights-api.html#id_121414

I took script from https://www.cisco.com/c/en/us/td/docs/cloud-systems-management/crosswork-network-automation/b_cisco-crosswork-cloud-user-guide/m_crosswork-network-insights-api.html and modified it for my needs
