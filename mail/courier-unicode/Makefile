# $NetBSD: Makefile,v 1.1 2017/02/12 02:14:01 mef Exp $

DISTNAME=	courier-unicode-1.4
CATEGORIES=	mail
MASTER_SITES=	https://sourceforge.net/projects/courier/files/courier-unicode/${PKGVERSION_NOREV}/
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.courier-mta.org/unicode/
COMMENT=	Implements several algorithms related to the Unicode Standard
LICENSE=	gnu-gpl-v3

USE_TOOLS+=	gmake autoconf aclocal automake
USE_LANGUAGES+=	c c++
GNU_CONFIGURE=	yes

pre-configure:
	(cd ${WRKSRC}; autoconf; aclocal; automake)

.include "../../mk/bsd.pkg.mk"
