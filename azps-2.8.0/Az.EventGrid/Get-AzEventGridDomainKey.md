---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: 4d72be4f7ddbe6cd5884269c724c7505cc05fffc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666540"
---
# <span data-ttu-id="d387b-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d387b-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="d387b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d387b-102">SYNOPSIS</span></span>
<span data-ttu-id="d387b-103">Az események esemény rácsvonal-tartományba való közzétételéhez használt megosztott hozzáférési kulcsokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d387b-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="d387b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d387b-104">SYNTAX</span></span>

### <span data-ttu-id="d387b-105">DomainNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d387b-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d387b-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d387b-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d387b-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d387b-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d387b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d387b-108">DESCRIPTION</span></span>
<span data-ttu-id="d387b-109">Az események esemény rácsvonal-tartományba való közzétételéhez használt megosztott hozzáférési kulcsokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d387b-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="d387b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d387b-110">EXAMPLES</span></span>

### <span data-ttu-id="d387b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d387b-111">Example 1</span></span>

<span data-ttu-id="d387b-112">Megkapja az esemény rácsa Domain1 az erőforráscsoport MyResourceGroupName megosztott hozzáférés kulcsait \` \` \` \` .</span><span class="sxs-lookup"><span data-stu-id="d387b-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="d387b-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="d387b-113">Example 2</span></span>

<span data-ttu-id="d387b-114">Megkapja az esemény rácsa Domain1 az erőforráscsoport MyResourceGroupName megosztott hozzáférés kulcsait \` \` \` \` .</span><span class="sxs-lookup"><span data-stu-id="d387b-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="d387b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d387b-115">PARAMETERS</span></span>

### <span data-ttu-id="d387b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d387b-116">-DefaultProfile</span></span>
<span data-ttu-id="d387b-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d387b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d387b-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="d387b-118">-DomainObject</span></span>
<span data-ttu-id="d387b-119">EventGrid tartomány objektuma.</span><span class="sxs-lookup"><span data-stu-id="d387b-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="d387b-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="d387b-120">-DomainResourceId</span></span>
<span data-ttu-id="d387b-121">Az esemény rácsát jelképező erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d387b-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="d387b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d387b-122">-Name</span></span>
<span data-ttu-id="d387b-123">EventGrid-tartomány neve.</span><span class="sxs-lookup"><span data-stu-id="d387b-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d387b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d387b-124">-ResourceGroupName</span></span>
<span data-ttu-id="d387b-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d387b-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d387b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d387b-126">CommonParameters</span></span>
<span data-ttu-id="d387b-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d387b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d387b-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d387b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d387b-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d387b-129">INPUTS</span></span>

### <span data-ttu-id="d387b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d387b-130">System.String</span></span>

### <span data-ttu-id="d387b-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="d387b-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="d387b-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d387b-132">OUTPUTS</span></span>

### <span data-ttu-id="d387b-133">Microsoft. Azure. Management. EventGrid. models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d387b-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="d387b-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d387b-134">NOTES</span></span>

## <span data-ttu-id="d387b-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d387b-135">RELATED LINKS</span></span>
