---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: 0cac398a77c6d26ed9454b7345ce1bb8fde5b965
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845265"
---
# Get-AzIotCentralApp

## Áttekintés
Egy vagy több IoT-alapú központi alkalmazás tulajdonságait kapja.

## SZINTAXISA

### ListIotCentralAppsParameterSet (alapértelmezett)
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InteractiveIotCentralParameterSet
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Egy adott IoT központi alkalmazás metaadatait vagy egy erőforráscsoport vagy-előfizetés összes alkalmazását kapja meg, a beállított paramétertől függően. 

## Példák

### 1. példa: adott IoT központi alkalmazás beolvasása
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

A megadott IoT központi alkalmazás metaadatait kapja meg.

Példa kimenet:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN DisplayName: az egyéni megjelenítendő név altartománya: SubscriptionId sablon: XXXXXXXXXXXX iotc-default@1.0.0 : XXXXXXXX-XXXX-ResourceGroupName MyResourceGroupName:

### 2. példa: a IoT központi alkalmazásainak beszerzése az előfizetésben.
```powershell
PS C:\> Get-AzIotCentralApp
```

A jelenlegi előfizetésben az összes IoT központi alkalmazás metaadatait kapja.

Példa kimenet:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN DisplayName: az egyéni megjelenítendő név altartománya: SubscriptionId sablon: XXXXXXXXXXXX iotc-default@1.0.0 : XXXXXXXX-XXXX-ResourceGroupName MyResourceGroupName:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 név: MyAppResourceName2 típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN2 DisplayName: az egyéni megjelenítendő név 2 aldomain: SubscriptionId sablon: XXXXXXXXXXXX: XXXXXXXX-XXXX- iotc-default@1.0.0 ResourceGroupName MyResourceGroupName2:

### 3 Példa: a IoT központi alkalmazásai beolvasása az erőforráscsoport-ban
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

A megadott erőforráscsoport összes IoT-alkalmazásának metaadatait kapja.

Példa kimenet:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN DisplayName: az egyéni megjelenítendő név altartománya: SubscriptionId sablon: XXXXXXXXXXXX iotc-default@1.0.0 : XXXXXXXX-XXXX-ResourceGroupName MyResourceGroupName:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 név: MyAppResourceName2 típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN2 DisplayName: az egyéni megjelenítendő név 2 aldomain: SubscriptionId sablon: XXXXXXXXXXXX: XXXXXXXX-XXXX- iotc-default@1.0.0 ResourceGroupName MyResourceGroupName:

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Name (név)
Az IOT központi alkalmazás-erőforrás neve.

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
IOT központi alkalmazás-erőforrás azonosítója

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. IotCentral. models. PSIotCentralApp

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
