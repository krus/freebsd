# $FreeBSD$
.PATH:  ${.CURDIR}/../../ofed/drivers/infiniband/core
.PATH:  ${.CURDIR}/../../ofed/include/linux

KMOD=	ibcore
SRCS=	addr.c iwcm.c sa_query.c ucma.c uverbs_cmd.c \
	agent.c local_sa.c multicast.c smi.c ud_header.c uverbs_main.c \
	mad.c notice.c umem.c uverbs_marshall.c \
	cache.c device.c packer.c sysfs.c user_mad.c verbs.c \
	cm.c fmr_pool.c mad_rmpp.c ucm.c cma.c \
	vnode_if.h device_if.h bus_if.h pci_if.h \
	opt_inet.h opt_inet6.h

CFLAGS+= -I${.CURDIR}/../../ofed/drivers/infiniband/core
CFLAGS+= -I${.CURDIR}/../mlx4ib
CFLAGS+= -I${.CURDIR}/../../ofed/include/
CFLAGS+= -DINET6 -DINET

.include <bsd.kmod.mk>

CFLAGS+= -Wno-cast-qual -Wno-pointer-arith ${GCC_MS_EXTENSIONS}

CWARNFLAGS.cm.c=	-Wno-unused-function
