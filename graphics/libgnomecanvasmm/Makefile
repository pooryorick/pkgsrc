# $NetBSD: Makefile,v 1.42 2017/02/12 06:24:45 ryoon Exp $

DISTNAME=	libgnomecanvasmm-2.26.0
PKGREVISION=	25
CATEGORIES=	graphics
MASTER_SITES=	${MASTER_SITE_GNOME:=sources/libgnomecanvasmm/2.26/}
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	adam@NetBSD.org
HOMEPAGE=	http://gtkmm.sourceforge.net/
COMMENT=	C++ bindings for libgnomecanvas

USE_LANGUAGES=		c c++
CXXFLAGS+=		-std=c++11
USE_LIBTOOL=		yes
USE_PKGLOCALEDIR=	yes
USE_TOOLS+=		gm4 gmake pkg-config
PKGCONFIG_OVERRIDE+=	${WRKSRC}/libgnomecanvas/libgnomecanvasmm-2.6.pc.in
GNU_CONFIGURE=		yes

.include "../../graphics/libgnomecanvas/buildlink3.mk"
.include "../../x11/gtkmm/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
