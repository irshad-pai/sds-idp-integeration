# Keycloak

Two keycloak servers to configure multiple Identity Providers, in order to bring users from external buckets with no need for users to go through the registration process.

The information can be found in this article: 

https://antonioberben.gitlab.io/website/posts/keycloak-idp/


http://sds.idp.com:8180/auth/realms/master/protocol/openid-connect/auth?client_id=sds-insight-api&scope=openid&response_type=code&redirect_uri=http://localhost:8000/sds.html


http://sds.idp.com:8180/auth/realms/master/protocol/openid-connect/auth?client_id=sds-insight-api&redirect_uri=http://localhost:8000/sds.html&scope=openid&response_type=code


Keycloak007
keycloakkey591@gmail.com



access_token=`curl http://sds.idp.com:8180/auth/realms/master/protocol/openid-connect/token -XPOST -d 'grant_type=client_credentials' -u 'admin:admin' | jq -r .access_token`
