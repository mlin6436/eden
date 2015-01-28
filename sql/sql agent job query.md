# Determine How Long a SQL Agent Job Has Been Running

As a DBA, it is important to know how long certain or all SQL agent jobs has been running on the server. Here is a helping query:

```sql
SELECT DATEDIFF(SECOND,aj.start_execution_date,GetDate()) AS Seconds
FROM msdb..sysjobactivity aj
JOIN msdb..sysjobs sj on sj.job_id = aj.job_id
WHERE aj.stop_execution_date IS NULL -- job hasn't stopped running
AND aj.start_execution_date IS NOT NULL -- job is currently running
AND sj.name = <sql_agent_job>
and not exists( -- make sure this is the most recent run
    select 1
    from msdb..sysjobactivity new
    where new.job_id = aj.job_id
    and new.start_execution_date > aj.start_execution_date
)
```
