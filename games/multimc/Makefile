# $OpenBSD: Makefile,v 1.1.1.1 2020/09/21 07:22:37 kmos Exp $

COMMENT =		free and open-source launcher for Minecraft

# git clone --recurse-submodules -b 0.6.11 https://github.com/MultiMC/MultiMC5
DISTNAME =		multimc-0.6.11
MASTER_SITES =		https://distfiles.yukiisbo.red/

CATEGORIES =		games

HOMEPAGE =		https://multimc.org

MAINTAINER =		Muhammad Kaisar Arkhan <hi@yukiisbo.red>

# Apache 2.0
PERMIT_PACKAGE =	Yes

WANTLIB +=		${COMPILER_LIBCXX} Qt5Concurrent Qt5Core Qt5Gui
WANTLIB +=		Qt5Network Qt5Widgets Qt5Xml c m z

MODULES =		devel/cmake \
			x11/qt5 \
			java
MODJAVA_VER =		1.8

RUN_DEPENDS =		audio/openal \
			games/lwjgl \
			java/javaPathHelper

CXXFLAGS +=	-DLWJGL_DIR='\"${LOCALBASE}/share/lwjgl/\"' \
		-DJAVAPATHHELPER_PATH='\"${LOCALBASE}/bin/javaPathHelper\"'

CONFIGURE_ARGS =	-DMultiMC_LAYOUT="lin-system"

WRKDIST =		${WRKDIR}/MultiMC5

.include <bsd.port.mk>
