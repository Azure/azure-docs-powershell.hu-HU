---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 0fbf44e9a68a5cfaaea4138ec17caa2960a41e67
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151258"
---
# <span data-ttu-id="74c63-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="74c63-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="74c63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74c63-102">SYNOPSIS</span></span>
<span data-ttu-id="74c63-103">Eltávolít egy új társviszony-létesítő szolgáltatás előtagot</span><span class="sxs-lookup"><span data-stu-id="74c63-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="74c63-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="74c63-104">SYNTAX</span></span>

### <span data-ttu-id="74c63-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="74c63-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74c63-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="74c63-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74c63-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="74c63-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74c63-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="74c63-108">DESCRIPTION</span></span>
<span data-ttu-id="74c63-109">Eltávolítja a társviszony-létesítő szolgáltatás előtagját egy társviszony-létesítő szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="74c63-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="74c63-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="74c63-110">EXAMPLES</span></span>

### <span data-ttu-id="74c63-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="74c63-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="74c63-112">Előtag eltávolítása társviszony-szolgáltatási objektumból</span><span class="sxs-lookup"><span data-stu-id="74c63-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="74c63-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="74c63-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="74c63-114">Előtag eltávolítása egy társviszony-szolgáltatáserőforrás-azonosítóból.</span><span class="sxs-lookup"><span data-stu-id="74c63-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="74c63-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="74c63-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="74c63-116">Előtag eltávolítása egy társviszony-szolgáltatáserőforrás-csoport nevéből és nevéből</span><span class="sxs-lookup"><span data-stu-id="74c63-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="74c63-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74c63-117">PARAMETERS</span></span>

### <span data-ttu-id="74c63-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74c63-118">-AsJob</span></span>
<span data-ttu-id="74c63-119">Futtassa a háttérben.</span><span class="sxs-lookup"><span data-stu-id="74c63-119">Run in the background.</span></span>

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

### <span data-ttu-id="74c63-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c63-120">-DefaultProfile</span></span>
<span data-ttu-id="74c63-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74c63-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74c63-122">-Force</span><span class="sxs-lookup"><span data-stu-id="74c63-122">-Force</span></span>
<span data-ttu-id="74c63-123">A művelet befejezésének kényszerítése</span><span class="sxs-lookup"><span data-stu-id="74c63-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="74c63-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74c63-124">-InputObject</span></span>
<span data-ttu-id="74c63-125">Használjon Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="74c63-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74c63-126">-Name</span><span class="sxs-lookup"><span data-stu-id="74c63-126">-Name</span></span>
<span data-ttu-id="74c63-127">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="74c63-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="74c63-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74c63-128">-PassThru</span></span>
<span data-ttu-id="74c63-129">Igaz értéket ad eredményül a sikerhez, a hamis értéket pedig a sikertelenséghez.</span><span class="sxs-lookup"><span data-stu-id="74c63-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="74c63-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="74c63-130">-PrefixName</span></span>
<span data-ttu-id="74c63-131">Az előtag neve.</span><span class="sxs-lookup"><span data-stu-id="74c63-131">The name of prefix.</span></span>

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

### <span data-ttu-id="74c63-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74c63-132">-ResourceGroupName</span></span>
<span data-ttu-id="74c63-133">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="74c63-133">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="74c63-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74c63-134">-ResourceId</span></span>
<span data-ttu-id="74c63-135">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="74c63-135">The resource id string name.</span></span>

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

### <span data-ttu-id="74c63-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74c63-136">-Confirm</span></span>
<span data-ttu-id="74c63-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="74c63-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74c63-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74c63-138">-WhatIf</span></span>
<span data-ttu-id="74c63-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="74c63-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74c63-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74c63-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74c63-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c63-141">CommonParameters</span></span>
<span data-ttu-id="74c63-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74c63-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c63-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74c63-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c63-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74c63-144">INPUTS</span></span>

### <span data-ttu-id="74c63-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="74c63-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="74c63-146">System.String</span><span class="sxs-lookup"><span data-stu-id="74c63-146">System.String</span></span>

## <span data-ttu-id="74c63-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74c63-147">OUTPUTS</span></span>

### <span data-ttu-id="74c63-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="74c63-148">System.Boolean</span></span>

## <span data-ttu-id="74c63-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="74c63-149">NOTES</span></span>

## <span data-ttu-id="74c63-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74c63-150">RELATED LINKS</span></span>
