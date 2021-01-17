---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 2923f05bc954c0570c49886c3a036ef78848a1e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329514"
---
# <span data-ttu-id="badb6-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="badb6-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="badb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="badb6-102">SYNOPSIS</span></span>
<span data-ttu-id="badb6-103">Létrehoz egy új Azure Event Grid tartománytémát.</span><span class="sxs-lookup"><span data-stu-id="badb6-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="badb6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="badb6-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="badb6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="badb6-105">DESCRIPTION</span></span>
<span data-ttu-id="badb6-106">Létrehoz egy új Azure Event Grid tartománytémát.</span><span class="sxs-lookup"><span data-stu-id="badb6-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="badb6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="badb6-107">EXAMPLES</span></span>

### <span data-ttu-id="badb6-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="badb6-108">Example 1</span></span>

<span data-ttu-id="badb6-109">Létrehoz egy Event Grid Domain Topic Topic1 nevű témakört a Domain Domain1 tartományban \` \` a \` \` \` MyResourceGroupName \` erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="badb6-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="badb6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="badb6-110">PARAMETERS</span></span>

### <span data-ttu-id="badb6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="badb6-111">-DefaultProfile</span></span>
<span data-ttu-id="badb6-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="badb6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="badb6-113">-DomainName</span><span class="sxs-lookup"><span data-stu-id="badb6-113">-DomainName</span></span>
<span data-ttu-id="badb6-114">EventGrid tartománynév.</span><span class="sxs-lookup"><span data-stu-id="badb6-114">EventGrid domain name.</span></span>

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

### <span data-ttu-id="badb6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="badb6-115">-Name</span></span>
<span data-ttu-id="badb6-116">EventGrid tartomány témakörének neve.</span><span class="sxs-lookup"><span data-stu-id="badb6-116">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="badb6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="badb6-117">-ResourceGroupName</span></span>
<span data-ttu-id="badb6-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="badb6-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="badb6-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="badb6-119">-Confirm</span></span>
<span data-ttu-id="badb6-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="badb6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="badb6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="badb6-121">-WhatIf</span></span>
<span data-ttu-id="badb6-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="badb6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="badb6-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="badb6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="badb6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="badb6-124">CommonParameters</span></span>
<span data-ttu-id="badb6-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="badb6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="badb6-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="badb6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="badb6-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="badb6-127">INPUTS</span></span>

### <span data-ttu-id="badb6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="badb6-128">System.String</span></span>

## <span data-ttu-id="badb6-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="badb6-129">OUTPUTS</span></span>

### <span data-ttu-id="badb6-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="badb6-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="badb6-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="badb6-131">NOTES</span></span>

## <span data-ttu-id="badb6-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="badb6-132">RELATED LINKS</span></span>
