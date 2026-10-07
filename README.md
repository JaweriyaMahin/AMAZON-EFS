# EFS Shared Storage – AWS

## Objective
Create shared storage for two Amazon Linux EC2 instances using Amazon EFS.

## What is EFS?
Amazon EFS (Elastic File System) is a managed and scalable file storage
service in AWS. It allows multiple EC2 instances to access the same files at the same time.

## Services Used
- Amazon EC2
- Amazon EFS
- Security Group
- NFS

## Architecture

EC2-1 ──┐
        ├── EFS → Shared Storage
EC2-2 ──┘

## Configuration
- OS: Amazon Linux 
- EFS Mount Point: `/mnt/efs`
- NFS Port: `2049`
- Two EC2 instances connected to the same EFS

## Result
A file created on EC2-1 was successfully accessed from EC2-2, 
proving that EFS provides shared storage between multiple EC2 instances.

## Real-World Use
EFS can be used when multiple servers need access to the same 
application files, uploads, shared content, or data.
