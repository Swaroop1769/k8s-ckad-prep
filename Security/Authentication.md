- All user access is managed by API server, whether accessing cluster through kubectl tool or API directly

The **kube-apiserver** authenticates users before processing it.

Different Authentication mechanisms:

1. Static Password File  // not recommended approach 
2. Static Token File
3. Certificates
4. Identity Services



