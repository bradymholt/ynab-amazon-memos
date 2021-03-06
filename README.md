# ynab-utils

Some miscellaneous utilities for YNAB

## Setup

```
git clone https://github.com/bradymholt/ynab-utils.git
cd ynab-utils
cp ./config.json.example ./config.json
# Modify ./config.json
./ynab-utils
```

## Usage

```
USAGE

  ynab-utils <command> [options]

COMMANDS

  transactionImporter         Import transactions                                                 
  amazonMemoUpdator           Update Amazon transactions in YNAB with list of order items         
  transactionApprover         Auto-approves categorized transactions                              
  negativeBalanceRoller       Rolls negative balances from previous month forward to current month
  goalBudgeter                Budgets current month according to Goal Targets                     
  all                         Runs all commands                                                   
  help <command>              Display help for a specific command                                 

GLOBAL OPTIONS

  -h, --help         Display help                                      
  -V, --version      Display version                                   
  --no-color         Disable colors                                    
  --quiet            Quiet mode - only displays warn and error messages
  -v, --verbose      Verbose mode - will also output debug messages    
```

## Deployment

Run:

```shell
npm run deploy
```

Deployment is handled with an Ansible playbook located on the `ops/` folder.  The first time you run this command you will be prompted for deployment config values which will be saved to `ops/config.yml`.
