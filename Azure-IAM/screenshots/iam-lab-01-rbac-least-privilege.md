# Azure IAM Lab 01 - RBAC and least privilege

Goal
Set up Azure RBAC so each user only has the minimum permissions they need.

What I did
- Created test users in Microsoft Entra ID
- Assigned Azure roles using RBAC at the correct scope
- Verified permissions followed the least privilege principle

Key terms
- RBAC: Role Based Access Control
- Scope: where the role applies (subscription, resource group, resource)
- Role assignment: connects a user or group to a role at a scope

Steps

1. Create test users
- In Microsoft Entra ID, created user1 and user2
- Purpose: simulate different access levels

Evidence
- Screenshot: user list

2. Choose the correct scope
- Selected the scope I wanted to control (resource group or subscription)
- Reason: least privilege is stronger when scope is smaller

Evidence
- Screenshot: scope page

3. Assign roles (least privilege)
- user2 assigned Contributor (only where needed)
- Avoided giving Owner unless required
- Used built in roles instead of custom roles for this basic lab

Evidence
- Screenshot: add role assignment
- Screenshot: role assignment result

4. Validate access
- Checked role assignments from Access control (IAM)
- Confirmed user permissions match the role and scope
- Optional: sign in as the user and confirm what they can and cannot do

Evidence
- Screenshot: role assignments list

What I learned
- Least privilege means smallest role + smallest scope
- Owner is risky because it can grant access and change permissions
- Contributor can manage resources but cannot grant access
- Reader can view but cannot change resources

Next lab
- Create a custom role for an exact permission set
- Use groups instead of assigning roles to individual users
