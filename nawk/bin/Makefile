DIST =		${.CURDIR}/../dist
.PATH:		${DIST}

PROG =		awk
SRCS =		awkgram.y b.c lex.c lib.c main.c parse.c proctab.c run.c tran.c

WARNS   =	3
WARNERR =	no

CPPFLAGS +=	-I${DIST} -I${.OBJDIR} -I${.CURDIR}
YHEADER   =	yes
#COPTS.run.c+=	-Wno-format-nonliteral
#COPTS.tran.c+=	-Wno-format-nonliteral

MKC_FEATURES +=	libm

.include "../../mk/addlinks.mk"

CFLAGS.check +=	-Wno-self-assign
CFLAGS.check +=	-Wno-pointer-sign
