---
title: Az Azure Az PowerShell-moduljának bemutatása
description: Bemutatkozik az Azure-ral való interakcióhoz javasolt új Az PowerShell-modul, amely az AzureRM PowerShell-modult váltja le.
ms.date: 02/12/2021
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: b52b6995fb50a6ce502d42e7df588ca72340a1e7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409477"
---
# <a name="introducing-the-azure-az-powershell-module"></a>Az Azure Az PowerShell-moduljának bemutatása

## <a name="overview"></a>Áttekintés

Az Az PowerShell-modul olyan parancsmagok készletét kínálja, amelyekkel az Azure-erőforrások közvetlenül a PowerShellből kezelhetők. A PowerShell hatékony automatizálási funkciókat kínál, amelyek az Azure-erőforrások kezeléséhez használhatók például egy CI/CD-folyamat kapcsán.

Az Az PowerShell-modul az AzureRM-et váltja fel., és ez az ajánlott verzió az Azure-ral folytatott interakcióhoz.

Az Az PowerShell-modult az alábbi módszerek egyikével használhatja:

* [Telepítse az Az PowerShell-modult a PowerShellGet használatával](install-az-ps.md) (ajánlott módszer).
* [Telepítse az Az PowerShell-modult az MSI használatával](install-az-ps-msi.md).
* [Használja az Azure Cloud Shellt](/azure/cloud-shell/overview).
* [Használja az Az PowerShell Docker-tárolót](azureps-in-docker.md).

## <a name="features"></a>Funkciók

Az Az PowerShell-modul előnyei:

* Biztonság és stabilitás
  * Jogkivonat-gyorsítótár titkosítása
  * Közbeékelődéses támadások megelőzése
  * Hitelesítés támogatása az ADFS 2019-cel
  * Felhasználónév- és jelszó-hitelesítés a PowerShell 7-ben
  * A folyamatos hozzáférés-kiértékelés és hasonló funkciók támogatása (várható megjelenés: 2021)
* Az összes Azure-szolgáltatás támogatása
  * Az összes általánosan elérhető Azure-szolgáltatás rendelkezik megfelelő támogatott PowerShell-modullal
  * Számos hibajavítás és API-verziófrissítés az AzureRM óta
* Új képességek
  * Támogatás a Cloud Shellben és egyéb platformokon
  * Hozzáférési jogkivonatok lekérése és használata az Azure-erőforrások eléréséhez
  * Parancsmag érhető el az Azure-erőforrásokon végzett összetett REST-műveletekhez

> [!NOTE]
> A PowerShell az Az PowerShell-lel történő használatához az összes platformon a PowerShell 7-es vagy újabb verziója javasolt.

Az Az PowerShell-modul a .NET Standard-kódtáron alapul, és kompatibilis a PowerShell 7-es vagy újabb verziójával az összes platformon, beleértve a Windows, macOS és Linux rendszereket is. Ezenkívül a Windows PowerShell 5.1-es verziójával is kompatibilis.

Elkötelezettek vagyunk az Azure-támogatás valamennyi platformra történő kiterjesztésében, ezért az összes Az PowerShell-modul platformfüggetlen.

## <a name="upgrade-your-environment-to-az"></a>Frissítés Az-környezetre

Az Azure PowerShell-beli legfrissebb funkcióinak használatához érdemes áttérnie az Az modul használatára. Ha nem áll készen az Az modul telepítésére az AzureRM helyett, több lehetősége is van, hogy kipróbálja az Az modult:

* Használjon egy `PowerShell` környezetet az [Azure Cloud Shell-lel](/azure/cloud-shell/overview). Az Azure Cloud Shell egy böngészőalapú környezet, amely telepített Az modullal és engedélyezett `Enable-AzureRM` kompatibilitási aliasokkal rendelkezik.
* Tartsa meg a Windows PowerShell 5.1-es verziójával telepített AzureRM modult, és telepítse az Az modult a PowerShell 7-es vagy újabb verziójában. A Windows PowerShell 5.1 és a PowerShell 7-es és újabb verziói különböző modulgyűjteményeket használnak. Kövesse az utasításokat a [PowerShell legújabb verziójának](/powershell/scripting/install/installing-powershell) telepítéséhez, majd [telepítse az Az modult](install-az-ps.md) a PowerShell 7-es vagy újabb verziójából.

Frissítés meglévő AzureRM-telepítésből:

1. [Távolítsa el az Azure PowerShell AzureRM modult.](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
1. [Telepítse az Azure PowerShell Az modult.](install-az-ps.md)
1. **NEM KÖTELEZŐ**: Engedélyezze a kompatibilitási módot, hogy aliasokat adjon az AzureRM-parancsmagokhoz az [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) paranccsal, amíg meg nem ismeri az új parancskészletet. További információt a következő szakaszban vagy [az AzureRM modulból az Az modulba való migrálást](migrate-from-azurerm-to-az.md) ismertető cikkben talál.

## <a name="migrate-existing-scripts-from-azurerm-to-az"></a>Meglévő szkriptek migrálása az AzureRM-ből az Az modulba

Ha a szkriptjei még mindig az AzureRM modulon alapulnak, számos erőforrás áll rendelkezésre az Az modulba történő migrálás megkönnyítéséhez:

* [Az AzureRM-ből az Az modulba történő migrálás első lépései](migrate-from-azurerm-to-az.md)
* [Az AzureRM és az Az 1.0.0 közötti kompatibilitástörő változások teljes listája](migrate-az-1.0.0.md)
* Az [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) parancsmag

## <a name="supportability"></a>Támogatási lehetőségek

Az Azure legfrissebb PowerShell-modulja az Az. A hibákat vagy a funkciókéréseket közvetlenül a [GitHub-adattárban](https://github.com/Azure/azure-powershell) rögzítheti, vagy a Microsoft ügyfélszolgálatán keresztül is jelentheti, ha rendelkezik támogatási szerződéssel. A funkciókérések az Az legújabb verziójában lesznek implementálva. A kritikus hibák javítása az Az utolsó két verziójában lesz implementálva.

Mivel az az PowerShell-modulok már rendelkeznek a AzureRM PowerShell-modulok képességeivel, és így tovább, a AzureRM PowerShell-modulokat a 2024. február 29-én kivonják.

A szolgáltatás megszakadásának elkerülése érdekében frissítse a AzureRM PowerShell-modulokat használó [parancsfájlokat](https://aka.ms/azpsmigrate) az az PowerShell-modulok 2024. február 29-én való használatára. A parancsfájlok automatikus frissítéséhez kövesse a gyors [üzembe helyezési útmutatót](/powershell/azure/quickstart-migrate-azurerm-to-az-automatically).

## <a name="data-collection"></a>Adatgyűjtés

Az Azure PowerShell alapértelmezés szerint gyűjti a telemetriaadatokat. A Microsoft összesíti a gyűjtött adatokat a használati minták felismerése, a gyakori problémák észlelése és az Azure PowerShell nyújtotta felhasználói élmény javítása érdekében.
A Microsoft Azure PowerShell nem gyűjt magánjellegű vagy személyes adatokat. A használati adatok például olyan problémák azonosítására szolgálnak, mint az alacsony sikerességi arányú parancsmagok, és segítenek a feladataink fontossági sorrendjének kialakításában.

Habár nagyra értékeljük az adatokon alapuló megállapításokat, megértjük, hogy nem mindenki szeretné elküldeni a használati adatait. Az adatgyűjtést a [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection) parancsmaggal tilthatja le. További információt [adatvédelmi nyilatkozatunkban talál](https://privacy.microsoft.com/privacystatement).
