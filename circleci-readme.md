# Readme for Disable or Enable CircleCI Workflows
1. Create organization contexts variable 

  Contexts name = ` DisableEnable ` 

  Environment Variables Name  = ` CIRCLECISECRET `
  
  Value = ` circleci ` for **Enable workflows** 
          
  Value = ` githubactions ` for **Disable workflows**

2. Insert this job to first job

```
# Add this job to all workflows
  disable-enable:
    docker:
      - image: 'cimg/base:stable'
    steps:
      - run: echo ${CIRCLECISECRET}         # Optional
      - run:
          name: Check contexts environment name
          shell: /bin/bash
          command: |
              if [[ ${CIRCLECISECRET} == 'circleci' ]]; then
                   echo "Switch context to circle"
                   exit 0
                 else 
                   echo "Switch context to githubactions"
              fi
              exit 99
```

3. Add this job at first in workflows

```
jobs:
    # Add this job to all workflows
    - disable-enable:
        context:
          - DisableEnable
```

4. Add require to every jobs in workflows

```
requires:
   - "disable-enable" # Add this requires jobs to all workflows
```
