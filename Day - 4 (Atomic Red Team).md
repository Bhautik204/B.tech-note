steps:
Get-Help Invoke-Atomictest
Invoke-AtomicTest T1566.001 -ShowDetails
Invoke-AtomicTest T1566.001 -TestNumbers 1 -CheckPrereq
Invoke-AtomicTest T1566.001 -TestNumbers 2 -CheckPrereq
`Invoke-AtomicTest T1566.001 -TestNumbers 1` 
`Invoke-AtomicTest T1566.001 -TestNumbers 1 -cleanup`.
go in event viewer  then click application and services
then select Microsoft > windows > sysmom > and clear log
`Invoke-AtomicTest T1566.001 -TestNumbers 1` 
then in C: > users > administration > appdata > local > temp  their is flag in txt file
`Invoke-AtomicTest T1566.001-1 -cleanup`.
Invoke-AtomicTest T1059.003 -ShowDetails
`Invoke-AtomicTest T1059.003 -TestNumber 4` run cmd save as ransome and extract flag
#AOC 
