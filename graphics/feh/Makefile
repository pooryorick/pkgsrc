# $NetBSD: Makefile,v 1.78 2017/01/27 12:04:08 szptvlfn Exp $

DISTNAME=	feh-2.18.1
CATEGORIES=	graphics
MASTER_SITES=	http://feh.finalrewind.org/
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://feh.finalrewind.org/
COMMENT=	Imlib2 based image viewer
LICENSE=	mit

USE_LANGUAGES=	c99

USE_TOOLS+=	gmake

LDFLAGS.SunOS+=		-lnsl -lsocket

BUILDLINK_DEPMETHOD.libXt?=	build

.include "../../sysutils/desktop-file-utils/desktopdb.mk"
.include "../../graphics/hicolor-icon-theme/buildlink3.mk"
.include "../../graphics/imlib2/buildlink3.mk"
.include "../../graphics/png/buildlink3.mk"
.include "../../www/curl/buildlink3.mk"
.include "../../x11/libXext/buildlink3.mk"
.include "../../x11/libXinerama/buildlink3.mk"
.include "../../x11/libXt/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
