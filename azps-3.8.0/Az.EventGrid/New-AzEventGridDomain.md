---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 442a88c7fe64fd8913e86ba0ee6be013f226061e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846070"
---
# <span data-ttu-id="83a80-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="83a80-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="83a80-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83a80-102">SYNOPSIS</span></span>
<span data-ttu-id="83a80-103">Új Azure Event Grid-tartományt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="83a80-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="83a80-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83a80-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83a80-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="83a80-105">DESCRIPTION</span></span>
<span data-ttu-id="83a80-106">Új Azure Event Grid-tartományt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="83a80-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="83a80-107">Miután létrejött a tartomány, egy alkalmazás közzéteheti az eseményeket a témakör végpontjának segítségével.</span><span class="sxs-lookup"><span data-stu-id="83a80-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="83a80-108">Példák</span><span class="sxs-lookup"><span data-stu-id="83a80-108">EXAMPLES</span></span>

### <span data-ttu-id="83a80-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="83a80-109">Example 1</span></span>

<span data-ttu-id="83a80-110">A \` \` megadott földrajzi hely \` westus2 \` , az erőforráscsoport- \` MyResourceGroupName \` létrehoz egy esemény rácshoz tartozó Domain1.</span><span class="sxs-lookup"><span data-stu-id="83a80-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="83a80-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="83a80-111">Example 2</span></span>

<span data-ttu-id="83a80-112">A megadott \` \` földrajzi hely \` westus2 \` , az erőforráscsoport \` MyResourceGroupName \` a megadott címkéket tartalmazó "részleg" és "környezet" Domain1 hozza létre az esemény rácsát.</span><span class="sxs-lookup"><span data-stu-id="83a80-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Department, Finance], [Environment, Test]}
```

## <span data-ttu-id="83a80-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83a80-113">PARAMETERS</span></span>

### <span data-ttu-id="83a80-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83a80-114">-DefaultProfile</span></span>
<span data-ttu-id="83a80-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83a80-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83a80-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="83a80-116">-Location</span></span>
<span data-ttu-id="83a80-117">A tartomány helye.</span><span class="sxs-lookup"><span data-stu-id="83a80-117">The location of the domain.</span></span>

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

### <span data-ttu-id="83a80-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="83a80-118">-Name</span></span>
<span data-ttu-id="83a80-119">EventGrid-tartomány neve.</span><span class="sxs-lookup"><span data-stu-id="83a80-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83a80-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83a80-120">-ResourceGroupName</span></span>
<span data-ttu-id="83a80-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="83a80-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="83a80-122">-Címke</span><span class="sxs-lookup"><span data-stu-id="83a80-122">-Tag</span></span>
<span data-ttu-id="83a80-123">Hashtable, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="83a80-123">Hashtable which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83a80-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83a80-124">-Confirm</span></span>
<span data-ttu-id="83a80-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83a80-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83a80-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83a80-126">-WhatIf</span></span>
<span data-ttu-id="83a80-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83a80-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83a80-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83a80-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83a80-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83a80-129">CommonParameters</span></span>
<span data-ttu-id="83a80-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83a80-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83a80-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83a80-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83a80-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83a80-132">INPUTS</span></span>

### <span data-ttu-id="83a80-133">System. String</span><span class="sxs-lookup"><span data-stu-id="83a80-133">System.String</span></span>

### <span data-ttu-id="83a80-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="83a80-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="83a80-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83a80-135">OUTPUTS</span></span>

### <span data-ttu-id="83a80-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="83a80-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="83a80-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83a80-137">NOTES</span></span>

## <span data-ttu-id="83a80-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83a80-138">RELATED LINKS</span></span>
