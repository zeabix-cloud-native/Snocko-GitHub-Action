# Readme for Disable or Enable CircleCI Workflows
1. Create organization contexts environment variable 

  Name  = ` BRANCH `
  
  Value = ` main ` for Enable workflows (If github repository branch = main)
          ` {any words or string} ` for Disable workflows

2. Insert this job to first job

```
# Add this job to all workflows
  disable-enable:
    docker:
      - image: 'cimg/base:stable'
    steps:
      - run: echo ${BRANCH}         # Optional
      - run: echo ${CIRCLE_BRANCH}  # Optional
      - run:
          name: Check contexts environment name
          shell: /bin/bash
          command: |
              if [[ $CIRCLE_BRANCH == $BRANCH ]]; then
                   echo "Branch match --> go go go"
                   exit 0
                 else 
                   echo "Branch miss match --> STOP!!!"
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
