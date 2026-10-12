# Create-Users-Groups-and-Organizational-Units
Hands-on Active Directory home lab documenting Windows Server administration, organizational units, user accounts, security groups, and access management.

## Overview
This lab covers foundational Microsoft Active Directory administration using Active Directory Users and Computers (ADUC) in a Windows Server domain environment.

**Lab environment:** Windows Server / Active Directory Domain Services  
**Domain:** `corp.lab.local` *(example lab domain)*  
**Tools:** Active Directory Users and Computers (ADUC)

## Objectives
- Create and organize Organizational Units (OUs).
- Create a domain user account.
- Create a security group.
- Add a user to a security group.
- Move a user between OUs.
- Understand group-based access management and least privilege.

## Tasks Completed

### 1. Organizational Unit Structure
I planned a company-style OU structure to separate users and computer objects.

Example structure:
- Sales
- IT
- HR
- Workstations

OUs help administrators organize domain objects and apply Group Policy or delegate administration where appropriate.

### 2. User Account Creation
I created a sample domain user in the Sales OU.

The exercise covered:
- First and last name fields.
- User logon name (UPN).
- Pre-Windows 2000 logon name (SAM account name).
- Password configuration and the option to require a password change at next logon.

Example account formats:
- UPN: `jsmith@corp.lab.local`
- SAM account name: `CORP\jsmith`

These are two logon formats for the same account.

### 3. Security Group Creation
I created a security group named `Sales-Team` with Global scope and Security group type.

Added the sample user to the group using the Members tab and the Check Names function.

This demonstrates how administrators can manage access through group membership instead of assigning permissions separately to each user.

### 4. Moving Users Between OUs
I practiced moving the sample user from Sales to IT and back to Sales.

This reinforced how domain objects can be reorganized as users change departments. OU placement can affect the Group Policy settings applied to an account.

## Key Concepts Learned

**Organizational Units:** Containers used to organize directory objects, support delegated administration, and apply Group Policy.

**User Principal Name (UPN):** A logon name formatted similarly to an email address.

**SAM Account Name:** The legacy Windows logon name format, commonly written as `DOMAIN\username`.

**Security Groups:** Groups used to assign permissions to resources and manage access through membership.

**Group-Based Access Management:** Grant permissions to appropriate groups, then manage access by adding or removing users from those groups.

**Least Privilege:** Provide only the access necessary for a user to perform their responsibilities.

**Security vs. Distribution Groups:** Security groups can be used for permissions. Distribution groups are intended for email distribution and do not grant resource permissions.

## Troubleshooting and Validation
- Used ADUC to create and locate directory objects.
- Practiced resolving a user account with Check Names when adding group membership.
- Reviewed OU protection against accidental deletion.
- Practiced moving a user between organizational units.

## Evidence
Screenshots will be added after verifying the lab configuration:
- [ ] OU structure visible in ADUC.
- [ ] Sample user visible in the Sales OU.
- [ ] Sales-Team group membership visible.
- [ ] User returned to the intended OU.

## Outcome
I developed foundational skills in Active Directory object organization, user provisioning, security group membership, and group-based access management.
