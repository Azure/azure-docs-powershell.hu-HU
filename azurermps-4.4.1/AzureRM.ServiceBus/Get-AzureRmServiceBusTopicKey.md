---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: 24041c299f2f242126f265ad232db3e0c5d526b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503203"
---
# Get-AzureRmServiceBusTopicKey

## Áttekintés
Az elsődleges és másodlagos kapcsolati karakterláncokat kapja a Bus témakörben.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmServiceBusTopicKey** parancsmag az elsődleges és másodlagos kapcsolati karakterláncokat adja eredményül a megadott buszvezető-témakörben.

## Példák

### Példa 1
```
PS C:\> Get-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

Az elsődleges és másodlagos kapcsolati karakterláncokat adja eredményül a megadott Bus-témakörben.

## PARAMÉTEREK

### -ResourceGroup
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: (All)
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

### -Name (név)
A AuthorizationRule témakör neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Névtér neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Topic
A téma neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### -ResourceGroup
 System. String
 

### -NamespaceName
 System. String
 

### -TopicName
 System. String
 

### -AuthorizationRuleName
 System. String

## KIMENETEK

### Microsoft. Azure. Command. ServiceBus. models. ListKeysAttributes
PrimaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-érték}; EntityPath = SB-to pic_exampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-érték}; EntityPath = SB-to pic_exampl1 PrimaryKey: {PrimaryKey Value} SecondaryKey: {SecondaryKey Value} kulcsnév: SBTopicAuthoRule1

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

