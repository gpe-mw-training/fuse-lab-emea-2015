GPE JBoss Fuse Lab
==================

This is a GPE JBoss Fuse Lab

HTTPie request
==============

http POST http://127.0.0.1:9191/entries/new < src//data/entry.json




fabric:create --clean root

fabric:container-create-child --profile insight-elasticsearch.datastore root elasticsearch-node
fabric:container-create-child --profile insight-core root elasticsearch-node
fabric:container-create-child --profile feature-camel root lab

fabric:container-add-profile lab gpe-fuse

fabric:container-remove-profile lab gpe-fuse