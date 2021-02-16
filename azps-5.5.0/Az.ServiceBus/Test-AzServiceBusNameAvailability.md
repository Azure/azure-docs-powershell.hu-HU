---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165899"
---
# <span data-ttu-id="cb0c5-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="cb0c5-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="cb0c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb0c5-102">SYNOPSIS</span></span>
<span data-ttu-id="cb0c5-103">A megadott várólista- vagy témakörnév elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="cb0c5-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="cb0c5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cb0c5-104">SYNTAX</span></span>

### <span data-ttu-id="cb0c5-105">QueueCheckNameAvailabilitySet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb0c5-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb0c5-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="cb0c5-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb0c5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cb0c5-107">DESCRIPTION</span></span>
<span data-ttu-id="cb0c5-108">A **Test-AzServiceBusNameAvailability** parancsmag ellenőrzi, hogy rendelkezésre áll-e a megadott várólistának vagy témakörnek megfelelő név.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="cb0c5-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cb0c5-109">EXAMPLES</span></span>

### <span data-ttu-id="cb0c5-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="cb0c5-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="cb0c5-111">Igaz értéket ad vissza, ha $nameQueue Megadott név Elérhető vagy Hamis, ha $nameQueue megadott név nem érhető el</span><span class="sxs-lookup"><span data-stu-id="cb0c5-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="cb0c5-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="cb0c5-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="cb0c5-113">Igaz értéket ad vissza, ha $nameTopic Megadott név Elérhető vagy Hamis, ha $nameTopic megadott név nem érhető el</span><span class="sxs-lookup"><span data-stu-id="cb0c5-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="cb0c5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb0c5-114">PARAMETERS</span></span>

### <span data-ttu-id="cb0c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb0c5-115">-DefaultProfile</span></span>
<span data-ttu-id="cb0c5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb0c5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cb0c5-117">-Name</span></span>
<span data-ttu-id="cb0c5-118">Queue Name to check the Name Availability</span><span class="sxs-lookup"><span data-stu-id="cb0c5-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="cb0c5-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cb0c5-119">-Namespace</span></span>
<span data-ttu-id="cb0c5-120">Servicebus Namespace Name</span><span class="sxs-lookup"><span data-stu-id="cb0c5-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="cb0c5-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="cb0c5-121">-Queue</span></span>
<span data-ttu-id="cb0c5-122">A várólistán lévő név elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="cb0c5-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="cb0c5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb0c5-123">-ResourceGroupName</span></span>
<span data-ttu-id="cb0c5-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cb0c5-124">Resource Group Name</span></span>

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

### <span data-ttu-id="cb0c5-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="cb0c5-125">-Topic</span></span>
<span data-ttu-id="cb0c5-126">A Témakörnév elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="cb0c5-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="cb0c5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb0c5-127">CommonParameters</span></span>
<span data-ttu-id="cb0c5-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb0c5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cb0c5-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb0c5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb0c5-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb0c5-130">INPUTS</span></span>

### <span data-ttu-id="cb0c5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="cb0c5-131">System.String</span></span>

## <span data-ttu-id="cb0c5-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb0c5-132">OUTPUTS</span></span>

### <span data-ttu-id="cb0c5-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb0c5-133">System.Boolean</span></span>

## <span data-ttu-id="cb0c5-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cb0c5-134">NOTES</span></span>

## <span data-ttu-id="cb0c5-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb0c5-135">RELATED LINKS</span></span>
