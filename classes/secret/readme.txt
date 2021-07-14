encrypt secret key
echo -n "User" | base64


decode key
echo -n "key" | base64 --decode


Create secret
kubectl create secret generic mysecret --from-file=username.txt --from-file=password.txt
