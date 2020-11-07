---
Module Name: Az.DataLakeStore
Module Guid: 90dfd814-abce-4e1f-99b6-fe16760c079a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Az.DataLakeStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Az.DataLakeStore.md
ms.openlocfilehash: 5796a3692274db9b49ed16c00935ed1cd2d4e8f0
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/15/2019
ms.locfileid: "93665506"
---
# Az. DataLakeStore modul
## Leírás
Az ebben a szakaszban szereplő témakörök az Azure-alapú Lake Store Azure PowerShell-parancsmagjai az Azure Resource Manager (ARM) keretrendszerben című témakörben olvashatók. A parancsmagok a Microsoft. Azure. commands. DataLakeStore névtérben találhatók. Ezek a parancsmagok csak az Azure Data Lake Storage Gen1-fiókjaival működnek.

## Az. DataLakeStore parancsmagok
### [Add-AzDataLakeStoreFirewallRule](Add-AzDataLakeStoreFirewallRule.md)
Tűzfal-szabály felvétele a megadott Data Lake Store-fiókba.

### [Add-AzDataLakeStoreItemContent](Add-AzDataLakeStoreItemContent.md)
Tartalmat ad az adattó-tároló elemeihez.

### [Add-AzDataLakeStoreTrustedIdProvider](Add-AzDataLakeStoreTrustedIdProvider.md)
A megadott Data Lake Store-fiókhoz hozzáadja a megbízható identitás-szolgáltatót.

### [Add-AzDataLakeStoreVirtualNetworkRule](Add-AzDataLakeStoreVirtualNetworkRule.md)
Virtuális hálózati szabály felvétele a megadott Data Lake Store-fiókba.

### [Enable-AzDataLakeStoreKeyVault](Enable-AzDataLakeStoreKeyVault.md)
Megkísérli engedélyezni a felhasználó által felügyelt kulcs boltozatát a megadott Data Lake Store-fiók titkosításához.

### [Exportálás – AzDataLakeStoreChildItemProperty](Export-AzDataLakeStoreChildItemProperty.md)
A tulajdonságok (a lemezhasználat és az ACL) exportálása a kijelölt útvonalról a kimeneti elérési útra a teljes fához

### [Exportálás – AzDataLakeStoreItem](Export-AzDataLakeStoreItem.md)
Az adattó áruházból letölt egy fájlt.

### [Get-AzDataLakeStoreAccount](Get-AzDataLakeStoreAccount.md)
Adatokat kap az adattó áruházbeli fiókról.

### [Get-AzDataLakeStoreChildItem](Get-AzDataLakeStoreChildItem.md)
Az elemek listájának beolvasása az adattó áruházban lévő mappákban.

### [Get-AzDataLakeStoreChildItemSummary](Get-AzDataLakeStoreChildItemSummary.md)
A megadott elérési úton lévő teljes méret, fájlok és könyvtárak összegzése

### [Get-AzDataLakeStoreFirewallRule](Get-AzDataLakeStoreFirewallRule.md)
A megadott tűzfalszabályok beolvasása a megadott adattó-tárolóban.
Ha nem adja meg a tűzfal szabályát, akkor a rendszer megjeleníti a fiókhoz tartozó összes tűzfal-szabályt.

### [Get-AzDataLakeStoreItem](Get-AzDataLakeStoreItem.md)
Az adattó áruházban lévő fájlok vagy mappák részleteit kapja meg.

### [Get-AzDataLakeStoreItemAclEntry](Get-AzDataLakeStoreItemAclEntry.md)
Beilleszt egy bejegyzést az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájába.

### [Get-AzDataLakeStoreItemContent](Get-AzDataLakeStoreItemContent.md)
A fájl tartalmának beolvasása az adattó áruházban.

### [Get-AzDataLakeStoreItemOwner](Get-AzDataLakeStoreItemOwner.md)
Az adattó áruházban lévő fájl vagy mappa tulajdonosát kapja meg.

### [Get-AzDataLakeStoreItemPermission](Get-AzDataLakeStoreItemPermission.md)
Az adattó-tárolóban lévő fájl vagy mappa engedélyét adja meg.

### [Get-AzDataLakeStoreTrustedIdProvider](Get-AzDataLakeStoreTrustedIdProvider.md)
A megadott adattárolóban kapja meg a megadott megbízható identitás-szolgáltatót.
Ha nem ad meg szolgáltatót, akkor a fiók összes szolgáltatóját listázhatja.

