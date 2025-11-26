  workflows defind into `.github/workflows` dir.

  ```yml
name: your workflow name
on: add action
jobs: # define list of jobs
  first-job: # Job name
    runs-on: ubuntu-22.04 # platerform_to_run_the_Runner
    steps: # what steps you want ?
      - name: print greeting
        run: echo "Hello World!"
      - name: print uptime
        run: uptime