# junk2

```
-- Who raised it and who is named
SELECT wr.id, wr.project_name, req.full_name AS requester, hod.full_name AS hod, gm.full_name AS gm
FROM xxx wr
LEFT JOIN users req ON req.id = wr.requester_user_id
LEFT JOIN users hod ON hod.id = wr.hod_approver_user_id
LEFT JOIN users gm  ON gm.id  = wr.gm_approver_user_id
WHERE wr.project_name ILIKE '%<project name>%';

-- Who set or changed the approvers
SELECT a.created_at, a.action, u.full_name AS actor, a.old_value, a.new_value
FROM yyy a LEFT JOIN users u ON u.id = a.actor_user_id
WHERE a.entity_id = 
ORDER BY a.created_at;


```