### [Get-AzDataLakeStoreVirtualNetworkRule](Get-AzDataLakeStoreVirtualNetworkRule.md)
A megadott virtuális hálózati szabályok beolvasása a megadott Data Lake Store áruházban.
Ha nincs megadva virtuális hálózati szabály, akkor a rendszer megjeleníti a fiókhoz tartozó összes virtuális hálózati szabályt.

### [Importálás – AzDataLakeStoreItem](Import-AzDataLakeStoreItem.md)
Helyi fájlt vagy könyvtárat tölt fel egy adattó-áruházba.

### [Bekapcsolódás a AzDataLakeStoreItem](Join-AzDataLakeStoreItem.md)
Csatlakozik egy vagy több fájlhoz egy fájl létrehozásához az adattó áruházban.

### [Move-AzDataLakeStoreItem](Move-AzDataLakeStoreItem.md)
Egy fájl vagy mappa áthelyezése vagy átnevezése az adattó áruházban.

### [Új – AzDataLakeStoreAccount](New-AzDataLakeStoreAccount.md)
Új Data Lake Store-fiók létrehozása

### [Új – AzDataLakeStoreItem](New-AzDataLakeStoreItem.md)
Új fájlt vagy mappát hoz létre az adattó áruházban.

### [Remove-AzDataLakeStoreAccount](Remove-AzDataLakeStoreAccount.md)
Véglegesen törli az adattó-tároló fiókját.

### [Remove-AzDataLakeStoreFirewallRule](Remove-AzDataLakeStoreFirewallRule.md)
A megadott tűzfalszabályok eltávolítása a megadott Data Lake Store-ban.

### [Remove-AzDataLakeStoreItem](Remove-AzDataLakeStoreItem.md)
Töröl egy fájlt vagy mappát az adattó áruházból.

### [Remove-AzDataLakeStoreItemAcl](Remove-AzDataLakeStoreItemAcl.md)
Törli az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listáját.

### [Remove-AzDataLakeStoreItemAclEntry](Remove-AzDataLakeStoreItemAclEntry.md)
Az adattó-tárolóban lévő fájl vagy mappa HOZZÁFÉRÉSének a bejegyzését távolítja el.

### [Remove-AzDataLakeStoreTrustedIdProvider](Remove-AzDataLakeStoreTrustedIdProvider.md)
A megadott megbízható identitás-szolgáltató eltávolítása a megadott Data Lake Store áruházból.

### [Remove-AzDataLakeStoreVirtualNetworkRule](Remove-AzDataLakeStoreVirtualNetworkRule.md)
A megadott virtuális hálózati szabály eltávolítása a megadott Data Lake Store-ból.

### [Set-AzDataLakeStoreAccount](Set-AzDataLakeStoreAccount.md)
Az adattó-tároló fiók módosítása.

### [Set-AzDataLakeStoreFirewallRule](Set-AzDataLakeStoreFirewallRule.md)
A megadott tűzfalszabályok módosítása a megadott adattó-tárolóban.

### [Set-AzDataLakeStoreItemAcl](Set-AzDataLakeStoreItemAcl.md)
Módosítja az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listáját.

### [Set-AzDataLakeStoreItemAclEntry](Set-AzDataLakeStoreItemAclEntry.md)
Módosította az adattó-tárolóban lévő fájl vagy mappa HOZZÁFÉRÉSének bejegyzését.

### [Set-AzDataLakeStoreItemExpiry](Set-AzDataLakeStoreItemExpiry.md)
Egy Azure Data Lake Store-fiókban lévő fájl elévülési idejének beállítása vagy eltávolítása.

### [Set-AzDataLakeStoreItemOwner](Set-AzDataLakeStoreItemOwner.md)
Módosítja egy fájl vagy mappa tulajdonosát az adattó-áruházban.

### [Set-AzDataLakeStoreItemPermission](Set-AzDataLakeStoreItemPermission.md)
Módosította az adattó-tárolóban lévő fájlok vagy mappák engedélyének oktális részét.

### [Set-AzDataLakeStoreTrustedIdProvider](Set-AzDataLakeStoreTrustedIdProvider.md)
Módosította a megadott megbízható identitás-szolgáltatót a megadott Data Lake Store-ban.

### [Set-AzDataLakeStoreVirtualNetworkRule](Set-AzDataLakeStoreVirtualNetworkRule.md)
Módosítja a megadott virtuális hálózati szabályt a megadott adattó-tárolóban.

### [Teszt-AzDataLakeStoreAccount](Test-AzDataLakeStoreAccount.md)
Teszteli az adattó áruházbeli fiók létezését.

### [Teszt-AzDataLakeStoreItem](Test-AzDataLakeStoreItem.md)
Teszteli az adattó-tárolóban lévő fájlok vagy mappák létezését.

