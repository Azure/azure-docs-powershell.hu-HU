---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361114"
---
# <span data-ttu-id="fa3eb-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="fa3eb-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="fa3eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa3eb-102">SYNOPSIS</span></span>
<span data-ttu-id="fa3eb-103">Az eventhub összes fogyasztói csoportját beveszi.</span><span class="sxs-lookup"><span data-stu-id="fa3eb-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="fa3eb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fa3eb-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa3eb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fa3eb-105">DESCRIPTION</span></span>
<span data-ttu-id="fa3eb-106">Az IotHub által használt különböző EventHubs összes eventhub fogyasztói csoportját beveszi.</span><span class="sxs-lookup"><span data-stu-id="fa3eb-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="fa3eb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fa3eb-107">EXAMPLES</span></span>

### <span data-ttu-id="fa3eb-108">1. példa: A telemetriai eventhub összes fogyasztói csoportját beveszi</span><span class="sxs-lookup"><span data-stu-id="fa3eb-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="fa3eb-109">A myiothub nevű iothub telemetriai eseményhubján található összes eventhub fogyasztói csoport lekérte</span><span class="sxs-lookup"><span data-stu-id="fa3eb-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="fa3eb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa3eb-110">PARAMETERS</span></span>

### <span data-ttu-id="fa3eb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa3eb-111">-DefaultProfile</span></span>
<span data-ttu-id="fa3eb-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fa3eb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa3eb-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fa3eb-113">-Name</span></span>
<span data-ttu-id="fa3eb-114">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="fa3eb-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="fa3eb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa3eb-115">-ResourceGroupName</span></span>
<span data-ttu-id="fa3eb-116">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fa3eb-116">Resource Group Name</span></span>

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

### <span data-ttu-id="fa3eb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa3eb-117">CommonParameters</span></span>
<span data-ttu-id="fa3eb-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa3eb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa3eb-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa3eb-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa3eb-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa3eb-120">INPUTS</span></span>

### <span data-ttu-id="fa3eb-121">System.String</span><span class="sxs-lookup"><span data-stu-id="fa3eb-121">System.String</span></span>

## <span data-ttu-id="fa3eb-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa3eb-122">OUTPUTS</span></span>

### <span data-ttu-id="fa3eb-123">Microsoft.Azure.Commands.Management.iotHub.Models.PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="fa3eb-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="fa3eb-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fa3eb-124">NOTES</span></span>

## <span data-ttu-id="fa3eb-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa3eb-125">RELATED LINKS</span></span>
