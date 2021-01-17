---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: b3d505d7c9412b15c2933ec03bb66af6f43a6b26
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372062"
---
# <span data-ttu-id="a556e-101">Remove-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="a556e-101">Remove-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="a556e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a556e-102">SYNOPSIS</span></span>
<span data-ttu-id="a556e-103">Törölhet vagy eltávolíthat egy regisztrált előtagot a szülő társviszony-erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="a556e-103">Delete or remove a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="a556e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a556e-104">SYNTAX</span></span>

### <span data-ttu-id="a556e-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a556e-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a556e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a556e-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredPrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a556e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a556e-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a556e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a556e-108">DESCRIPTION</span></span>
<span data-ttu-id="a556e-109">Lehetővé teszi a regisztrált előtag eltávolítását a szülő társviszony-erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="a556e-109">Allows the removal of registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="a556e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a556e-110">EXAMPLES</span></span>

### <span data-ttu-id="a556e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a556e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredPrefix -ResourceId $resourceId
```

<span data-ttu-id="a556e-112">Egy regisztrált előtag eltávolítása erőforrás-azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="a556e-112">Remove a registerd prefix by resource id.</span></span>

## <span data-ttu-id="a556e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a556e-113">PARAMETERS</span></span>

### <span data-ttu-id="a556e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a556e-114">-AsJob</span></span>
<span data-ttu-id="a556e-115">Futtassa a háttérben.</span><span class="sxs-lookup"><span data-stu-id="a556e-115">Run in the background.</span></span>

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

### <span data-ttu-id="a556e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a556e-116">-DefaultProfile</span></span>
<span data-ttu-id="a556e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a556e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a556e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a556e-118">-Force</span></span>
<span data-ttu-id="a556e-119">A művelet végrehajtásához</span><span class="sxs-lookup"><span data-stu-id="a556e-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="a556e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a556e-120">-InputObject</span></span>
<span data-ttu-id="a556e-121">A Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a556e-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a556e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a556e-122">-Name</span></span>
<span data-ttu-id="a556e-123">Az előtag neve.</span><span class="sxs-lookup"><span data-stu-id="a556e-123">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a556e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a556e-124">-PassThru</span></span>
<span data-ttu-id="a556e-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="a556e-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a556e-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="a556e-126">-PeeringName</span></span>
<span data-ttu-id="a556e-127">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="a556e-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a556e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a556e-128">-ResourceGroupName</span></span>
<span data-ttu-id="a556e-129">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="a556e-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a556e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a556e-130">-ResourceId</span></span>
<span data-ttu-id="a556e-131">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="a556e-131">The resource id string name.</span></span>

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

### <span data-ttu-id="a556e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a556e-132">-Confirm</span></span>
<span data-ttu-id="a556e-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a556e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a556e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a556e-134">-WhatIf</span></span>
<span data-ttu-id="a556e-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a556e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a556e-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a556e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a556e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a556e-137">CommonParameters</span></span>
<span data-ttu-id="a556e-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a556e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a556e-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a556e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a556e-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a556e-140">INPUTS</span></span>

### <span data-ttu-id="a556e-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="a556e-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="a556e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a556e-142">System.String</span></span>

## <span data-ttu-id="a556e-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a556e-143">OUTPUTS</span></span>

### <span data-ttu-id="a556e-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a556e-144">System.Boolean</span></span>

## <span data-ttu-id="a556e-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a556e-145">NOTES</span></span>

## <span data-ttu-id="a556e-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a556e-146">RELATED LINKS</span></span>
