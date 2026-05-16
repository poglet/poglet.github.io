---
layout: default
title: Configuring Dynamic DNS on OPNsense
parent: Guides
---

# Configuring Dynamic DNS on OPNsense

These steps are based on the guide configuration shared in the [OPNsense Reddit Community](https://www.reddit.com/r/opnsense/comments/1bgdqx0/how_to_set_up_cloudflare_dynamic_dns_ddns_in/).

---

## Cloudflare Configuration

1. **Create an API Token:** Go to **My Profile** > **API Tokens** and click **Create Token**.
2. **Select Template:** Locate **Edit zone DNS** and click **Use template**.
3. **Name the Token:** Change the token name if desired (e.g., *OPNsense DDNS*).
4. **Set Permissions:** Set permissions to **Zone** > **DNS** > **Edit**.
5. **Set Zone Resources:** Set to **Include** > **Specific zone** > *[Select the zone you want OPNsense to update]*.
6. **Review Summary:** Leave the remaining settings at their defaults and click **Continue to summary**.
7. **Generate Token:** If the configuration looks correct, click **Create Token**.
8. **Test (Optional):** Copy the provided test code and paste it into your terminal to verify the setup if desired.
9. **Save the Token:** Copy the generated token and save it securely (e.g., in a password manager), as this is the only time it will be visible.

---

## OPNsense Configuration

### General Settings
1. Navigate to **Services** > **Dynamic DNS** > **Settings** > **General settings**.
2. Check the box to **Enable**.
3. Set the **Interval** (e.g., `360` seconds for 10 updates per hour).
4. Set the **Backend** to `ddclient`. 
   * *Note: If this backend option is missing, navigate to **System** > **Firmware** > **Plugins** and install `os-ddclient` by clicking the **+** icon.*

### Account Settings
1. Click the **Accounts** tab at the top and click the orange **+** icon to create a new account.
2. Configure the entry with the following details:
   * **Enabled:** Check this box
   * **Description:** Enter an identifying name (e.g., `Cloudflare`)
   * **Service:** Select `Cloudflare`
   * **Username:** Leave blank
   * **Password:** Paste your Cloudflare API token
   * **Zone:** Enter your domain zone (must match the zone configured in Cloudflare, e.g., `domain.com`)
   * **Hostname(s):** Enter the specific domain or subdomain to update (e.g., `subdomain.domain.com`)
   * **Check IP Method:** Set to `Interface`
   * **Interface to Monitor:** Set to `WAN`
   * **Force SSL:** Check this box
3. Click **Save** to apply the configuration.
