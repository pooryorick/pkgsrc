# $NetBSD: Makefile,v 1.7 2016/09/30 13:09:10 wiz Exp $

DISTNAME=		adwaita-icon-theme-3.22.0
CATEGORIES=		graphics gnome
MASTER_SITES=		${MASTER_SITE_GNOME:=/sources/adwaita-icon-theme/3.22/}
EXTRACT_SUFX=		.tar.xz

MAINTAINER=		prlw1@cam.ac.uk
HOMEPAGE=		http://www.gnome.org/
COMMENT=		Standard GNOME icons
LICENSE=		cc-by-sa-v3.0 OR gnu-lgpl-v3

TOOL_DEPENDS+=		librsvg>=2.22.3:../../graphics/librsvg
# for gtk-encode-symbolic-svg
TOOL_DEPENDS+=		gtk3+>=3:../../x11/gtk3

GNU_CONFIGURE=		yes
USE_TOOLS+=		gmake pkg-config
# otherwise it creates lots of superfluous lib/locale dirs
USE_PKGLOCALEDIR=	yes
TOOLS_NOOP+=		gtk-update-icon-cache

PKGCONFIG_OVERRIDE+=	adwaita-icon-theme.pc.in

# should be created by the upstream installation Makefile targets,
# but isn't
INSTALLATION_DIRS+=	share/icons/Adwaita/96x96/places

FILES_SUBST+=		GTK_UPDATE_ICON_CACHE="${LOCALBASE}/bin/gtk-update-icon-cache"
FILES_SUBST+=		ICON_THEME_DIR="${LOCALBASE}/share/icons/Adwaita"
INSTALL_TEMPLATES+=	../../graphics/adwaita-icon-theme/files/icon-cache.tmpl
DEINSTALL_TEMPLATES+=	../../graphics/adwaita-icon-theme/files/icon-cache.tmpl
PRINT_PLIST_AWK+=	/^share\/icons\/gnome\/icon-theme.cache$$/ { next; }

post-install:
.for s in 16 22 24 32 48 96 256
	 ${LOCALBASE}/bin/rsvg-convert ${FILESDIR}/distributor-logo.svg \
	 -w ${s} -h ${s} -o \
	 ${DESTDIR}${PREFIX}/share/icons/Adwaita/${s}x${s}/places/start-here.png
.endfor

BUILDLINK_DEPMETHOD.gettext-lib=        build
.include "../../devel/gettext-lib/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
