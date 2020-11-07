---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: f7870ec0d8cb75b760faab037f85f36aae88e203
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847061"
---
# <span data-ttu-id="d06f7-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d06f7-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="d06f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d06f7-102">SYNOPSIS</span></span>
<span data-ttu-id="d06f7-103">Új Azure Event Grid-témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d06f7-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="d06f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d06f7-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d06f7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d06f7-105">DESCRIPTION</span></span>
<span data-ttu-id="d06f7-106">Új Azure Event Grid-témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d06f7-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="d06f7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d06f7-107">EXAMPLES</span></span>

### <span data-ttu-id="d06f7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d06f7-108">Example 1</span></span>

<span data-ttu-id="d06f7-109">Létrehoz egy esemény rácsos \` téma1 \` a tartomány \` Domain1 az \` erőforráscsoport MyResourceGroupName csoportban \` \` .</span><span class="sxs-lookup"><span data-stu-id="d06f7-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="d06f7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d06f7-110">PARAMETERS</span></span>

### <span data-ttu-id="d06f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d06f7-111">-DefaultProfile</span></span>
<span data-ttu-id="d06f7-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d06f7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d06f7-113">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="d06f7-113">-DomainName</span></span>
<span data-ttu-id="d06f7-114">EventGrid-tartomány neve.</span><span class="sxs-lookup"><span data-stu-id="d06f7-114">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d06f7-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d06f7-115">-Name</span></span>
<span data-ttu-id="d06f7-116">EventGrid a tartomány témájának nevét.</span><span class="sxs-lookup"><span data-stu-id="d06f7-116">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d06f7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d06f7-117">-ResourceGroupName</span></span>
<span data-ttu-id="d06f7-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d06f7-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="d06f7-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d06f7-119">-Confirm</span></span>
<span data-ttu-id="d06f7-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d06f7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d06f7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d06f7-121">-WhatIf</span></span>
<span data-ttu-id="d06f7-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d06f7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d06f7-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d06f7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d06f7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d06f7-124">CommonParameters</span></span>
<span data-ttu-id="d06f7-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d06f7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d06f7-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d06f7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d06f7-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d06f7-127">INPUTS</span></span>

### <span data-ttu-id="d06f7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d06f7-128">System.String</span></span>

## <span data-ttu-id="d06f7-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d06f7-129">OUTPUTS</span></span>

### <span data-ttu-id="d06f7-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d06f7-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="d06f7-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d06f7-131">NOTES</span></span>

## <span data-ttu-id="d06f7-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d06f7-132">RELATED LINKS</span></span>
