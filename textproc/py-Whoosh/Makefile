# $NetBSD: Makefile,v 1.11 2017/01/01 14:44:00 wiz Exp $
#

DISTNAME=	Whoosh-2.5.7
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	textproc devel
MASTER_SITES=	${MASTER_SITE_PYPI:=W/Whoosh/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://whoosh.ca/
COMMENT=	Fast, featureful full-text indexing and searching library implemented
LICENSE=	apache-2.0

USE_LANGUAGES=		# none

PYTHON_VERSIONS_INCOMPATIBLE=	34 35 36

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
