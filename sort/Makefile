PROG =	sort
SRCS =	append.c fields.c files.c fsort.c init.c msort.c sort.c tmp.c
SRCS +=	radix_sort.c

CFLAGS.check +=	-Wno-error=unused-result # asprintf(...) and fread(...) on glibc/Linux-es

MKC_FEATURES +=	efun

.include <mkc.init.mk>

.include "../mk/hacks.mk"

.include "../mk/addlinks.mk"
