---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 83d36cfdb892cc5366aabb589f3536e18e79eace
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182932"
---
# <span data-ttu-id="2b7c8-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="2b7c8-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="2b7c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b7c8-102">SYNOPSIS</span></span>
<span data-ttu-id="2b7c8-103">Regisztrált előtagot állít be vagy frissít a fölérendelt társközi erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="2b7c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b7c8-104">SYNTAX</span></span>

### <span data-ttu-id="2b7c8-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2b7c8-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b7c8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2b7c8-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b7c8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2b7c8-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b7c8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b7c8-108">DESCRIPTION</span></span>
<span data-ttu-id="2b7c8-109">Lehetővé teszi egy regisztrált előtag frissítését a fölérendelt társközi erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="2b7c8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2b7c8-110">EXAMPLES</span></span>

### <span data-ttu-id="2b7c8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2b7c8-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="2b7c8-112">Frissíti az előtagot erőforrás-azonosító szerint.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="2b7c8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b7c8-113">PARAMETERS</span></span>

### <span data-ttu-id="2b7c8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b7c8-114">-AsJob</span></span>
<span data-ttu-id="2b7c8-115">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-115">Run in the background.</span></span>

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

### <span data-ttu-id="2b7c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b7c8-116">-DefaultProfile</span></span>
<span data-ttu-id="2b7c8-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b7c8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b7c8-118">-InputObject</span></span>
<span data-ttu-id="2b7c8-119">Get-AzPeering használata</span><span class="sxs-lookup"><span data-stu-id="2b7c8-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7c8-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2b7c8-120">-Name</span></span>
<span data-ttu-id="2b7c8-121">Az előtag neve.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-121">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7c8-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="2b7c8-122">-PeeringName</span></span>
<span data-ttu-id="2b7c8-123">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="2b7c8-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="2b7c8-124">-Prefix</span></span>
<span data-ttu-id="2b7c8-125">A munkamenet IPv4-előtagja</span><span class="sxs-lookup"><span data-stu-id="2b7c8-125">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="2b7c8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b7c8-126">-ResourceGroupName</span></span>
<span data-ttu-id="2b7c8-127">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="2b7c8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b7c8-128">-ResourceId</span></span>
<span data-ttu-id="2b7c8-129">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-129">The resource id string name.</span></span>

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

### <span data-ttu-id="2b7c8-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2b7c8-130">-Confirm</span></span>
<span data-ttu-id="2b7c8-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b7c8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b7c8-132">-WhatIf</span></span>
<span data-ttu-id="2b7c8-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b7c8-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b7c8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b7c8-135">CommonParameters</span></span>
<span data-ttu-id="2b7c8-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b7c8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b7c8-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2b7c8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b7c8-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b7c8-138">INPUTS</span></span>

### <span data-ttu-id="2b7c8-139">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="2b7c8-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="2b7c8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2b7c8-140">System.String</span></span>

## <span data-ttu-id="2b7c8-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b7c8-141">OUTPUTS</span></span>

### <span data-ttu-id="2b7c8-142">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="2b7c8-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="2b7c8-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b7c8-143">NOTES</span></span>

## <span data-ttu-id="2b7c8-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b7c8-144">RELATED LINKS</span></span>
