PROG =	xinstall
SRCS =	xinstall.c getid.c
MAN  =	install.1

.PATH:		${.CURDIR}/../mtree
CPPFLAGS +=	-I${.CURDIR}/../mtree -I${.CURDIR}/

CPPFLAGS +=	-DHAVE_NBTOOL_CONFIG_H

COPTS.xinstall.c += -Wno-format-nonliteral

PROGNAME ?=	install

.include <mkc.init.mk>

CFLAGS.check   +=	-Wno-error=deprecated-declarations
CFLAGS.check   +=	-Wno-error=unused-result # write(...) on glibc/Linux-es
CFLAGS.check   +=	-erroff=E_DEPRECATED_ATT # vfork(2) on SunOS

.if ${TARGET_OPSYS} == "SunOS"
CFLAGS.check   +=	-Wno-error=pointer-sign
.endif

.include "../mk/hacks.mk"

.include "../mk/imp.f_getsetmode.mk"
.include "../mk/imp.f_pwdgrp.mk"
.include "../mk/imp.f_flags_to_string.mk"
.include "../mk/imp.f_lchmod.mk"
.include "../mk/imp.f_struct_stat.mk"

MKC_FEATURES +=	fparseln LIST strsep vis

.include "../mk/addlinks.mk"
