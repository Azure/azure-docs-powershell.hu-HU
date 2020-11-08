---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184290"
---
# <span data-ttu-id="7c8c8-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="7c8c8-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="7c8c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c8c8-102">SYNOPSIS</span></span>
<span data-ttu-id="7c8c8-103">Létrehozhat regisztrált előtagokat a társközi objektumokhoz.</span><span class="sxs-lookup"><span data-stu-id="7c8c8-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="7c8c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c8c8-104">SYNTAX</span></span>

### <span data-ttu-id="7c8c8-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7c8c8-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c8c8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7c8c8-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c8c8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7c8c8-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c8c8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c8c8-108">DESCRIPTION</span></span>
<span data-ttu-id="7c8c8-109">Létrehozhat regisztrált előtagokat a társközi objektumokhoz.</span><span class="sxs-lookup"><span data-stu-id="7c8c8-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="7c8c8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7c8c8-110">EXAMPLES</span></span>

### <span data-ttu-id="7c8c8-111">A beolvasás és a regisztrált előtag létrehozása</span><span class="sxs-lookup"><span data-stu-id="7c8c8-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="7c8c8-112">Szerezzen be egy olyan partnert, aki regisztrált előtagot szeretne felvenni.</span><span class="sxs-lookup"><span data-stu-id="7c8c8-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="7c8c8-113">Ezután adja át a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7c8c8-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="7c8c8-114">Regisztrált ASN-resourceId létrehozása a társközi használattal</span><span class="sxs-lookup"><span data-stu-id="7c8c8-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="7c8c8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c8c8-115">PARAMETERS</span></span>

### <span data-ttu-id="7c8c8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c8c8-116">-AsJob</span></span>
<span data-ttu-id="7c8c8-117">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="7c8c8-117">Run in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8c8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c8c8-118">-DefaultProfile</span></span>
<span data-ttu-id="7c8c8-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c8c8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c8c8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c8c8-120">-InputObject</span></span>
<span data-ttu-id="7c8c8-121">Get-AzPeering használata</span><span class="sxs-lookup"><span data-stu-id="7c8c8-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8c8-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7c8c8-122">-Name</span></span>
<span data-ttu-id="7c8c8-123">Az előtag neve.</span><span class="sxs-lookup"><span data-stu-id="7c8c8-123">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8c8-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="7c8c8-124">-PeeringName</span></span>
<span data-ttu-id="7c8c8-125">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="7c8c8-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8c8-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="7c8c8-126">-Prefix</span></span>
<span data-ttu-id="7c8c8-127">A munkamenet IPv4-előtagja</span><span class="sxs-lookup"><span data-stu-id="7c8c8-127">The session IPv4 prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8c8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c8c8-128">-ResourceGroupName</span></span>
<span data-ttu-id="7c8c8-129">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="7c8c8-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8c8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c8c8-130">-ResourceId</span></span>
<span data-ttu-id="7c8c8-131">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="7c8c8-131">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8c8-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7c8c8-132">-Confirm</span></span>
<span data-ttu-id="7c8c8-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7c8c8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c8c8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c8c8-134">-WhatIf</span></span>
<span data-ttu-id="7c8c8-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7c8c8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c8c8-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c8c8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c8c8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c8c8-137">CommonParameters</span></span>
<span data-ttu-id="7c8c8-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c8c8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c8c8-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7c8c8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c8c8-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c8c8-140">INPUTS</span></span>

### <span data-ttu-id="7c8c8-141">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="7c8c8-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="7c8c8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7c8c8-142">System.String</span></span>

## <span data-ttu-id="7c8c8-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c8c8-143">OUTPUTS</span></span>

### <span data-ttu-id="7c8c8-144">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="7c8c8-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="7c8c8-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c8c8-145">NOTES</span></span>

## <span data-ttu-id="7c8c8-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c8c8-146">RELATED LINKS</span></span>
