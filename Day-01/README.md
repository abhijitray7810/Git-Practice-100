# Git Repository Setup - Stratos DC Storage Server

## Project Overview

This project involves setting up a Git repository on the Storage Server in the Stratos DC for the Nautilus development team's new application development project.

## Objective

Create a centralized Git bare repository that will serve as the primary version control system for the Nautilus application development team.

## Requirements

- Install Git package using yum
- Create a bare repository at `/opt/cluster.git`
- Ensure proper configuration for team collaboration

## Repository Structure

```
/opt/cluster.git/
├── HEAD
├── config
├── description
├── hooks/
├── info/
├── objects/
└── refs/
```

## What is a Bare Repository?

A bare repository is a Git repository that doesn't have a working directory. It only contains the version control information (the `.git` directory contents). This makes it ideal for:

- Central repositories that act as collaboration hubs
- Repositories that users push to and pull from
- Server-side repositories that don't need file checkouts

## Getting Started

### Prerequisites

- Access to Storage Server in Stratos DC
- Root or sudo privileges
- Network connectivity to the server

### Installation Steps

1. Connect to the Storage Server via SSH
2. Install Git using yum package manager
3. Create the bare repository at specified location
4. Verify the installation and configuration

For detailed commands, see [COMMANDS.md](COMMANDS.md)

## Usage for Developers

Once the repository is set up, developers can:

### Clone the Repository

```bash
git clone <username>@<storage-server>:/opt/cluster.git
```

### Basic Git Workflow

```bash
# Make changes to files
git add .
git commit -m "Your commit message"
git push origin main
```

### Pull Latest Changes

```bash
git pull origin main
```

## Repository Information

- **Location:** `/opt/cluster.git`
- **Type:** Bare Repository
- **Server:** Storage Server, Stratos DC
- **Purpose:** Central repository for Nautilus development team

## Team Information

- **Client:** Nautilus Development Team
- **DevOps Team:** Stratos DC
- **Project:** New Application Development

## Documentation

- [COMMANDS.md](COMMANDS.md) - Complete command reference
- [QUESTION.md](QUESTION.md) - Original requirements and task details

## Support

For issues or questions regarding this setup, contact the DevOps team.

## Notes

- The repository name must be exactly `/opt/cluster.git`
- Ensure proper permissions are set for team access
- Regular backups of the repository are recommended

## License

Internal use only - Nautilus Development Team

---

**Created for:** Nautilus Development Team  
**Maintained by:** Stratos DC DevOps Team  
**Last Updated:** October 2025
