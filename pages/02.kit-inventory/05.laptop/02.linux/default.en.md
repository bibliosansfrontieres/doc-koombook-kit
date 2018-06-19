---
title: 'Linux Ubuntu'
---

## Ubuntu

Ubuntu is a user-friendly Linux distribution with a "simple, intuitive, and secure" interface.

By default, the computer starts up using Ubuntu.

### Installation

LTS (Long Term Support) versions, which are supported for five years, are preferred.  Version 16.04 recently replaced 14.04.  There are currently some concerns regarding guest sessions on version 18.04.

The installation and configuration can both be done using an ansible playbook (an automization tool for configuration and management) called `idbuntu`
([that is available on Github](https://github.com/bibliosansfrontieres/idbuntu)). The reading, although technical, describes the implementation in its entirety.

## Sessions

There are three types of user sessions.

### Guest Sessions

**Guest sessions** are designed for users.

Among other characteristics, these sessions have amnesia: once opened, it is a completely new session, recreated based on a model, and the session is erased once it is closed.  Because of this, we don't have to worry about potential information left by each user, such as personal documents or log-in information for websites.

### `Ideas Box` Sessions

**`Ideas Box` Sessions** serve as a model for guest sessions.

Any customizations, such as wallpaper or shortcuts, made in an Ideas Box session will be replicated in the guest session model. Thus, Ideas Box sessions are not meant to be used daily.

To login to an Ideas Box session, use the username `ideascube`.  BSF will send the password to you upon request.

### `Admin` Sessions

**`Admin` Sessions** can be used for the administration and maintenance of the system. This is the only session with administrative rights, and thus the only one that permits you to add or delete software or programs, change the network configuration, and edit other system components.

It is only used by technicians, in case problems arise.

The login name is `bsfadmins`, but we prefer to create a dedicated session for the local technician.  The BSF technicians' SSH keys remain present in the root account.  If they are deleted, no support can be provided.

### See Also

  * [Script to create accounts](https://github.com/bibliosansfrontieres/idbuntu/blob/master/roles/users/tasks/main.yml)
  * [Customization of  guest sessions](https://help.ubuntu.com/community/CustomizeGuestSession) on the Ubuntu Wiki

## The Programs

The list of programs generally installed appear in [the playbook](https://github.com/bibliosansfrontieres/idbuntu/blob/master/roles/software/tasks/main.yml).

These include office, image creation, video editing, photo retouching, music editing and publishing, programming, discovering, and gaming programs.

We also added the Tor browser (to surf the web anonymously), as well as Skype.

## Administration

To proceed to system administration, you must first of all contact BSF to put in place a dedicated account.  This account is not created automatically because it is rarely needed.  However, on some projects that have the necessary resources, having this account is a plus.

By default, Ubuntu automatically downloads and applies security updates.
