---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: b40a37729d52cfe3b1dba691fd11724fcd0b03fb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848845"
---
# New-AzureRmKeyVault

## Áttekintés
Egy fő boltozatot hoz létre.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **New-AzureRmKeyVault** parancsmag létrehoz egy fő boltozatot a megadott erőforráscsoport számára. Ez a parancsmag az aktuálisan bejelentkezett felhasználó engedélyeit is feljogosítja a kulcsfájl hozzáadására, eltávolítására, illetve a kulcsok és a titok megadására.

Megjegyzés: Ha a hiba megjelenik, **az előfizetéshez nincs regisztrálva a "Microsoft. kulcskezelő" névtér használata** az új kulcsfájl létrehozásakor, futtassa a **Register-AzureRmResourceProvider-ProviderNamespace "Microsoft. kulcskezelő"** parancsot, majd futtassa újra a **New-AzureRmKeyVault** parancsot. További információt a Register-AzureRmResourceProvider című témakörben talál.

## Példák

### Példa 1: normál kulcsú boltozat létrehozása
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

Ez a parancs létrehoz egy Contoso03Vault nevű kulcs boltozatot az Azure régióban, a Kelet-Amerikai Egyesült Államokban. A parancs hozzáadja a fő boltozatot a Group14 nevű erőforráscsoport csoportjához. Mivel a parancs nem ad meg értéket a *SKU* paraméterhez, létrehoz egy standard kulcs boltozatot.

### 2. példa: prémium kulcsú boltozat létrehozása
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

Ez a parancs az előző példához hasonlóan létrehoz egy fő boltozatot. A prémium kulcsú boltozatot azonban a *SKU* paraméterhez tartozó prémium értékkel adja meg.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForDeployment
A Microsoft. számítási erőforrás-szolgáltatója kinyerheti a titkokat ebből a kulcsfájlból, ha ez a kulcs boltozata az erőforrás létrehozásakor, például virtuális gép létrehozásakor jelenik meg.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForDiskEncryption
Lehetővé teszi, hogy az Azure Disk Encryption szolgáltatás a kulcsok kijavítását és kicsomagolását a kulcsból.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForTemplateDeployment
Lehetővé teszi az Azure Resource Manager számára, hogy ebből a kulcsfájlból kiírja a titkot, ha ezt a kulcspárt a sablonok központi telepítéséhez hivatkozik.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableSoftDelete
Itt adhatja meg, hogy engedélyezve van-e a finom törlés funkció ehhez a kulcshoz. Ha a Soft-delete beállítás engedélyezve van, a türelmi időszakra visszaállíthatja a fő boltozatot és annak tartalmát a törlés után.

A funkcióról további információt az [Azure Key Vault Soft-delete – áttekintés](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)című témakörben talál. Útmutatásért olvassa el a következő témakört: [Hogyan lehet használni a kulcsfájl Soft-deletet a PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell)segítségével.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hely
Azt az Azure-területet adja meg, amelyben a fő pince hozható létre. Használja a [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) parancsot a lehetőségek megjelenítéséhez.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak a meglévő erőforrás-csoportnak a nevét adja meg, amelybe a kulcs boltozatát létre szeretné hozni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
A fő boltozat-példány SKU-ának meghatározása. Ha tudni kívánja, hogy mely funkciók érhetők el az egyes SKU-hoz, olvassa el az Azure Key Vault árképzési webhelye című témakört https://go.microsoft.com/fwlink/?linkid=512521) .

```yaml
Type: SkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címke
A kulcs-érték párok a hash-táblázatok formájában. Példa:

@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
A létrehozandó fő pince nevét adja meg. A név lehet betűk, számjegyek és kötőjelek tetszőleges kombinációja. A névnek betűvel vagy számmal kell kezdődnie. A névnek univerzálisan egyedinek kell lennie.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. Azure. Command. PSVault. models.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmKeyVault](./Get-AzureRmKeyVault.md)

[Remove-AzureRmKeyVault](./Remove-AzureRmKeyVault.md)
