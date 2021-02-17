---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169491"
---
# <span data-ttu-id="eef70-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="eef70-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="eef70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eef70-102">SYNOPSIS</span></span>
<span data-ttu-id="eef70-103">Regisztrált előtagokat hozhat létre társviszony-objektumokhoz.</span><span class="sxs-lookup"><span data-stu-id="eef70-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="eef70-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eef70-104">SYNTAX</span></span>

### <span data-ttu-id="eef70-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eef70-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eef70-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="eef70-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eef70-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="eef70-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eef70-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eef70-108">DESCRIPTION</span></span>
<span data-ttu-id="eef70-109">Regisztrált előtagokat hozhat létre társviszony-objektumokhoz.</span><span class="sxs-lookup"><span data-stu-id="eef70-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="eef70-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eef70-110">EXAMPLES</span></span>

### <span data-ttu-id="eef70-111">Társviszony létrehozása és regisztrált előtag létrehozása</span><span class="sxs-lookup"><span data-stu-id="eef70-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="eef70-112">Szerezze be azt a társviszonyt, amelybe regisztrált előtagot szeretne felvenni.</span><span class="sxs-lookup"><span data-stu-id="eef70-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="eef70-113">Ezután adja át a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="eef70-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="eef70-114">Regisztrált asn létrehozása társviszony-erőforrásazonosítóval</span><span class="sxs-lookup"><span data-stu-id="eef70-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="eef70-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eef70-115">PARAMETERS</span></span>

### <span data-ttu-id="eef70-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eef70-116">-AsJob</span></span>
<span data-ttu-id="eef70-117">Futtassa a háttérben.</span><span class="sxs-lookup"><span data-stu-id="eef70-117">Run in the background.</span></span>

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

### <span data-ttu-id="eef70-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef70-118">-DefaultProfile</span></span>
<span data-ttu-id="eef70-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eef70-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eef70-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eef70-120">-InputObject</span></span>
<span data-ttu-id="eef70-121">Használjon Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="eef70-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="eef70-122">-Name</span><span class="sxs-lookup"><span data-stu-id="eef70-122">-Name</span></span>
<span data-ttu-id="eef70-123">Az előtag neve.</span><span class="sxs-lookup"><span data-stu-id="eef70-123">The name of prefix.</span></span>

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

### <span data-ttu-id="eef70-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="eef70-124">-PeeringName</span></span>
<span data-ttu-id="eef70-125">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="eef70-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="eef70-126">-Előtag</span><span class="sxs-lookup"><span data-stu-id="eef70-126">-Prefix</span></span>
<span data-ttu-id="eef70-127">A munkamenet IPv4-előtagja</span><span class="sxs-lookup"><span data-stu-id="eef70-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="eef70-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eef70-128">-ResourceGroupName</span></span>
<span data-ttu-id="eef70-129">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="eef70-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="eef70-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eef70-130">-ResourceId</span></span>
<span data-ttu-id="eef70-131">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="eef70-131">The resource id string name.</span></span>

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

### <span data-ttu-id="eef70-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eef70-132">-Confirm</span></span>
<span data-ttu-id="eef70-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="eef70-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eef70-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eef70-134">-WhatIf</span></span>
<span data-ttu-id="eef70-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="eef70-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eef70-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eef70-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eef70-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef70-137">CommonParameters</span></span>
<span data-ttu-id="eef70-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eef70-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef70-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eef70-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef70-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eef70-140">INPUTS</span></span>

### <span data-ttu-id="eef70-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="eef70-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="eef70-142">System.String</span><span class="sxs-lookup"><span data-stu-id="eef70-142">System.String</span></span>

## <span data-ttu-id="eef70-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eef70-143">OUTPUTS</span></span>

### <span data-ttu-id="eef70-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="eef70-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="eef70-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eef70-145">NOTES</span></span>

## <span data-ttu-id="eef70-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eef70-146">RELATED LINKS</span></span>
