# $OpenBSD: Makefile,v 1.4 2020/07/03 21:12:29 sthen Exp $

MODPY_EGG_VERSION =	5.2.2
TRYTON_MODULE =		account_deposit
REVISION =		0

TRYTON_DEPENDS +=	account \
			account_invoice \
			company \
			party

RUN_DEPENDS +=		devel/py-dateutil${MODPY_FLAVOR} \
			databases/py-sql${MODPY_FLAVOR}

.include <bsd.port.mk>
