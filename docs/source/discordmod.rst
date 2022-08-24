=====
Discord Moderation
=====

- **Developer IDs**

On Discord, every username can have 9999 variants of it before it becomes unavailable. 
Trying to ban someone by just putting "Eternalll" is extremely dangerous. 
This is why we use `Developer IDs`_ instead, they provide a number such as 349909910995206145 (my ID) that ensures you are punishing the correct person.
Please enable this feature immediately.

.. _`Developer IDs`: https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID


- **Moderation Bot**

Atlas Utilities#3685 is the main moderation bot for all things. Main moderation commands use the **!** prefix.

Issuing Punishments
------------

.. warning::
    :ref:`Be aware that all bot-issued punishments are direct-messaged to the user. Refrain from using vague or immature reasons.`

+-----------+----------------------------------------+
| Command   | Function                               |
+===========+========================================+
| !warn 1   | Warn command.                          |
+-----------+----------------------------------------+
| !warn 2   | Mute command.                          |
+-----------+----------------------------------------+
| !warn 3   | Kick command.                          |
+-----------+----------------------------------------+
| !warn 4   | Softban command.                       |
+-----------+----------------------------------------+
| !warn 5   | Ban command.                           |
+-----------+----------------------------------------+
| !sclose   | Close ticket                           |
+-----------+----------------------------------------+

.. important::
    :ref:`Do not actually use the <brackets> and (parenthesis), they denote required and optional input.`

Warning
------------

.. code-block:: none

    !warn <user> <reason>

Warn the user, logging to the modlog and DMing the user. Warns cannot be appealed and are a recommended first action after or with a verbal warning.

.. important::
    :ref:`Remember, the user is DMed. Please provide an appropriate and at least a semi-descriptive reason so that the member can remediate their behavior.`

Mute
------------

.. code-block:: none

    !warn 2 <user> <time> <reason>

Mutes a user, preventing them from talking (and viewing certain channels). You must disconnect the user if they are in voice.

Users who evade mutes by leaving become permanently muted when rejoining. They must reach out to Modmail to get this fixed as it is their fault.

It is at moderator discretion to choose a time appropriate for the punishment. 

.. tip::
    :ref:`A time period of a day is usually suggested as a generic minimum period as punished users will be less likely to retaliate after 24 hours have passed.`

Kick
------------

.. code-block:: none

    !warn 3 <user> <reason>

Kicks remove the member from the server without deleting messages.

Reserve this punishment for new-ish members who need a reality check to come back when they are ready to read the rules and play nice.

Mostly unused, but can make a statement if necessary.

.. important::
    :ref:`Will remove all roles. Therefore, the member returning must rejoin the server to gain back roles.`

Softban
------------

.. code-block:: none

    !warn 4 <user> <reason>

Softban removes a member from the server, deleting 1 day of messages.

Reserve this punishment for those who you wish to kick, at the same time wanting to delete their messages alongside it.

Calls the user purge portion of the API by immediately banning and unbanning the user.

.. important::
    :ref:`Will remove all roles. Therefore, the member returning must rejoin the server to gain back roles.`

Ban
------------

.. code-block:: none
    
    !warn 5 <user> <reason>

Bans and DMs the user a link where they may appeal and purges 1 day of messages.

.. important::
    :ref:`Members may appeal their punishment via ban appeal form.`

Modlog Management
------------

- **Invoking the Modlog**

To search a user's modlog, you will run **!warnings <id>**. This will invoke an embed, beginning with an overview of their punishment history.

.. important::
    :ref:`Do not actually use the <brackets> and (parenthesis), they denote required and optional input.`

To interact with the modlog, you will need to use the arrow reactions to populate a single infraction. 

.. warning::
    :ref:`Do not interact with the modlog overview. Use the reactions to scroll to a specific reaction.`

- **◀️, ▶️ and ❌**

The left and right reactions scroll through the modlog. Pressing ❌ will close the embed.

- **✏️ and 🗑️**

After scrolling to an individual punishment, ✏️ will allow you to edit the reason. Useful if you made a typo or were not specific enough in your punishment reason. 
🗑️ allows you to clear the modlog entry.

.. important::
    :ref:`Edits made to the modlog do not update for the punished user in their direct messages.`

.. warning::
    :ref:`Cleared mutes will automatically unmute the user. Please keep this in mind when modifying the modlog.`