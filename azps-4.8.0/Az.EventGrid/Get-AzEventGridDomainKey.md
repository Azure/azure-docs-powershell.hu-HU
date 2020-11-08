---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: c080a5132d5ed31828fbf7a35385432d3c91a923
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184544"
---
# <span data-ttu-id="e6317-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e6317-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="e6317-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6317-102">SYNOPSIS</span></span>
<span data-ttu-id="e6317-103">Az események esemény rácsvonal-tartományba való közzétételéhez használt megosztott hozzáférési kulcsokat kapja.</span><span class="sxs-lookup"><span data-stu-id="e6317-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="e6317-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6317-104">SYNTAX</span></span>

### <span data-ttu-id="e6317-105">DomainNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6317-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6317-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6317-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6317-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6317-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6317-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6317-108">DESCRIPTION</span></span>
<span data-ttu-id="e6317-109">Az események esemény rácsvonal-tartományba való közzétételéhez használt megosztott hozzáférési kulcsokat kapja.</span><span class="sxs-lookup"><span data-stu-id="e6317-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="e6317-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e6317-110">EXAMPLES</span></span>

### <span data-ttu-id="e6317-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e6317-111">Example 1</span></span>

<span data-ttu-id="e6317-112">Megkapja az esemény rácsa Domain1 az erőforráscsoport MyResourceGroupName megosztott hozzáférés kulcsait \` \` \` \` .</span><span class="sxs-lookup"><span data-stu-id="e6317-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="e6317-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e6317-113">Example 2</span></span>

<span data-ttu-id="e6317-114">Megkapja az esemény rácsa Domain1 az erőforráscsoport MyResourceGroupName megosztott hozzáférés kulcsait \` \` \` \` .</span><span class="sxs-lookup"><span data-stu-id="e6317-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="e6317-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6317-115">PARAMETERS</span></span>

### <span data-ttu-id="e6317-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6317-116">-DefaultProfile</span></span>
<span data-ttu-id="e6317-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6317-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6317-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="e6317-118">-DomainObject</span></span>
<span data-ttu-id="e6317-119">EventGrid tartomány objektuma.</span><span class="sxs-lookup"><span data-stu-id="e6317-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6317-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="e6317-120">-DomainResourceId</span></span>
<span data-ttu-id="e6317-121">Az esemény rácsát jelképező erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e6317-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="e6317-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6317-122">-Name</span></span>
<span data-ttu-id="e6317-123">EventGrid-tartomány neve.</span><span class="sxs-lookup"><span data-stu-id="e6317-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6317-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6317-124">-ResourceGroupName</span></span>
<span data-ttu-id="e6317-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6317-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6317-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6317-126">CommonParameters</span></span>
<span data-ttu-id="e6317-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6317-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6317-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e6317-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6317-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6317-129">INPUTS</span></span>

### <span data-ttu-id="e6317-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e6317-130">System.String</span></span>

### <span data-ttu-id="e6317-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="e6317-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="e6317-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6317-132">OUTPUTS</span></span>

### <span data-ttu-id="e6317-133">Microsoft. Azure. Management. EventGrid. models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="e6317-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="e6317-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6317-134">NOTES</span></span>

## <span data-ttu-id="e6317-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6317-135">RELATED LINKS</span></span>
