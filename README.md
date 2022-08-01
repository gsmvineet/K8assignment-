# K8assignment-
Step 1:	kubectl delete pod db-b54cd94f4-hwpgj
Observation :  After deleting pod   voting result changed to 50 :50 Also Db pod restarted and running 1/1 

Step 2: kubectl delete pod result-5d57b59f4b-jnmk9
Observation : After deleting result pod  result pod cage to 0:100

step 3:kubectl delete po vote-94849dc97-4krdj
Observation : After deleting vote pod also the result page show 1 vote and change to after clicking on cat or dog. 

Step4 : kubectl delete pod worker-dd46d7584-5xjb9

Observation : voting and result app were reachable Also  data is  showing in result app. Also it was observed that worker podrestarted after db was restarted

Step 6 : all the pods restarted and running 1/1. Asked collegue to vote , checked the result tab is got cganged . 


3. your comment on WHY result app STOPPED working after db pod stop

Observation : Since i have already restatrted result pod  so in browser votting  & result tab both were working 

But actually after db pod restart DB pod data mount path was not available old DB1 was deleted and new DB created .
and result pod was showing socket error which we can seen from the kubectl logs command . 
Result pod was still trying to connect old DB1  instead of new DB. 

After restart the result pod it was connected with new DB. 
