# $NetBSD: Makefile,v 1.22 2017/02/12 06:25:03 ryoon Exp $

DISTNAME=	gmpc-wikipedia-11.8.16
PKGREVISION=	18
CATEGORIES=	audio
MASTER_SITES=	http://download.sarine.nl/Programs/gmpc/11.8/
MASTER_SITES+=	${MASTER_SITE_SOURCEFORGE:=musicpd/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://gmpc.wikia.com/wiki/GMPC_PLUGIN_WIKIPEDIA
COMMENT=	Plugin for GMPC showing the currently playing artist's Wikipedia page
LICENSE=	gnu-gpl-v2

GNU_CONFIGURE=	yes
USE_LIBTOOL=	yes
USE_TOOLS+=	intltool pkg-config xgettext

.include "../../audio/gmpc/buildlink3.mk"
.include "../../www/webkit24-gtk/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
