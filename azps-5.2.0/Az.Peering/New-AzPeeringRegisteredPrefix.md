---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347394"
---
# <span data-ttu-id="8f0f5-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="8f0f5-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="8f0f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f0f5-102">SYNOPSIS</span></span>
<span data-ttu-id="8f0f5-103">Regisztrált előtagokat hozhat létre társviszony-objektumokhoz.</span><span class="sxs-lookup"><span data-stu-id="8f0f5-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="8f0f5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8f0f5-104">SYNTAX</span></span>

### <span data-ttu-id="8f0f5-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8f0f5-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f0f5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8f0f5-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f0f5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8f0f5-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f0f5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8f0f5-108">DESCRIPTION</span></span>
<span data-ttu-id="8f0f5-109">Regisztrált előtagokat hozhat létre társviszony-objektumokhoz.</span><span class="sxs-lookup"><span data-stu-id="8f0f5-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="8f0f5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8f0f5-110">EXAMPLES</span></span>

### <span data-ttu-id="8f0f5-111">Társviszony létrehozása és regisztrált előtag létrehozása</span><span class="sxs-lookup"><span data-stu-id="8f0f5-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="8f0f5-112">Szerezze be azt a társviszonyt, amelybe regisztrált előtagot szeretne felvenni.</span><span class="sxs-lookup"><span data-stu-id="8f0f5-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="8f0f5-113">Ezután adja át a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="8f0f5-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="8f0f5-114">Regisztrált asn létrehozása társviszony-erőforrásazonosítóval</span><span class="sxs-lookup"><span data-stu-id="8f0f5-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="8f0f5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f0f5-115">PARAMETERS</span></span>

### <span data-ttu-id="8f0f5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f0f5-116">-AsJob</span></span>
<span data-ttu-id="8f0f5-117">Futtassa a háttérben.</span><span class="sxs-lookup"><span data-stu-id="8f0f5-117">Run in the background.</span></span>

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

### <span data-ttu-id="8f0f5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f0f5-118">-DefaultProfile</span></span>
<span data-ttu-id="8f0f5-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f0f5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f0f5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f0f5-120">-InputObject</span></span>
<span data-ttu-id="8f0f5-121">A Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="8f0f5-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="8f0f5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8f0f5-122">-Name</span></span>
<span data-ttu-id="8f0f5-123">Az előtag neve.</span><span class="sxs-lookup"><span data-stu-id="8f0f5-123">The name of prefix.</span></span>

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

### <span data-ttu-id="8f0f5-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="8f0f5-124">-PeeringName</span></span>
<span data-ttu-id="8f0f5-125">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="8f0f5-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="8f0f5-126">-Előtag</span><span class="sxs-lookup"><span data-stu-id="8f0f5-126">-Prefix</span></span>
<span data-ttu-id="8f0f5-127">A munkamenet IPv4-előtagja</span><span class="sxs-lookup"><span data-stu-id="8f0f5-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="8f0f5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f0f5-128">-ResourceGroupName</span></span>
<span data-ttu-id="8f0f5-129">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="8f0f5-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="8f0f5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f0f5-130">-ResourceId</span></span>
<span data-ttu-id="8f0f5-131">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="8f0f5-131">The resource id string name.</span></span>

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

### <span data-ttu-id="8f0f5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f0f5-132">-Confirm</span></span>
<span data-ttu-id="8f0f5-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8f0f5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f0f5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f0f5-134">-WhatIf</span></span>
<span data-ttu-id="8f0f5-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8f0f5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f0f5-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f0f5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f0f5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f0f5-137">CommonParameters</span></span>
<span data-ttu-id="8f0f5-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f0f5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f0f5-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f0f5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f0f5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f0f5-140">INPUTS</span></span>

### <span data-ttu-id="8f0f5-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="8f0f5-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="8f0f5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8f0f5-142">System.String</span></span>

## <span data-ttu-id="8f0f5-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f0f5-143">OUTPUTS</span></span>

### <span data-ttu-id="8f0f5-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="8f0f5-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="8f0f5-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8f0f5-145">NOTES</span></span>

## <span data-ttu-id="8f0f5-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f0f5-146">RELATED LINKS</span></span>
