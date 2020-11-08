---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: c080a5132d5ed31828fbf7a35385432d3c91a923
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185477"
---
# <span data-ttu-id="2f79d-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2f79d-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="2f79d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f79d-102">SYNOPSIS</span></span>
<span data-ttu-id="2f79d-103">Az események esemény rácsvonal-tartományba való közzétételéhez használt megosztott hozzáférési kulcsokat kapja.</span><span class="sxs-lookup"><span data-stu-id="2f79d-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="2f79d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f79d-104">SYNTAX</span></span>

### <span data-ttu-id="2f79d-105">DomainNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f79d-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f79d-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f79d-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f79d-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f79d-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f79d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f79d-108">DESCRIPTION</span></span>
<span data-ttu-id="2f79d-109">Az események esemény rácsvonal-tartományba való közzétételéhez használt megosztott hozzáférési kulcsokat kapja.</span><span class="sxs-lookup"><span data-stu-id="2f79d-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="2f79d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2f79d-110">EXAMPLES</span></span>

### <span data-ttu-id="2f79d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2f79d-111">Example 1</span></span>

<span data-ttu-id="2f79d-112">Megkapja az esemény rácsa Domain1 az erőforráscsoport MyResourceGroupName megosztott hozzáférés kulcsait \` \` \` \` .</span><span class="sxs-lookup"><span data-stu-id="2f79d-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="2f79d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2f79d-113">Example 2</span></span>

<span data-ttu-id="2f79d-114">Megkapja az esemény rácsa Domain1 az erőforráscsoport MyResourceGroupName megosztott hozzáférés kulcsait \` \` \` \` .</span><span class="sxs-lookup"><span data-stu-id="2f79d-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="2f79d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f79d-115">PARAMETERS</span></span>

### <span data-ttu-id="2f79d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f79d-116">-DefaultProfile</span></span>
<span data-ttu-id="2f79d-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f79d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f79d-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="2f79d-118">-DomainObject</span></span>
<span data-ttu-id="2f79d-119">EventGrid tartomány objektuma.</span><span class="sxs-lookup"><span data-stu-id="2f79d-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="2f79d-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="2f79d-120">-DomainResourceId</span></span>
<span data-ttu-id="2f79d-121">Az esemény rácsát jelképező erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2f79d-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="2f79d-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f79d-122">-Name</span></span>
<span data-ttu-id="2f79d-123">EventGrid-tartomány neve.</span><span class="sxs-lookup"><span data-stu-id="2f79d-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="2f79d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f79d-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f79d-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2f79d-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="2f79d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f79d-126">CommonParameters</span></span>
<span data-ttu-id="2f79d-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f79d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f79d-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2f79d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f79d-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f79d-129">INPUTS</span></span>

### <span data-ttu-id="2f79d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2f79d-130">System.String</span></span>

### <span data-ttu-id="2f79d-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="2f79d-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="2f79d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f79d-132">OUTPUTS</span></span>

### <span data-ttu-id="2f79d-133">Microsoft. Azure. Management. EventGrid. models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="2f79d-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="2f79d-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f79d-134">NOTES</span></span>

## <span data-ttu-id="2f79d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f79d-135">RELATED LINKS</span></span>
