---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: 92a70d16f8cd1db2c37c1247c994a3c406df5a54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938769"
---
# <span data-ttu-id="53931-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="53931-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="53931-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53931-102">SYNOPSIS</span></span>
<span data-ttu-id="53931-103">Az események eseményrács-témakörben való közzétételéhez használt megosztott hozzáférési kulcsokat használja.</span><span class="sxs-lookup"><span data-stu-id="53931-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="53931-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53931-104">SYNTAX</span></span>

### <span data-ttu-id="53931-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53931-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53931-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53931-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53931-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="53931-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53931-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53931-108">DESCRIPTION</span></span>
<span data-ttu-id="53931-109">Az események eseményrács-témakörben való közzétételéhez használt megosztott hozzáférési kulcsokat használja.</span><span class="sxs-lookup"><span data-stu-id="53931-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="53931-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53931-110">EXAMPLES</span></span>

### <span data-ttu-id="53931-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="53931-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="53931-112">A \` MyResourceGroupName erőforráscsoport Eseményrács témakörÉnek \` \` 1. témakörének megosztott hozzáférési kulcsait kapja \` meg.</span><span class="sxs-lookup"><span data-stu-id="53931-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="53931-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="53931-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="53931-114">A \` MyResourceGroupName erőforráscsoport Eseményrács témakörÉnek \` \` 1. témakörének megosztott hozzáférési kulcsait kapja \` meg.</span><span class="sxs-lookup"><span data-stu-id="53931-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="53931-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53931-115">PARAMETERS</span></span>

### <span data-ttu-id="53931-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53931-116">-DefaultProfile</span></span>
<span data-ttu-id="53931-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="53931-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53931-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53931-118">-InputObject</span></span>
<span data-ttu-id="53931-119">EventGrid Topic objektum.</span><span class="sxs-lookup"><span data-stu-id="53931-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53931-120">-Name</span><span class="sxs-lookup"><span data-stu-id="53931-120">-Name</span></span>
<span data-ttu-id="53931-121">EventGrid-témakör neve.</span><span class="sxs-lookup"><span data-stu-id="53931-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53931-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53931-122">-ResourceGroupName</span></span>
<span data-ttu-id="53931-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="53931-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53931-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53931-124">-ResourceId</span></span>
<span data-ttu-id="53931-125">Az Eseményrács témakört képviselő erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="53931-125">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53931-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53931-126">CommonParameters</span></span>
<span data-ttu-id="53931-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53931-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53931-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53931-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53931-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53931-129">INPUTS</span></span>

### <span data-ttu-id="53931-130">System.String</span><span class="sxs-lookup"><span data-stu-id="53931-130">System.String</span></span>

### <span data-ttu-id="53931-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="53931-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="53931-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53931-132">OUTPUTS</span></span>

### <span data-ttu-id="53931-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="53931-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="53931-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53931-134">NOTES</span></span>

## <span data-ttu-id="53931-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53931-135">RELATED LINKS</span></span>
