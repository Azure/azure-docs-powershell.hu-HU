---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 6b98f4266e730e1cfb60ef51046e6846f24999d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672691"
---
# Get-AzureRmServerManagementGateway

## Áttekintés
Egy vagy több kiszolgálói felügyeleti átjárót kap.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### A paraméterek (alapértelmezett)
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Many-ByResourceGroup
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Single-ByName
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Single-ByObject
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmServerManagementGateway** parancsmag egy vagy több Azure Server Management-átjárót kap.

## Példák

### Példa 1: az összes átjáró beolvasása egy előfizetésben
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

Ez a parancs beilleszti az előfizetésben az összes kiszolgálóoldali kezelési átjárót.

### 2. példa: az átjárók beolvasása egy erőforrás csoportban
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

Ez a parancs a Group001 nevű erőforráscsoport csoportjába tartozó összes Kiszolgálókezelő-átjárót beilleszti.

### 3. példa: az átjáró minden telepített példányának lekérése
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

Ez a parancs beolvassa a Gateway01 nevű Kiszolgálókezelő-átjáró minden előfordulását, amely a Group002 nevű erőforráscsoport nevéhez tartozik.

## PARAMÉTEREK

### -Gateway
Azt a átjárót adja meg, amelyre a parancsmag bekerül.

A parancsmag a *ResourceGroupName* és a *GatewayName* paramétert használja a megadott átjárón a művelet végrehajtásához.

Ha ezt a paramétert adja meg, ez a parancsmag az átjáró részletes állapotát fogja tartalmazni.

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -GatewayName
Annak a Kiszolgálókezelő-átjárónak a nevét adja meg, amelynek a parancsmagja a kaput kapja.

Ha a *GatewayName* paramétert adja meg, ez a parancsmag az átjáróban részletezett állapotot fogja tartalmazni.

```yaml
Type: System.String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforrás-csoportnak a nevét adja meg, amelyhez ez a parancsmag átjárókat kap.

```yaml
Type: System.String
Parameter Sets: Many-ByResourceGroup, Single-ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Átjáró
Az "átjáró" paraméter elfogadja az "átjáró" típusú értéket a csővezetéken

## KIMENETEK

### Microsoft. Azure. Command. ServerManagement. Model. Gateway

## MEGJEGYZI
* Ha ez a parancsmag paraméterek nélkül használatos, az előfizetéshez társított összes átjárót fogja visszaadni.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmServerManagementGateway](./New-AzureRmServerManagementGateway.md)

[Remove-AzureRmServerManagementGateway](./Remove-AzureRmServerManagementGateway.md)


