# Maintainer: Corey Hinshaw <coreyhinshaw@gmail.com>
# Contributor: zer0def <zer0def@github>

pkgname=luks-tpm
pkgver=0.3.0
pkgrel=1
pkgdesc="Utility to manage LUKS keyfiles sealed by the TPM"
arch=('any')
url="https://github.com/electrickite/luks-tpm"
license=('GPL')
depends=('tpm-tools' 'trousers' 'cryptsetup' 'bash' 'coreutils' 'gawk' 'util-linux')
install="${pkgname}.install"
backup=('etc/default/luks-tpm')

source=("${pkgname}" 'default' "${pkgname}.hook")
sha512sums=(
  '0a60f85a5c06bc7224769c9a700ba526a6a5ffcfd74cb0c44ecd3d6a2c7efdc7340c3a611fd0377df0b7654de8d4550348c3f7f0d10050b296d32ff6234d1f5e'
  '378b6421e8c1a5a53da4aaeda0fc607cd2ad6c842611f47c393f5f5744ceb6dce99c29241d97f9eaae09a4a4780f6163b67ab2f5bd8c97a1cda2a26a28674f62'
  '840168b9c8e9d40431beac01e389b61e9456007a71d2b80d518f493002a3655e3c01ef78cf17557790f0c5deeca415e70ef8690f2aa49369e5cdc04bea7897b6'
)
b2sums=(
  'd5a35f23fd09cdbfd035242835ed2983f0ca188847e5c3d2e63985b8a6f0dded20d759e8f6a7d903bb6a8c110bc2b964cf77607ec7b35bb9aab241d87657b7a9'
  'a463fee2156732a2cfc61d458566bb6de20ae66ca9fa85fb25025c8784effff0fe96c55be5ba9ebecf7266fd605d5090abc5235eeb7df43e240ee65542bb889e'
  '7eb4b30b4bde5f296a53027bcf230944c966d7dcabcd161abb51e0e368ca3190f8a06ddea442cdd7465fb965f87c68477c583276f910c0f0c84f6c2f2fe1882c'
)

package() {
  install -Dm755 "${srcdir}/luks-tpm" "${pkgdir}/usr/bin/luks-tpm"
  install -Dm644 "${srcdir}/default" "${pkgdir}/etc/default/luks-tpm"
  install -Dm644 "${srcdir}/luks-tpm.hook" "${pkgdir}/usr/share/libalpm/hooks/luks-tpm.hook"
}
