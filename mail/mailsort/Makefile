# $NetBSD: Makefile,v 1.5 2016/07/09 06:38:30 wiz Exp $
#

DISTNAME=	mailsort-1.26
PKGREVISION=	4
CATEGORIES=	mail
MASTER_SITES=	http://search.cpan.org/CPAN/authors/id/A/AZ/AZS/mailsort/

MAINTAINER=	reed@reedmedia.net
HOMEPAGE=	http://search.cpan.org/~azs/mailsort/
COMMENT=	Sort mbox mail folders by date

LICENSE=	gnu-gpl-v2

INSTALLATION_DIRS=	bin ${PKGMANDIR}/man1
REPLACE_PERL+=	mailsort
USE_LANGUAGES=	# none
USE_TOOLS=	perl pod2man

do-build:
	pod2man ${WRKSRC}/mailsort > ${WRKSRC}/mailsort.1

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/mailsort ${DESTDIR}${PREFIX}/bin/
	${INSTALL_MAN} ${WRKSRC}/mailsort.1 \
		${DESTDIR}${PREFIX}/${PKGMANDIR}/man1/

.include "../../mk/bsd.pkg.mk"
