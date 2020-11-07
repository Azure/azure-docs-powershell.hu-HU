---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/get-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
ms.openlocfilehash: fdf674b5ec2dfcefe8fcada92cfaf0fd1073f7f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680665"
---
# Get-AzureRmIotCentralApp

## Áttekintés
Egy vagy több IoT-alapú központi alkalmazás tulajdonságait kapja.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ListIotCentralAppsParameterSet (alapértelmezett)
```
Get-AzureRmIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InteractiveIotCentralParameterSet
```
Get-AzureRmIotCentralApp [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzureRmIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Egy adott IoT központi alkalmazás metaadatait vagy egy erőforráscsoport vagy-előfizetés összes alkalmazását kapja meg, a beállított paramétertől függően. 

## Példák

### 1. példa: adott IoT központi alkalmazás beolvasása
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

A megadott IoT központi alkalmazás metaadatait kapja meg.

Példa kimenet:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN DisplayName: az egyéni megjelenítendő név altartománya: SubscriptionId sablon: XXXXXXXXXXXX iotc-default@1.0.0 : XXXXXXXX-XXXX-ResourceGroupName MyResourceGroupName:

### 2. példa: a IoT központi alkalmazásainak beszerzése az előfizetésben.
```powershell
PS C:\> Get-AzureRmIotCentralApp
```

A jelenlegi előfizetésben az összes IoT központi alkalmazás metaadatait kapja.

Példa kimenet:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN DisplayName: az egyéni megjelenítendő név altartománya: SubscriptionId sablon: XXXXXXXXXXXX iotc-default@1.0.0 : XXXXXXXX-XXXX-ResourceGroupName MyResourceGroupName:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 név: MyAppResourceName2 típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN2 DisplayName: az egyéni megjelenítendő név 2 aldomain: SubscriptionId sablon: XXXXXXXXXXXX: XXXXXXXX-XXXX- iotc-default@1.0.0 ResourceGroupName MyResourceGroupName2:

### 3 Példa: a IoT központi alkalmazásai beolvasása az erőforráscsoport-ban
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

A megadott erőforráscsoport összes IoT-alkalmazásának metaadatait kapja.

Példa kimenet:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName név: MyAppResourceName típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN DisplayName: az egyéni megjelenítendő név altartománya: SubscriptionId sablon: XXXXXXXXXXXX iotc-default@1.0.0 : XXXXXXXX-XXXX-ResourceGroupName MyResourceGroupName:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 név: MyAppResourceName2 típus: Microsoft. IoTCentral/IoTApps hely: westus címke: {[kulcs, val]} SKU: Microsoft. Azure. Command. IotCentral. models. PSIotCentralAppSkuInfo. ApplicationId. XXXXXXXXXXXX: XXXXXXXX-XXXX-XXXX-XXXX-MYAPPSUBDOMAIN2 DisplayName: az egyéni megjelenítendő név 2 aldomain: SubscriptionId sablon: XXXXXXXXXXXX: XXXXXXXX-XXXX- iotc-default@1.0.0 ResourceGroupName MyResourceGroupName:

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Name (név)
Az IOT központi alkalmazás-erőforrás neve.

```yaml
Type: String
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
Type: String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
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
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String
## KIMENETEK

### Microsoft. Azure. Command. IotCentral. models. PSIotCentralApp
## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
