# virtual-printer

Based on https://github.com/AIWIP/virtual-printer/

A virtual printer for testing your printing application. Supports IPP, SNMP and has web interface.

## Install dependencies
`npm install`

## Running
`node .`

## Testing SNMP
`snmpwalk -v 2c -c any localhost:1061`