# $NetBSD: Makefile,v 1.4 2017/02/12 06:24:55 ryoon Exp $

DISTNAME=	kxmlgui-${KF5VER}
PKGREVISION=	3
CATEGORIES=	x11

HOMEPAGE=	https://community.kde.org/Frameworks
COMMENT=	User configurable main windows
LICENSE=	gnu-gpl-v2 AND gnu-lgpl-v2.1

.include "../../meta-pkgs/kf5/Makefile.common"

USE_TOOLS+=	msgmerge

MAKE_DIRS+=	${PKG_SYSCONFDIR}/xdg/ui
CONF_FILES+=	${PREFIX}/share/examples/kxmlgui/ui_standards.rc \
		${PKG_SYSCONFDIR}/xdg/ui/ui_standards.rc

.include "../../lang/python/tool.mk"
.include "../../misc/attica-qt5/buildlink3.mk"
.include "../../x11/kglobalaccel/buildlink3.mk"
.include "../../x11/ktextwidgets/buildlink3.mk"
.include "../../x11/qt5-qtbase/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
