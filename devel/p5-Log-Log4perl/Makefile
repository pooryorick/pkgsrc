# $NetBSD: Makefile,v 1.30 2016/11/16 10:22:55 wiz Exp $

DISTNAME=	Log-Log4perl-1.48
PKGNAME=	p5-${DISTNAME}
CATEGORIES=	devel
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=Log/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://log4perl.sourceforge.net/
COMMENT=	Log4j implementation for Perl
LICENSE=	${PERL5_LICENSE}

PERL5_PACKLIST=	auto/Log/Log4perl/.packlist

REPLACE_PERL+=	lib/Log/Log4perl/Layout/PatternLayout/Multiline.pm

post-extract:
	${FIND} ${WRKSRC} -name "*.pm" -type f -exec ${CHMOD} -x {} \;

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
