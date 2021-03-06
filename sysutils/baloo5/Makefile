# $NetBSD: Makefile,v 1.8 2017/02/12 06:24:49 ryoon Exp $

DISTNAME=	baloo-${KF5VER}
PKGNAME=	baloo5-${KF5VER}
PKGREVISION=	4
CATEGORIES=	sysutils

HOMEPAGE=	https://community.kde.org/Frameworks
COMMENT=	Framework for searching and managing metadata
LICENSE=	gnu-gpl-v2 AND gnu-lgpl-v2.1

.include "../../meta-pkgs/kf5/Makefile.common"

CONFLICTS+=	baloo-[0-9]*

BUILD_DEPENDS+=	kdoctools>=${KF5VER}:../../devel/kdoctools

USE_TOOLS+=	msgmerge

CONF_FILES+=    ${PREFIX}/share/examples/baloo5/baloo_file.desktop \
                ${PKG_SYSCONFDIR}/xdg/autostart/baloo_file.desktop

post-extract:
	cp ${FILESDIR}/FindLibinotify.cmake ${WRKSRC}/cmake/

SUBST_CLASSES+=		fix-moc
SUBST_STAGE.fix-moc=	post-configure
SUBST_MESSAGE.fix-moc=	Cleaning up MOC includes
SUBST_FILES.fix-moc=	_KDE_build/src/kioslaves/kded/CMakeFiles/baloosearchmodule_automoc.dir/AutogenInfo.cmake
SUBST_SED.fix-moc=	-e 's,;${PREFIX}/include;,;,g'

.include "../../mk/bsd.prefs.mk"

.if ${OPSYS} != "Linux"
.include "../../devel/libinotify/buildlink3.mk"
.endif
.include "../../databases/lmdb/buildlink3.mk"
.include "../../devel/kidletime/buildlink3.mk"
.include "../../devel/kio/buildlink3.mk"
.include "../../graphics/hicolor-icon-theme/buildlink3.mk"
.include "../../sysutils/kfilemetadata5/buildlink3.mk"
.include "../../x11/qt5-qtbase/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
