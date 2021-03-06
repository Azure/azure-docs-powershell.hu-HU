---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: a6aa52408cf1befd1c1208258c184be327ff2a15
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928554"
---
# Get-AzRecoveryServicesVault

## SYNOPSIS

Lekérte a Helyreállítási szolgáltatások tárolóinak listáját.

## SZINTAXIS

### ByTagNameValueParameterSet
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByTagObjectParameterSet
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS

A **Get-AzRecoveryServicesVault** parancsmag lekérte a helyreállítási szolgáltatások tárolóinak listáját az aktuális előfizetésben.

## PÉLDÁK

### 1. példa

```
PS C:\> Get-AzRecoveryServicesVault
```

A kijelölt előfizetésben található tárolólista lekérte.

### 2. példa

```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

A kijelölt előfizetés erőforráscsoportban található tároló listájának lekérte.

### 3. példa

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $vault.Identity | fl

PrincipalId : XXXXXXXX-XXXX-XXXX
TenantId    : XXXXXXXX-XXXX-XXXX
Type        : SystemAssigned
```

Az első parancsmag a tárolót az erőforráscsoportban kapja meg a megadott néven. Ezután hozzáférhetünk az MSI-adatokhoz a tárolóból.

## PARAMETERS

### -DefaultProfile

Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Megadja annak a tárolónak a nevét, amelyről le kellkérdezni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName

Annak az Azure-erőforráscsoportnak a nevét adja meg, amelyből lekéri a megadott Recovery Services-objektumot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag

Megadja a lekérdezéshez használható címkéket.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TagName

A lekérdezéshez használható címke kulcsát adja meg.

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TagValue

Annak a címkének az értékét adja meg, amelynél a lekérdezést el kell

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.RecoveryServices.ARSVault

## MEGJEGYZÉSEK
Get-AzRecoveryServicesVault.RecoveryServices(<=2.10.0) nem működik az Az.Accounts(>=1.8.1) verzióban helytelen összeállítási hivatkozás miatt. Az Az.RecoveryServices modult frissíteni kell 2.11.0-s vagy újabb verzióra, ha a legújabb Az vagy Az.Accounts verziót használja.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzRecoveryServicesVaultSettingsFile](./Get-AzRecoveryServicesVaultSettingsFile.md)

[New-AzRecoveryServicesVault](./New-AzRecoveryServicesVault.md)

[Remove-AzRecoveryServicesVault](./Remove-AzRecoveryServicesVault.md)
