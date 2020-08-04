## Nexus
npm private registry with Nexus

#### If you use binding mount volume, please assign permissions to storage.
```
chown -R 200 /some/dir/nexus-data
```

---

#### Default username and password
```
username: admin
password: (get from locate storage `admin.password` file)
```

---

#### Generate Basic Authentication
````
echo -n '<username>:<passowrd>' | base64
````
output :
```
YWRtaW46YWRtaW4=
```
copy to .npmrc
```
//localhost:8081/repository/npm-private/:_auth=YWRtaW46MTIzNDU2Nzg=
```

---

#### References
- [`https://levelup.gitconnected.com/deploying-private-npm-packages-to-nexus-a16722cc8166`](https://levelup.gitconnected.com/deploying-private-npm-packages-to-nexus-a16722cc8166)
- [`https://blog.sonatype.com/using-nexus-3-as-your-repository-part-2-npm-packages`](https://blog.sonatype.com/using-nexus-3-as-your-repository-part-2-npm-packages)
