# $OpenBSD: Makefile,v 1.15 2020/02/22 19:56:05 bcallah Exp $

COMMENT =		3D light cycle game

DISTNAME =		armagetronad-0.2.8.3.5.src
PKGNAME =		${DISTNAME:S/.src//}

CATEGORIES =		games

HOMEPAGE =		http://armagetronad.org/
MAINTAINER =		Brian Callahan <bcallah@openbsd.org>

# GPLv2+
PERMIT_PACKAGE =		Yes

WANTLIB += GL GLU SDL SDL_image c iconv jpeg lzma m png pthread ${COMPILER_LIBCXX}
WANTLIB += xml2 z

COMPILER =		base-clang ports-gcc base-gcc

MASTER_SITES =		${MASTER_SITE_SOURCEFORGE:=armagetronad/}

BUILD_DEPENDS =		shells/bash
LIB_DEPENDS =		converters/libiconv \
			devel/sdl-image \
			textproc/libxml

USE_GMAKE =		Yes
CONFIGURE_STYLE =	gnu
CONFIGURE_ARGS +=	--enable-games=no \
			--enable-uninstall=no \
			--disable-useradd \
			--disable-initscripts \
			--disable-sysinstall \
			--disable-binreloc

WRKDIST =		${WRKDIR}/${DISTNAME:S/.src//}

.include <bsd.port.mk>
