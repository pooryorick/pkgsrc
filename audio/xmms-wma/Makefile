# $NetBSD: Makefile,v 1.15 2016/04/20 12:10:35 nros Exp $
#

DISTNAME=	xmms-wma-1.0.5
PKGREVISION=	4
CATEGORIES=	audio
MASTER_SITES=	${MASTER_SITE_BACKUP}
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://mcmcc.bat.ru/xmms-wma/
COMMENT=	WMA input plugin for XMMS
LICENSE=	gnu-gpl-v2

ONLY_FOR_PLATFORM=	*-*-i386 # Doesn't seem to be very portable...

USE_TOOLS+=	gmake

.include "../../mk/bsd.prefs.mk"

.if ${OPSYS} != "Linux" # XXX
SUBST_CLASSES+=		rintf
SUBST_STAGE.rintf=	pre-configure
SUBST_FILES.rintf=	ffmpeg-strip-wma/wmadec.c
SUBST_SED.rintf=	-e "s,lrintf,rintf,g"
.endif

.include "../../audio/xmms/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
