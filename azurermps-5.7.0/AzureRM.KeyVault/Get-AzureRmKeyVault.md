---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 7b26eeb94854d21791bb662b4c1d9ce19973a193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505507"
---
# Get-AzureRmKeyVault

## Áttekintés
Kulcsos boltozatokat kap.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ListAllVaultsInSubscription (alapértelmezett)
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetVaultByName
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedVault
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAllDeletedVaultsInSubscription
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmKeyVault** parancsmag információkat kap az előfizetések fő boltozatáról. Az előfizetésben megtekintheti az összes fontos boltozat-példányt, vagy szűrheti az eredményeket egy erőforráscsoport vagy egy adott kulcs boltozatával.

Fontos tudni, hogy bár az erőforráscsoport beállítása nem kötelező a parancsmag számára, ha egyetlen kulcs típusú boltozatot kap, akkor a jobb teljesítmény érdekében ezt el kell végeznie.

## Példák

### Példa 1: a jelenlegi előfizetésben lévő összes kulcs boltozatának beszerzése
```
PS C:\>Get-AzureRMKeyVault
```

Ez a parancs a jelenlegi előfizetésben a legfontosabb boltozatokat kapja.

### 2. példa: adott kulcsos boltozat beszerzése
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

Ez a parancs a Contoso03Vault nevű kulcs boltozatát kapja a jelenlegi előfizetésben, majd a $MyVault változóban tárolja. A $MyVault tulajdonságait ellenőrizheti, hogy miként kaphat részleteket a fő boltozatról.

### 3. példa: kulcsos boltívek beszerzése erőforráscsoporthoz
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

Ez a parancs a ContosoPayRollResourceGroup nevű erőforráscsoport minden fő boltozatát beolvassa.

### 4. példa: az összes törölt kulcsfájl beolvasása a jelenlegi előfizetésben
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

Ez a parancs beolvassa a jelenlegi előfizetés összes törölt kulcsát.

### Példa 5: törölt kulcsfájl beszerzése
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

Ez a parancs beolvassa a Contoso03Vault nevű, az aktuális előfizetésben és a eastus2-régióban a törölt kulcs boltozattal kapcsolatos információkat.

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

### -InRemovedState
Itt adhatja meg, hogy megjelenjen-e a korábban törölt boltozatok a kimenetben.

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hely
A törölt boltozat helye.

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A lekérdezett fő boltozattal vagy a fő boltozatokkal társított erőforráscsoport nevét adja meg.

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címke
A kulcs-érték párok a hash-táblázatok formájában. Példa:

@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}

```yaml
Type: Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
A fő pince nevét adja meg.

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. Command. PSKeyVault. models.

### System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. devault. models. PSKeyVaultIdentityItem]

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault

### System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmKeyVault](./New-AzureRmKeyVault.md)

[Remove-AzureRmKeyVault](./Remove-AzureRmKeyVault.md)
