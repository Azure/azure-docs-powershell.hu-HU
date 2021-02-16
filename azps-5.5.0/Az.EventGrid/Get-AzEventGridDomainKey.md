---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: c080a5132d5ed31828fbf7a35385432d3c91a923
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209599"
---
# <span data-ttu-id="db968-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="db968-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="db968-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db968-102">SYNOPSIS</span></span>
<span data-ttu-id="db968-103">Lekérte az események Eseményrács tartományba való közzétételéhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="db968-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="db968-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db968-104">SYNTAX</span></span>

### <span data-ttu-id="db968-105">DomainNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db968-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db968-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db968-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db968-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="db968-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db968-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db968-108">DESCRIPTION</span></span>
<span data-ttu-id="db968-109">Lekérte az események Eseményrács tartományba való közzétételéhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="db968-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="db968-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db968-110">EXAMPLES</span></span>

### <span data-ttu-id="db968-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="db968-111">Example 1</span></span>

<span data-ttu-id="db968-112">A \` MyResourceGroupName erőforráscsoport Eseményrács tartomány1 tartományának megosztott \` \` hozzáférési kulcsait kapja \` meg.</span><span class="sxs-lookup"><span data-stu-id="db968-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="db968-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="db968-113">Example 2</span></span>

<span data-ttu-id="db968-114">A \` MyResourceGroupName erőforráscsoport Eseményrács tartomány1 tartományának megosztott \` \` hozzáférési kulcsait kapja \` meg.</span><span class="sxs-lookup"><span data-stu-id="db968-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="db968-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db968-115">PARAMETERS</span></span>

### <span data-ttu-id="db968-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db968-116">-DefaultProfile</span></span>
<span data-ttu-id="db968-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db968-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db968-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="db968-118">-DomainObject</span></span>
<span data-ttu-id="db968-119">EventGrid Domain objektum.</span><span class="sxs-lookup"><span data-stu-id="db968-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="db968-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="db968-120">-DomainResourceId</span></span>
<span data-ttu-id="db968-121">Az Eseményrács tartományt képviselő erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="db968-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="db968-122">-Name</span><span class="sxs-lookup"><span data-stu-id="db968-122">-Name</span></span>
<span data-ttu-id="db968-123">EventGrid tartománynév.</span><span class="sxs-lookup"><span data-stu-id="db968-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="db968-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db968-124">-ResourceGroupName</span></span>
<span data-ttu-id="db968-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="db968-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="db968-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db968-126">CommonParameters</span></span>
<span data-ttu-id="db968-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db968-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db968-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db968-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db968-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db968-129">INPUTS</span></span>

### <span data-ttu-id="db968-130">System.String</span><span class="sxs-lookup"><span data-stu-id="db968-130">System.String</span></span>

### <span data-ttu-id="db968-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="db968-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="db968-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db968-132">OUTPUTS</span></span>

### <span data-ttu-id="db968-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="db968-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="db968-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db968-134">NOTES</span></span>

## <span data-ttu-id="db968-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db968-135">RELATED LINKS</span></span>
