---
Module Name: AzureRM.DataLakeStore
Module Guid: 90dfd814-abce-4e1f-99b6-fe16760c079a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/AzureRM.DataLakeStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/AzureRM.DataLakeStore.md
ms.openlocfilehash: 26a97d9f41ed7d0acb4e80a3302b22c8b2fab1c1
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/14/2020
ms.locfileid: "93491814"
---
# AzureRM. DataLakeStore modul
## Leírás
Az ebben a szakaszban szereplő témakörök az Azure-alapú Lake Store Azure PowerShell-parancsmagjai az Azure Resource Manager (ARM) keretrendszerben című témakörben olvashatók. A parancsmagok a Microsoft. Azure. commands. DataLakeStore névtérben találhatók. Ezek a parancsmagok csak az Azure Data Lake Storage Gen1-fiókjaival működnek.

## AzureRM. DataLakeStore parancsmagok
### [Add-AzureRmDataLakeStoreFirewallRule](Add-AzureRmDataLakeStoreFirewallRule.md)
Tűzfal-szabály felvétele a megadott Data Lake Store-fiókba.

### [Add-AzureRmDataLakeStoreItemContent](Add-AzureRmDataLakeStoreItemContent.md)
Tartalmat ad az adattó-tároló elemeihez.

### [Add-AzureRmDataLakeStoreTrustedIdProvider](Add-AzureRmDataLakeStoreTrustedIdProvider.md)
A megadott Data Lake Store-fiókhoz hozzáadja a megbízható identitás-szolgáltatót.

### [Add-AzureRmDataLakeStoreVirtualNetworkRule](Add-AzureRmDataLakeStoreVirtualNetworkRule.md)
Virtuális hálózati szabály felvétele a megadott Data Lake Store-fiókba.

### [Enable-AzureRmDataLakeStoreKeyVault](Enable-AzureRmDataLakeStoreKeyVault.md)
Megkísérli engedélyezni a felhasználó által felügyelt kulcs boltozatát a megadott Data Lake Store-fiók titkosításához.

### [Exportálás – AzureRmDataLakeStoreChildItemProperties](Export-AzureRmDataLakeStoreChildItemProperties.md)
A tulajdonságok (lemezhasználat és ACL) exportálása a teljes fához a megadott elérési úttal egy kimeneti elérési útra

### [Exportálás – AzureRmDataLakeStoreItem](Export-AzureRmDataLakeStoreItem.md)
Az adattó áruházból letölt egy fájlt.

### [Get-AzureRmDataLakeStoreAccount](Get-AzureRmDataLakeStoreAccount.md)
Adatokat kap az adattó áruházbeli fiókról.

### [Get-AzureRmDataLakeStoreChildItem](Get-AzureRmDataLakeStoreChildItem.md)
Az elemek listájának beolvasása az adattó áruházban lévő mappákban.

### [Get-AzureRmDataLakeStoreChildItemSummary](Get-AzureRmDataLakeStoreChildItemSummary.md)
A megadott elérési úton lévő teljes méret, fájlok és könyvtárak összegzése

### [Get-AzureRmDataLakeStoreFirewallRule](Get-AzureRmDataLakeStoreFirewallRule.md)
A megadott tűzfalszabályok beolvasása a megadott adattó-tárolóban.
Ha nem adja meg a tűzfal szabályát, akkor a rendszer megjeleníti a fiókhoz tartozó összes tűzfal-szabályt.

### [Get-AzureRmDataLakeStoreItem](Get-AzureRmDataLakeStoreItem.md)
Az adattó áruházban lévő fájlok vagy mappák részleteit kapja meg.

### [Get-AzureRmDataLakeStoreItemAclEntry](Get-AzureRmDataLakeStoreItemAclEntry.md)
Beilleszt egy bejegyzést az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájába.

### [Get-AzureRmDataLakeStoreItemContent](Get-AzureRmDataLakeStoreItemContent.md)
A fájl tartalmának beolvasása az adattó áruházban.

### [Get-AzureRmDataLakeStoreItemOwner](Get-AzureRmDataLakeStoreItemOwner.md)
Az adattó áruházban lévő fájl vagy mappa tulajdonosát kapja meg.

### [Get-AzureRmDataLakeStoreItemPermission](Get-AzureRmDataLakeStoreItemPermission.md)
Az adattó-tárolóban lévő fájl vagy mappa engedélyét adja meg.

### [Get-AzureRmDataLakeStoreTrustedIdProvider](Get-AzureRmDataLakeStoreTrustedIdProvider.md)
A megadott adattárolóban kapja meg a megadott megbízható identitás-szolgáltatót.
Ha nem ad meg szolgáltatót, akkor a fiók összes szolgáltatóját listázhatja.

### [Get-AzureRmDataLakeStoreVirtualNetworkRule](Get-AzureRmDataLakeStoreVirtualNetworkRule.md)
A megadott virtuális hálózati szabályok beolvasása a megadott Data Lake Store áruházban.
Ha nincs megadva virtuális hálózati szabály, akkor a rendszer megjeleníti a fiókhoz tartozó összes virtuális hálózati szabályt.

