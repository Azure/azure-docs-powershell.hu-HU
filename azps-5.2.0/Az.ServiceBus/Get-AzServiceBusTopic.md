---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
ms.openlocfilehash: 3d688362932f61bdea9d685b98f2cba757288da2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371291"
---
# <span data-ttu-id="7061a-101">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="7061a-101">Get-AzServiceBusTopic</span></span>

## <span data-ttu-id="7061a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7061a-102">SYNOPSIS</span></span>
<span data-ttu-id="7061a-103">A megadott Service Bus-témakör leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7061a-103">Returns a description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="7061a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7061a-104">SYNTAX</span></span>

```
Get-AzServiceBusTopic [-ResourceGroupName <String>] [-Namespace <String>] [-Name <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7061a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7061a-105">DESCRIPTION</span></span>
<span data-ttu-id="7061a-106">A **Get-AzServiceBusTopic** parancsmag visszaadja a szolgáltatásbusz megadott névterének leírását.</span><span class="sxs-lookup"><span data-stu-id="7061a-106">The **Get-AzServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7061a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7061a-107">EXAMPLES</span></span>

### <span data-ttu-id="7061a-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7061a-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="7061a-109">Az adott Service Bus névtérhez megadott témakör leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7061a-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="7061a-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="7061a-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="7061a-111">Visszaadja az adott Service Bus névterhez kapcsolódó témakörök listáját.</span><span class="sxs-lookup"><span data-stu-id="7061a-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="7061a-112">Alapértelmezés szerint 100 témakört ad vissza, ha több mint 100 témakört ad vissza, használja a -MaxCount Parameter paramétert.</span><span class="sxs-lookup"><span data-stu-id="7061a-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="7061a-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="7061a-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="7061a-114">Visszaadja az adott Service Bus névtér első 150 témakörének listáját.</span><span class="sxs-lookup"><span data-stu-id="7061a-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="7061a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7061a-115">PARAMETERS</span></span>

### <span data-ttu-id="7061a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7061a-116">-DefaultProfile</span></span>
<span data-ttu-id="7061a-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7061a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7061a-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="7061a-118">-MaxCount</span></span>
<span data-ttu-id="7061a-119">Határozza meg, hogy legfeljebb hány témakört kell visszahozni.</span><span class="sxs-lookup"><span data-stu-id="7061a-119">Determine the maximum number of Topics to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7061a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7061a-120">-Name</span></span>
<span data-ttu-id="7061a-121">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="7061a-121">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7061a-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7061a-122">-Namespace</span></span>
<span data-ttu-id="7061a-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="7061a-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7061a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7061a-124">-ResourceGroupName</span></span>
<span data-ttu-id="7061a-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7061a-125">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7061a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7061a-126">CommonParameters</span></span>
<span data-ttu-id="7061a-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7061a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7061a-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7061a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7061a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7061a-129">INPUTS</span></span>

### <span data-ttu-id="7061a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7061a-130">System.String</span></span>

## <span data-ttu-id="7061a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7061a-131">OUTPUTS</span></span>

### <span data-ttu-id="7061a-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="7061a-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="7061a-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7061a-133">NOTES</span></span>

## <span data-ttu-id="7061a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7061a-134">RELATED LINKS</span></span>
