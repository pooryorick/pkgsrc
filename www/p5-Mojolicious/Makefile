# $NetBSD: Makefile,v 1.116 2017/02/12 03:16:17 wen Exp $

DISTNAME=	Mojolicious-7.25
PKGNAME=	p5-${DISTNAME}
CATEGORIES=	www perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=Mojolicious/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://mojolicio.us/
COMMENT=	Perl web framework: The Web In A Box!
LICENSE=	artistic-2.0

USE_LANGUAGES=	# empty
PERL5_PACKLIST= auto/Mojolicious/.packlist

REPLACE_PERL+=	script/*

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
