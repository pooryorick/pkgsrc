# $NetBSD: Makefile,v 1.40 2017/01/28 12:09:14 wiz Exp $

DISTNAME=	pyOpenSSL-16.2.0
PKGNAME=	${PYPKGPREFIX}-${DISTNAME:S/py//}
CATEGORIES=	security python
MASTER_SITES=	${MASTER_SITE_PYPI:=p/pyOpenSSL/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/pyca/pyopenssl/
COMMENT=	Python interface to the OpenSSL library
LICENSE=	apache-2.0

DEPENDS+=	${PYPKGPREFIX}-cryptography>=0.3:../../security/py-cryptography
DEPENDS+=	${PYPKGPREFIX}-six>=1.5.2:../../lang/py-six
# TEST_DEPENDS
BUILD_DEPENDS+=	${PYPKGPREFIX}-test-[0-9]*:../../devel/py-test

.include "../../lang/python/egg.mk"
.include "../../security/openssl/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