### [Importálás – AzureRmDataLakeStoreItem](Import-AzureRmDataLakeStoreItem.md)
Helyi fájlt vagy könyvtárat tölt fel egy adattó-áruházba.

### [Bekapcsolódás a AzureRmDataLakeStoreItem](Join-AzureRmDataLakeStoreItem.md)
Csatlakozik egy vagy több fájlhoz egy fájl létrehozásához az adattó áruházban.

### [Move-AzureRmDataLakeStoreItem](Move-AzureRmDataLakeStoreItem.md)
Egy fájl vagy mappa áthelyezése vagy átnevezése az adattó áruházban.

### [Új – AzureRmDataLakeStoreAccount](New-AzureRmDataLakeStoreAccount.md)
Új Data Lake Store-fiók létrehozása

### [Új – AzureRmDataLakeStoreItem](New-AzureRmDataLakeStoreItem.md)
Új fájlt vagy mappát hoz létre az adattó áruházban.

### [Remove-AzureRmDataLakeStoreAccount](Remove-AzureRmDataLakeStoreAccount.md)
Véglegesen törli az adattó-tároló fiókját.

### [Remove-AzureRmDataLakeStoreFirewallRule](Remove-AzureRmDataLakeStoreFirewallRule.md)
A megadott tűzfalszabályok eltávolítása a megadott Data Lake Store-ban.

### [Remove-AzureRmDataLakeStoreItem](Remove-AzureRmDataLakeStoreItem.md)
Töröl egy fájlt vagy mappát az adattó áruházból.

### [Remove-AzureRmDataLakeStoreItemAcl](Remove-AzureRmDataLakeStoreItemAcl.md)
Törli az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listáját.

### [Remove-AzureRmDataLakeStoreItemAclEntry](Remove-AzureRmDataLakeStoreItemAclEntry.md)
Az adattó-tárolóban lévő fájl vagy mappa HOZZÁFÉRÉSének a bejegyzését távolítja el.

### [Remove-AzureRmDataLakeStoreTrustedIdProvider](Remove-AzureRmDataLakeStoreTrustedIdProvider.md)
A megadott megbízható identitás-szolgáltató eltávolítása a megadott Data Lake Store áruházból.

### [Remove-AzureRmDataLakeStoreVirtualNetworkRule](Remove-AzureRmDataLakeStoreVirtualNetworkRule.md)
A megadott virtuális hálózati szabály eltávolítása a megadott Data Lake Store-ból.

### [Set-AzureRmDataLakeStoreAccount](Set-AzureRmDataLakeStoreAccount.md)
Az adattó-tároló fiók módosítása.

### [Set-AzureRmDataLakeStoreFirewallRule](Set-AzureRmDataLakeStoreFirewallRule.md)
A megadott tűzfalszabályok módosítása a megadott adattó-tárolóban.

### [Set-AzureRmDataLakeStoreItemAcl](Set-AzureRmDataLakeStoreItemAcl.md)
Módosítja az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listáját.

### [Set-AzureRmDataLakeStoreItemAclEntry](Set-AzureRmDataLakeStoreItemAclEntry.md)
Módosította az adattó-tárolóban lévő fájl vagy mappa HOZZÁFÉRÉSének bejegyzését.

### [Set-AzureRmDataLakeStoreItemExpiry](Set-AzureRmDataLakeStoreItemExpiry.md)
Egy Azure Data Lake Store-fiókban lévő fájl elévülési idejének beállítása vagy eltávolítása.

### [Set-AzureRmDataLakeStoreItemOwner](Set-AzureRmDataLakeStoreItemOwner.md)
Módosítja egy fájl vagy mappa tulajdonosát az adattó-áruházban.

### [Set-AzureRmDataLakeStoreItemPermission](Set-AzureRmDataLakeStoreItemPermission.md)
Módosította az adattó-tárolóban lévő fájlok vagy mappák engedélyének oktális részét.

### [Set-AzureRmDataLakeStoreTrustedIdProvider](Set-AzureRmDataLakeStoreTrustedIdProvider.md)
Módosította a megadott megbízható identitás-szolgáltatót a megadott Data Lake Store-ban.

### [Set-AzureRmDataLakeStoreVirtualNetworkRule](Set-AzureRmDataLakeStoreVirtualNetworkRule.md)
Módosítja a megadott virtuális hálózati szabályt a megadott adattó-tárolóban.

### [Teszt-AzureRmDataLakeStoreAccount](Test-AzureRmDataLakeStoreAccount.md)
Teszteli az adattó áruházbeli fiók létezését.

### [Teszt-AzureRmDataLakeStoreItem](Test-AzureRmDataLakeStoreItem.md)
Teszteli az adattó-tárolóban lévő fájlok vagy mappák létezését.

