# $NetBSD: Makefile,v 1.6 2017/01/12 00:48:24 rodent Exp $

DISTNAME=	ftfy-4.2.0
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	python textproc
MASTER_SITES=	${MASTER_SITE_PYPI:=f/ftfy/}

MAINTAINER=	rodent@NetBSD.org
HOMEPAGE=	http://github.com/LuminosoInsight/python-ftfy
COMMENT=	Fixes some problems with Unicode text after the fact
LICENSE=	mit

DEPENDS+=	${PYPKGPREFIX}-html5lib-[0-9]*:../../textproc/py-html5lib
DEPENDS+=	${PYPKGPREFIX}-wcwidth-[0-9]*:../../devel/py-wcwidth

USE_LANGUAGES=	# none

post-install:
	${MV} ${DESTDIR}${PREFIX}/bin/ftfy \
		${DESTDIR}${PREFIX}/bin/ftfy${PYVERSSUFFIX} || ${TRUE}

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
