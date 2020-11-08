---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025711"
---
# <span data-ttu-id="0a0e5-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0a0e5-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="0a0e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a0e5-102">SYNOPSIS</span></span>
<span data-ttu-id="0a0e5-103">Megkapja az összes eventhub-consumergroups.</span><span class="sxs-lookup"><span data-stu-id="0a0e5-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="0a0e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a0e5-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a0e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a0e5-105">DESCRIPTION</span></span>
<span data-ttu-id="0a0e5-106">Megkapja az IotHub által használt különböző EventHubs tartozó összes eventhub consumergroups.</span><span class="sxs-lookup"><span data-stu-id="0a0e5-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="0a0e5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0a0e5-107">EXAMPLES</span></span>

### <span data-ttu-id="0a0e5-108">Az 1 példa beolvassa a telemetriai eventhub összes eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="0a0e5-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="0a0e5-109">Beolvassa a telemetriai eventhub összes eventhub consumergroups a iothub nevű myiothub</span><span class="sxs-lookup"><span data-stu-id="0a0e5-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="0a0e5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a0e5-110">PARAMETERS</span></span>

### <span data-ttu-id="0a0e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a0e5-111">-DefaultProfile</span></span>
<span data-ttu-id="0a0e5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0a0e5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a0e5-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0a0e5-113">-Name</span></span>
<span data-ttu-id="0a0e5-114">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="0a0e5-114">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a0e5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a0e5-115">-ResourceGroupName</span></span>
<span data-ttu-id="0a0e5-116">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="0a0e5-116">Resource Group Name</span></span>

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

### <span data-ttu-id="0a0e5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a0e5-117">CommonParameters</span></span>
<span data-ttu-id="0a0e5-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a0e5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a0e5-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a0e5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a0e5-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a0e5-120">INPUTS</span></span>

### <span data-ttu-id="0a0e5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0a0e5-121">System.String</span></span>

## <span data-ttu-id="0a0e5-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a0e5-122">OUTPUTS</span></span>

### <span data-ttu-id="0a0e5-123">Microsoft. Azure. Command. Management. IotHub. models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="0a0e5-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="0a0e5-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a0e5-124">NOTES</span></span>

## <span data-ttu-id="0a0e5-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a0e5-125">RELATED LINKS</span></span>
