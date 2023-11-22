API call to review a deployment:

curl -L \
  -X POST \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: token <YOUR-TOKEN>" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/repos/<YOUR-ORG>/<YOUR-REPO>/actions/runs/<RUN-ID>/pending_deployments \
  -d '{"environment_ids":[<YOUR-ENV-ID],"state":"<STATE>","comment":"<COMMENT"}'

API Call to trigger another workflow:

curl -X POST -H "Accept: application/json" \
        -H "Authorization: token <YOUR-TOKEN>" \
        https://api.github.com/repos/<YOUR-ORG>/<YOUR-REPO>/actions/workflows/<YOUR-WORKFLOW>/dispatches \
        -d '{"ref":"<BRANCH>", "inputs": {"message": "<MESSAGE>"}}'

