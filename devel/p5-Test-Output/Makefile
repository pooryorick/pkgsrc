# $NetBSD: Makefile,v 1.21 2016/06/08 19:23:39 wiz Exp $

DISTNAME=	Test-Output-1.03
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	5
CATEGORIES=	devel perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=Test/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://search.cpan.org/dist/Test-Output/
COMMENT=	Utilities to test STDOUT and STDERR messages
LICENSE=	artistic-2.0

DEPENDS+=	p5-Sub-Exporter-[0-9]*:../../devel/p5-Sub-Exporter
DEPENDS+=	p5-Capture-Tiny>=0.17:../../devel/p5-Capture-Tiny
DEPENDS+=	p5-Test-Simple-[0-9]*:../../devel/p5-Test-Simple

PERL5_PACKLIST=		auto/Test/Output/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
