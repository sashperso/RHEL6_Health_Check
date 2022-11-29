# rhel6_health_check

The goal of this project is to automate a RHEL6 health check, and is an expansion from the rhel_health_check_crew's initial playbook to automate a RHEL8 health check. This allows a consultant more time for analysis and recommendations, rather than conducting information gathering activities.

## Name
Automated RHEL6 Health Check

## Description
This project uses Ansible to automate certain components of a RHEL6 health check.
An existing RHEL6 health check template can be found here:
https://gitlab.consulting.redhat.com/customer-success/consulting-engagement-reports/cer-template/-/blob/master/canned-content/en_US/RHEL-HC/implementation.adoc

### Strengths
- Ansible is agentless, so as long as the controller has an ssh connection (or is local), then it is possible to run an Ansible automated health check across a large fleet.
- Ansible is declarative code, therefore it is easier to read because developers state what they want the program to do, rather than describe how to do it.
### Weaknesses
- The customer will need to install Ansible on their system, in order to use this automated health check.
- There is a dependency on python packages, so their version needs to match what the Ansible interpreter requires.

### Opportunities
- More time for the consultant to add value - perform analysis and recommendations, rather than gather information.
- Standardise RHEL health check engagements at a high level.

### Threats
- Lack of adoption due to consultant not being familiar with the tool.
- Will the tool output recommendations? Who owns and takes responsibility for recommendations?
- Product ownership - who will own and maintain this tool?

## Badges
On some READMEs, you may see small images that convey metadata, such as whether or not all the tests are passing for the project. You can use Shields to add some to your README. Many services also have instructions for adding a badge.

## Visuals
Depending on what you are making, it can be a good idea to include screenshots or even a video (you'll frequently see GIFs rather than actual videos). Tools like ttygif can help, but check out Asciinema for a more sophisticated method.

## Installation
Within a particular ecosystem, there may be a common way of installing things, such as using Yarn, NuGet, or Homebrew. However, consider the possibility that whoever is reading your README is a novice and would like more guidance. Listing specific steps helps remove ambiguity and gets people to using your project as quickly as possible. If it only runs in a specific context like a particular programming language version or operating system or has dependencies that have to be installed manually, also add a Requirements subsection.

## Usage
The following instructions allow the user to conduct a rhel health check on their local machine.
$ git clone <url>
$ cd ~/rhel
$ ansible-playbook rhel_hc_init.yml -K
Enter root password
$ cat /tmp/rhel_hc_report_<time>_<date>

## Support
Tell people where they can go to for help. It can be any combination of an issue tracker, a chat room, an email address, etc.

## Roadmap
Milestone 1: Project Started
Date: 221025
![Automated RHEL Health Check Product Roadmap](/images/rhel_hc_product_roadmap.png "Automated RHEL Health Check Product Roadmap")

## Contributing
We are open to contributions. 
We need designers who can identify problems, and co-create solutions with engineers. We need engineers to build the prototype.

Please read CONTRIBUTING.md for more information.

## Authors and acknowledgment
Show your appreciation to those who have contributed to the project.

## License
For open source projects, say how it is licensed.

## Project status
If you have run out of energy or time for your project, put a note at the top of the README saying that development has slowed down or stopped completely. Someone may choose to fork your project or volunteer to step in as a maintainer or owner, allowing your project to keep going. You can also make an explicit request for maintainers.
