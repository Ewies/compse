root@debian:/Docker_Test# docker-compose up
Recreating 98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_dockertest_fhem_1 ...
Recreating 98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_dockertest_fhem_1 ... error

ERROR: for 98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_98f73ae03f4c_dockertest_fhem_1  No such image: sha256:ca2cbdc721a44e301c78be6ec72deead353296e47c6526848d873a9df7efd943

ERROR: for fhem  No such image: sha256:ca2cbdc721a44e301c78be6ec72deead353296e47c6526848d873a9df7efd943
ERROR: Encountered errors while bringing up the project.

version: '2'

services:
    fhem:
        expose:
            - "8083"
            - "7072"
        ports:
            - "8083:8083"
            - "7072:7072"
        image: steffen/fhem2
        privileged: true
