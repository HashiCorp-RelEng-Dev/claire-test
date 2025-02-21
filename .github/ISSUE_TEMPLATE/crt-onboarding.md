name: CRT Onboarding
description: Submit an onboarding request
body:
  - type: input
    id: repository name
    attributes:
      label: Repository Name
      description: What is the name of the repository that you would like to onboard?
    validations:
      required: true
  - type: input
    id: repository link
    attributes:
      label: Link to Repository
      description: Link/URL to Repository
    validations:
      required: true

  - type: dropdown
    id: Repository Type
    attributes:
      label: What type of repository is this? (Community Edition, Internal, or Enterprise?)
      multiple: false
      default: 0
      options:
        - "CE"
        - "INT"
        - "ENT"
    validations:
      required: true
  - type: textarea
    id: Release Approvers
    attributes:
     label: Description
     description: Please include the github usernames that you would like to have added as release approvers
    validations:
      required: true
  - type: markdown
    attributes:
      value: |
        ---
  - type: tasklist
    id: link
    attributes:
     label: What do you plan to release? Go Biniaries, Docker Images, Redhat? 
     description: Please tick all the types of artifacts
     - [ ] Go Binaries
     - [ ] Docker Images
     - [ ] RedHat Images
     - [ ] Linux Packages
    validations:
      required: true

