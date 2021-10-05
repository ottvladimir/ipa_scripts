# ipa_scripts

        curl -v  \
         -H referer:https://ipa.demo1.freeipa.org/ipa \
         -H "Content-Type:application/json" \
         -H "Accept:applicaton/json"\
         --negotiate -u : \
         --cacert /etc/ipa/ca.crt  \ 
         -d  '{"method":"user_find","params":[[""],{}],"id":0}' \
         -X POST https://ipa.demo1.freeipa.org/ipa/json
