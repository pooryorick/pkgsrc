# $NetBSD: Makefile,v 1.8 2016/07/29 12:10:19 wen Exp $
#

DISTNAME=	Switch-2.17
PKGNAME=	p5-${DISTNAME}
CATEGORIES=	lang perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=../../authors/id/C/CH/CHORNY/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://search.cpan.org/dist/Switch/
COMMENT=	Switch statement for Perl
LICENSE=	${PERL5_LICENSE}

DEPENDS+=	p5-Text-Balanced-[0-9]*:../../textproc/p5-Text-Balanced
DEPENDS+=	p5-Filter-[0-9]*:../../textproc/p5-Filter

PERL5_PACKLIST=	auto/Switch/.packlist
USE_LANGUAGES=	# none

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
