---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369037"
---
# <span data-ttu-id="e477f-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="e477f-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="e477f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e477f-102">SYNOPSIS</span></span>
<span data-ttu-id="e477f-103">A megadott várólista- vagy témakörnév elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="e477f-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="e477f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e477f-104">SYNTAX</span></span>

### <span data-ttu-id="e477f-105">QueueCheckNameAvailabilitySet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e477f-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e477f-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e477f-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e477f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e477f-107">DESCRIPTION</span></span>
<span data-ttu-id="e477f-108">A **Test-AzServiceBusNameAvailability** parancsmag ellenőrzi, hogy rendelkezésre áll-e a megadott várólistának vagy témakörnek megfelelő név.</span><span class="sxs-lookup"><span data-stu-id="e477f-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="e477f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e477f-109">EXAMPLES</span></span>

### <span data-ttu-id="e477f-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="e477f-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="e477f-111">Igaz értéket ad vissza, ha a Megadott $nameQueue Értéke Elérhető vagy Hamis, ha $nameQueue megadott név nem érhető el</span><span class="sxs-lookup"><span data-stu-id="e477f-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="e477f-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="e477f-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="e477f-113">Igaz értéket ad vissza, ha $nameTopic Megadott név Elérhető vagy Hamis, ha $nameTopic megadott név nem érhető el</span><span class="sxs-lookup"><span data-stu-id="e477f-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="e477f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e477f-114">PARAMETERS</span></span>

### <span data-ttu-id="e477f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e477f-115">-DefaultProfile</span></span>
<span data-ttu-id="e477f-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e477f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e477f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e477f-117">-Name</span></span>
<span data-ttu-id="e477f-118">Queue Name to check the Name Availability</span><span class="sxs-lookup"><span data-stu-id="e477f-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="e477f-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e477f-119">-Namespace</span></span>
<span data-ttu-id="e477f-120">Servicebus Namespace Name</span><span class="sxs-lookup"><span data-stu-id="e477f-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="e477f-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="e477f-121">-Queue</span></span>
<span data-ttu-id="e477f-122">A várólistán lévő név elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="e477f-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="e477f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e477f-123">-ResourceGroupName</span></span>
<span data-ttu-id="e477f-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e477f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e477f-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="e477f-125">-Topic</span></span>
<span data-ttu-id="e477f-126">A Témakörnév elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="e477f-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="e477f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e477f-127">CommonParameters</span></span>
<span data-ttu-id="e477f-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e477f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e477f-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e477f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e477f-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e477f-130">INPUTS</span></span>

### <span data-ttu-id="e477f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e477f-131">System.String</span></span>

## <span data-ttu-id="e477f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e477f-132">OUTPUTS</span></span>

### <span data-ttu-id="e477f-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e477f-133">System.Boolean</span></span>

## <span data-ttu-id="e477f-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e477f-134">NOTES</span></span>

## <span data-ttu-id="e477f-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e477f-135">RELATED LINKS</span></span>
