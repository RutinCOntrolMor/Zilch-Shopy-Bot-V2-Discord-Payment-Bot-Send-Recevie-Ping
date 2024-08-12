<div align="center">


# Discord Payment Bot

![LatestVersion](https://maszindex.zaanposni.com/api/v1/views/version/current/readme?)
[![https://github.com/users/zaanposni/packages/container/package/masz_backend](https://img.shields.io/badge/using-docker-blue?style=for-the-badge)](https://github.com/users/zaanposni/packages/container/package/masz_backend)
[![https://discord.gg/hashnode](https://img.shields.io/discord/779262870016884756?logo=discord&style=for-the-badge)](https://discord.gg/hashnode)
[![SupportedLanguages](https://img.shields.io/badge/translated-7%20languages-brightgreen?style=for-the-badge)](https://github.com/zaanposni/discord-masz/blob/master/translations/supported_languages.json) 



![Discord Bots](https://top.gg/api/widget/962093056910323743.svg)<br>

## Links

- **[Support Server](https://discord.gg/TsSAfdN4hS)**
- **[Invite Bot](https://discord.com/api/oauth2/authorize?client_id=962093056910323743&permissions=1374524140630&scope=bot%20applications.commands)**


## AI-Powered Spam Identification

The bot boasts a remarkable capability to identify spam messages and even detect sequences of messages that exhibit spam-like characteristics with a high degree of precision, especially when aptly trained.

### Swift Configuration Procedure

1. Activate the system via the `/antispam enable` command.
2. Configure the list of disregarded channels and roles through the `/antispam ignore` command group.

## Next-Generation Word Filtering

AIAS introduces an innovative word filtering system that excels in pinpointing blacklisted terms even within the most challenging contexts. This filter is proficient in neutralizing bypass symbols, implementing antialiasing, and remarkably, it can even identify offensive language concealed amidst a series of messages.

## Optimal CPU Utilization

- Remarkably efficient CPU usage, consuming only about 0.1% of an Intel i7 9750h's processing power when streaming high-quality audio (Opus 48Khz 16-bit Stereo) to a singular server.

## Comprehensive Discord API Coverage

- This library encompasses the entirety of Discord API endpoints, including those related to voice communication.

## Simultaneous Discord API Access

- This library leverages custom asynchronous coroutines and a well-structured thread pool mechanism to achieve the capability of making fully asynchronous and concurrent requests to the Discord API.

## Advanced Rate-Limiting Mechanism

- This system guarantees the preservation of request execution order as per their submission order, even when launched across various threads. All this is achieved without violating the limitations set by the Discord API and while maintaining concurrent execution across all endpoints.

⭐ **Incident Tracking and Managed (Temporary) Sanctions** - An ideal solution for moderating your server efficiently.
⭐ **Effortless Search Functionality** - Facilitates reliable user-specific infraction or note searches.
⭐ **Localization Customization** - Flexibility to tailor time zones and languages to your preference.
⭐ **Automated Moderation** - Empower your server to efficiently tackle trolls and disruptors.
⭐ **Ban Appeal Management and Webhook Notifications** - A transparent approach to server moderation.
⭐ **Web Interface and Discord Bot Integration** - Experience the comprehensive features of MASZ.
⭐ **Robust API and Plugin Compatibility** - Ideal for developing custom scripts and automations tailored to your needs.

### 🚀 Demo

[![https://demomasz.zaanposni.com](https://img.shields.io/badge/demo-online-%234c1?style=for-the-badge)](https://demomasz.zaanposni.com)

Visit [https://demomasz.zaanposni.com](https://demomasz.zaanposni.com) for a demo.\
Furthermore, join the demo guild [https://discord.gg/7ubU6aWX9c](https://discord.gg/7ubU6aWX9c) to get the required permissions.

### 👀 Preview

![dashboard preview](/docs/dashboard.png)

**Previews and examples can be found at:** [https://github.com/zaanposni/discord-masz/tree/master/docs](https://github.com/zaanposni/discord-masz/tree/master/docs)

### 🤝 Support Server

Join this server to receive update information or get support: [https://discord.gg/hashnode](https://discord.gg/hashnode)

## 🛠 Hosting


The process of **establishing your personal MASZ instance** can be undertaken through the subsequent guidelines. Should you encounter any queries or concerns, do not hesitate to reach out to either Zaanposni or a designated support representative:

- [Discord server](https://discord.gg/hashnode)
- [Email](mailto:me@zaanposni.com)


Please be aware that MASZ is not made available as a public hosted service. It is incumbent upon you to personally host your own instance. 

Furthermore, kindly note that exclusive support is provided solely for deployments on Linux and Windows servers. Refer below for the prerequisites in terms of software. 

It is imperative to understand that free hosting platforms such as Replit or Heroku **do not function** in this context. Consequently, opting for a Virtual Private Server (VPS) is a requisite for this purpose.


### Quick Summary

- Craft a Discord application via [https://discord.com/developers/applications](https://discord.com/developers/applications)
- Define redirect URLs for your Discord application as specified [here](https://github.com/zaanposni/discord-masz#discord-oauth).
- Activate **Server Members** and **Message Content Intent** in your bot's settings.
- Initiate the configuration using `python3 setup.py` (`python setup.py` on Windows).
- Launch the application with the command `docker-compose up -d`.
- The application shall be accessible via `127.0.0.1:5565`.
- Further insights into diverse deployment strategies and additional steps can be found through continued reading.


### Discord Authorization Protocol

Generate your personalized OAuth application by visiting the designated platform [here](https://discord.com/developers/applications). Furthermore, configure the requisite redirect paths within the `OAuth2` tab.

Kindly ensure to establish the ensuing configurations (choose either localhost or domain contingent upon your deployment):

![redirect illustration](/docs/redirects.png)
![redirect illustration 2](/docs/redirects2.png)

### Bot Mindset

In your bot configurations, activate the **Server Members** and **Message Content Intent** for heightened operational awareness.

![intents example](/docs/intents.png)


### Slash Commands Integration

If you have undertaken the addition of your bot autonomously, it's possible that your bot is currently devoid of the requisite authorization for creating slash commands. To rectify this, kindly follow the provided link for authorizing your bot's capability: `https://discord.com/api/oauth2/authorize?permissions=8&scope=bot%20applications.commands&client_id=yourid`.

Please ensure to substitute "yourid" with your specific client id at the conclusion of the link.

## ✔️ Docker Setup (Recommended)

[![https://github.com/users/zaanposni/packages/container/package/masz_backend](https://img.shields.io/badge/using-docker-blue?style=for-the-badge)](https://github.com/users/zaanposni/packages/container/package/masz_backend)

### Requirements

- [docker](https://docs.docker.com/engine/install/ubuntu/) & [docker-compose](https://docs.docker.com/compose/) (`docker-compose -v` > 1.25)
- [python3](https://www.python.org/) for setup

#### In Case of Domain Deployment

- A (sub)domain is requisite for housing the application.
- Your host necessitates the implementation of a reverse proxy.

### Operational Directives

- Procure this repository through downloading: `git clone https://github.com/zaanposni/discord-masz` ([link to compressed file](https://codeload.github.com/zaanposni/discord-masz/zip/master))
- Utilize `python3 setup.py` (or `python setup.py` on Windows) to initiate the configuration procedure.
- Initiate the launch of the application using the command: `docker-compose up -d`.
- The application shall be accessible via `127.0.0.1:5565`. In the case of hosting the application under a domain, ensure that your reverse proxy directs traffic towards this designated local port.

### Update

To install a new update of ShopyBOT just use:

```bash
docker-compose pull
docker-compose up -d
```

## ↪ Post Implementation Phase

### 🐾 Initial Measures

- You shall be able to access your application through `yourdomain.com` (or `127.0.0.1:5565`). Upon doing so, a login interface will appear, prompting you to undergo Discord OAuth2-based authentication.
- Upon granting authorization for your service to interface with your Discord account, your profile image will become visible within the toolbar (in developmental stages, this image is hosted on `127.0.0.1:8080`).
- In the eventuality that you are logged in as a site administrator, you shall find utility in the "register guild" (+) icon, which serves to record your guilds and commence the process.
- Depending on the preferred attributes and functionalities, it might be necessary to bestow upon your bot elevated permissions, which are elucidated in the section labeled `Activation of Constricted Attributes`.

### Recordkeeping and Rate Restriction

MASZ makes use of the `X-Forwarded-For` HTTP header for the purpose of recordkeeping and rate restriction. It is imperative that this header is configured within your reverse proxy to ensure the optimal user experience.

### Activation of Constricted Attributes

#### ⭐ Exoneration Petition Attribute

Should you wish for individuals under banishment to access their case details, confer the `ban people` entitlement upon your bot. This shall permit them to discern the rationale behind their banishment and provide comments or submit an exoneration petition. Moreover, ascertain that the bot holds a position of sufficient authority within the hierarchy of roles to impose bans upon individuals subordinate to it.

In addition, if you aspire to enable the feature of exoneration petitions ("ban appeals"), devise a set of inquiries within the designated "appeals" segment of your guild dashboard.

## ⭐ Infliction Attribute

In the eventuality that you desire the application to implement penal measures like muting and barring, executing them automatically (such as unbanning after a predetermined duration on temporary bans), endow your bot with the subsequent permissions based on your requisites:

```md
Administer designations - for muted designation | Regulate members - for utilizing discord's timeouts
Expel individuals
Prohibit individuals
```

Moreover, assure that the bot occupies a sufficiently elevated position within the hierarchy of roles to reprimand individuals subordinate to it.

In case you opt not to utilize a designation for muting members, MASZ will inherently resort to discord's timeouts in the absence of your specification of a muted designation.

## ⭐ Self-regulation Attribute

In order to circumvent any predicaments concerning message eradication or access permissions, it is strongly recommended to confer upon your bot an exceedingly elevated and robust or even the `administrator` designation.

## ⭐ Invitational Tracing

Empowers MASZ to trace the invitations being employed by new members. Bestow upon your bot the `oversee guild` privilege to avail of this attribute.

## ⭐ Rigorous Permission Scrutiny

You possess the capability to activate stringent permissions within your guild configuration. This mode will scrutinize the permissions of your role-bearing moderators prior to fashioning a moderator case. A moderator shall solely be empowered to conceive a modcase of expulsion or prohibition if they possess the corresponding entitlement within discord. Should you choose not to activate this mode, moderators can devise any modcase.

</div>