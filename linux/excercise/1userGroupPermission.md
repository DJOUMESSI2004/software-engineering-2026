🧪 FULL PRACTICAL EXERCISE — Users, Groups, Permissions
🎯 Scenario

You are the system administrator of a small development team.

You must create:

Two human users:

wilfrid

brenda

One service user (no login):

deploybot

One group:

devteam

One shared project folder:

/projectX

The rules:

Human users must have home directories.

The service user must NOT have a home directory and must NOT be able to log in.

The shared folder /projectX must be accessible ONLY by members of devteam.

Files created inside /projectX must automatically belong to the group devteam.

The folder must have chmod 770 permissions (your tab explains this mode) .

You must justify why each command is used — not just type it.