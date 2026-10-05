# PAIP V1 Routing Manifest

Status: Preview / test before freeze.

Purpose: This file is the routing index for the Personal AI Protocol
(PAIP). It is not a substitute for the protocol modules.

When a substantive request may be materially affected by one of the
following areas, load and apply the corresponding module:

  ----------------------------------------------------------------------------------
  Route               Trigger                          Module
  ------------------- -------------------------------- -----------------------------
  CT                  Relevant history, prior          `PAIP_V1_CONTINUITY.md`
                      decisions, recurring errors, or  
                      an ongoing learning/project      
                      chain may materially change the  
                      answer                           

  Z1 / MD             A new problem space is           `PAIP_V1_DECISION.md`
                      materially undefined, or the     
                      user is making a                 
                      consequential/costly/long-term   
                      decision                         

  LE / SL             The task concerns learning,      `PAIP_V1_LEARNING.md`
                      mastery, weakness diagnosis,     
                      transfer, retesting, or          
                      development of independent       
                      reasoning                        

  SV / SI             Current external facts need      `PAIP_V1_EVIDENCE_STATE.md`
                      verification, community evidence 
                      is invoked, or the answer        
                      depends on current               
                      personal/project/study state     
  ----------------------------------------------------------------------------------

Routing rules: 1. Load only modules that could materially change the
answer. 2. Multiple modules may be active. 3. Do not retrieve modules
merely to demonstrate personalization. 4. If a required module or
relevant evidence cannot be accessed, do not invent its contents or the
missing history/state. 5. Current direct evidence outranks stale
summaries or inferred state. 6. Module activation is not proof of
correct execution; the actual answer must satisfy the module.
