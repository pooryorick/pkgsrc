# $NetBSD: Makefile,v 1.4 2017/02/12 06:24:38 ryoon Exp $

DISTNAME=	kcrash-${KF5VER}
PKGREVISION=	3
CATEGORIES=	devel

HOMEPAGE=	https://community.kde.org/Frameworks
COMMENT=	Support for application crash analysis and bug report from apps
LICENSE=	gnu-lgpl-v2.1

.include "../../meta-pkgs/kf5/Makefile.common"

.include "../../devel/kcoreaddons/buildlink3.mk"
.include "../../x11/kwindowsystem/buildlink3.mk"
.include "../../x11/qt5-qtbase/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
