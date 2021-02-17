---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 83d36cfdb892cc5366aabb589f3536e18e79eace
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169467"
---
# <span data-ttu-id="e315d-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="e315d-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="e315d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e315d-102">SYNOPSIS</span></span>
<span data-ttu-id="e315d-103">Beállítja vagy frissíti a szülő társviszony-erőforrás regisztrált előtagját.</span><span class="sxs-lookup"><span data-stu-id="e315d-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="e315d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e315d-104">SYNTAX</span></span>

### <span data-ttu-id="e315d-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e315d-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e315d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e315d-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e315d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e315d-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e315d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e315d-108">DESCRIPTION</span></span>
<span data-ttu-id="e315d-109">Lehetővé teszi egy regisztrált előtag frissítését a szülő társviszony-létesítő erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="e315d-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="e315d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e315d-110">EXAMPLES</span></span>

### <span data-ttu-id="e315d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e315d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="e315d-112">Erőforrás-azonosító szerint frissíti az előtagot.</span><span class="sxs-lookup"><span data-stu-id="e315d-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="e315d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e315d-113">PARAMETERS</span></span>

### <span data-ttu-id="e315d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e315d-114">-AsJob</span></span>
<span data-ttu-id="e315d-115">Futtassa a háttérben.</span><span class="sxs-lookup"><span data-stu-id="e315d-115">Run in the background.</span></span>

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

### <span data-ttu-id="e315d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e315d-116">-DefaultProfile</span></span>
<span data-ttu-id="e315d-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e315d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e315d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e315d-118">-InputObject</span></span>
<span data-ttu-id="e315d-119">Használjon Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="e315d-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="e315d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e315d-120">-Name</span></span>
<span data-ttu-id="e315d-121">Az előtag neve.</span><span class="sxs-lookup"><span data-stu-id="e315d-121">The name of prefix.</span></span>

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

### <span data-ttu-id="e315d-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="e315d-122">-PeeringName</span></span>
<span data-ttu-id="e315d-123">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="e315d-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e315d-124">-Előtag</span><span class="sxs-lookup"><span data-stu-id="e315d-124">-Prefix</span></span>
<span data-ttu-id="e315d-125">A munkamenet IPv4-előtagja</span><span class="sxs-lookup"><span data-stu-id="e315d-125">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="e315d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e315d-126">-ResourceGroupName</span></span>
<span data-ttu-id="e315d-127">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="e315d-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="e315d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e315d-128">-ResourceId</span></span>
<span data-ttu-id="e315d-129">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="e315d-129">The resource id string name.</span></span>

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

### <span data-ttu-id="e315d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e315d-130">-Confirm</span></span>
<span data-ttu-id="e315d-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e315d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e315d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e315d-132">-WhatIf</span></span>
<span data-ttu-id="e315d-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e315d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e315d-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e315d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e315d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e315d-135">CommonParameters</span></span>
<span data-ttu-id="e315d-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e315d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e315d-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e315d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e315d-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e315d-138">INPUTS</span></span>

### <span data-ttu-id="e315d-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="e315d-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="e315d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e315d-140">System.String</span></span>

## <span data-ttu-id="e315d-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e315d-141">OUTPUTS</span></span>

### <span data-ttu-id="e315d-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="e315d-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="e315d-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e315d-143">NOTES</span></span>

## <span data-ttu-id="e315d-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e315d-144">RELATED LINKS</span></span>
