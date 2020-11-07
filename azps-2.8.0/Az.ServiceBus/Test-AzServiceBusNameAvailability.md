---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: 396a328de8c075b49ae4dda181158c33518eaa8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838018"
---
# <span data-ttu-id="86d47-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="86d47-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="86d47-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86d47-102">SYNOPSIS</span></span>
<span data-ttu-id="86d47-103">Az adott várólista vagy a téma nevének elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="86d47-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="86d47-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86d47-104">SYNTAX</span></span>

### <span data-ttu-id="86d47-105">QueueCheckNameAvailabilitySet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86d47-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86d47-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="86d47-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86d47-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="86d47-107">DESCRIPTION</span></span>
<span data-ttu-id="86d47-108">A **teszt-AzServiceBusNameAvailability** parancsmag a várólista vagy a témakör megadott nevének elérhetőségét ellenőrzi</span><span class="sxs-lookup"><span data-stu-id="86d47-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="86d47-109">Példák</span><span class="sxs-lookup"><span data-stu-id="86d47-109">EXAMPLES</span></span>

### <span data-ttu-id="86d47-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="86d47-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="86d47-111">Igaz érték visszaadása, ha a megadott $nameQueue neve Availabile, vagy hamis értéket ad eredményül, ha a megadott $nameQueue név nem érhető el</span><span class="sxs-lookup"><span data-stu-id="86d47-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="86d47-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="86d47-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="86d47-113">Igaz érték visszaadása, ha a megadott $nameTopic neve Availabile, vagy hamis értéket ad eredményül, ha a megadott $nameTopic név nem érhető el</span><span class="sxs-lookup"><span data-stu-id="86d47-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="86d47-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86d47-114">PARAMETERS</span></span>

### <span data-ttu-id="86d47-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d47-115">-DefaultProfile</span></span>
<span data-ttu-id="86d47-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86d47-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86d47-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="86d47-117">-Name</span></span>
<span data-ttu-id="86d47-118">Várólista neve a név elérhetőségének ellenőrzéséhez</span><span class="sxs-lookup"><span data-stu-id="86d47-118">Queue Name to check the Name Availability</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86d47-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="86d47-119">-Namespace</span></span>
<span data-ttu-id="86d47-120">Servicebus-névtér neve</span><span class="sxs-lookup"><span data-stu-id="86d47-120">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86d47-121">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="86d47-121">-Queue</span></span>
<span data-ttu-id="86d47-122">A várólista nevének elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="86d47-122">To Check Name Availability for Queue Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: QueueCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d47-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86d47-123">-ResourceGroupName</span></span>
<span data-ttu-id="86d47-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="86d47-124">Resource Group Name</span></span>

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

### <span data-ttu-id="86d47-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="86d47-125">-Topic</span></span>
<span data-ttu-id="86d47-126">A téma nevének elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="86d47-126">To Check Name Availability for Topic Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TopicCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d47-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d47-127">CommonParameters</span></span>
<span data-ttu-id="86d47-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86d47-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="86d47-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86d47-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d47-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86d47-130">INPUTS</span></span>

### <span data-ttu-id="86d47-131">System. String</span><span class="sxs-lookup"><span data-stu-id="86d47-131">System.String</span></span>

## <span data-ttu-id="86d47-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86d47-132">OUTPUTS</span></span>

### <span data-ttu-id="86d47-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86d47-133">System.Boolean</span></span>

## <span data-ttu-id="86d47-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86d47-134">NOTES</span></span>

## <span data-ttu-id="86d47-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86d47-135">RELATED LINKS</span></span>
