# $NetBSD: Makefile,v 1.87 2017/02/12 06:24:48 ryoon Exp $

DISTNAME=	gnome-keyring-2.32.1
PKGREVISION=	22
CATEGORIES=	security gnome
MASTER_SITES=	${MASTER_SITE_GNOME:=sources/gnome-keyring/2.32/}
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.gnome.org/
COMMENT=	GNOME password and secret manager

USE_TOOLS+=		gmake intltool msgfmt pkg-config
GNU_CONFIGURE=		YES
USE_LIBTOOL=		YES
USE_PKGLOCALEDIR=	YES

PKGCONFIG_OVERRIDE+=	gcr/gcr.pc.in
PKGCONFIG_OVERRIDE+=	gp11/gp11.pc.in

CFLAGS.HPUX+=		-DMAP_ANON=MAP_ANONYMOUS

# Workaround a bug with NetBSD's openpam
# The bug is described in PR security/39313
#
CFLAGS.NetBSD+=		-DNO_STATIC_MODULES

CONFIGURE_ENV.SunOS+=	ac_cv_header_security_pam_modules_h=yes

.include "../../mk/dlopen.buildlink3.mk"

BUILDLINK_TRANSFORM+=	opt:-ldl:${BUILDLINK_LDADD.dl:M*}

BUILDLINK_API_DEPENDS.glib2+=	glib2>=2.26.0
.include "../../devel/glib2/schemas.mk"
.include "../../devel/gettext-lib/buildlink3.mk"
.include "../../devel/glib2/buildlink3.mk"
.include "../../security/libgcrypt/buildlink3.mk"
.include "../../security/libtasn1/buildlink3.mk"
.include "../../sysutils/dbus/buildlink3.mk"
.include "../../x11/gtk2/buildlink3.mk"
.include "../../mk/pam.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
