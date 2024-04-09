# SPDX-License-Identifier: AGPL-3.0
#
# Maintainer: Pellegrino Prevete <pellegrinoprevete@gmail.com>
# Maintainer: Truocolo <truocolo@aol.com>
# Maintainer: Kewl <xrjy@nygb.rh.bet(rot13)>

_py="python"
_pkg="web3"
pkgname="${_py}-${_pkg}"
_pkgname="${_pkg}"
pkgver=5.31.3
pkgrel=1
pkgdesc=(
  "A Python library for interacting"
  "with Ethereum, inspired by web3.js"
)
pkgdesc="${pkgdesc[*]}"
arch=(
  'any'
)
depends=(
  "${_py}-aiohttp"
  "${_py}-eth-abi"
  "${_py}-eth-account"
  "${_py}-eth-hash"
  "${_py}-eth-typing"
  "${_py}-eth-utils"
  "${_py}-hexbytes"
  "${_py}-ipfshttpclient"
  "${_py}-jsonschema"
  "${_py}-lru-dict"
  "${_py}-protobuf"
  "${_py}-requests"
  "${_py}-websockets"
)
makedepends=(
  "${_py}-setuptools"
)
_http="https://github.com"
_ns="ethereum"
url="${_http}/${_ns}/${_pkgname}.py"
license=(
  'GPL3'
)
_pypi="https://files.pythonhosted.org/packages/source"
source=(
  "${_pypi}/${_pkg:0:1}/${_pkg}/${_pkg}-${pkgver}.tar.gz"
)
sha256sums=(
  '4b2d420647c81856e3cf398996cd3cc80c719dc3a10881884c5c3b1467e4f850'
)

build() {
  cd \
    "${_pkgname}-${pkgver}"
  "${_py}" \
    setup.py \
      build
}

package() {
  cd \
    "${_pkgname}-${pkgver}"
  "${_py}" \
    setup.py \
    install \
      --root="${pkgdir}" \
      --optimize=1 \
      --skip-build
}

# vim: ft=sh syn=sh et
