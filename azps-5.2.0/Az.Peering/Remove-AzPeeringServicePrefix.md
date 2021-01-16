---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 0fbf44e9a68a5cfaaea4138ec17caa2960a41e67
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338046"
---
# <span data-ttu-id="c40d5-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="c40d5-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="c40d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c40d5-102">SYNOPSIS</span></span>
<span data-ttu-id="c40d5-103">Eltávolít egy új társviszony-létesítő szolgáltatás előtagot</span><span class="sxs-lookup"><span data-stu-id="c40d5-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="c40d5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c40d5-104">SYNTAX</span></span>

### <span data-ttu-id="c40d5-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c40d5-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c40d5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c40d5-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c40d5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c40d5-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c40d5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c40d5-108">DESCRIPTION</span></span>
<span data-ttu-id="c40d5-109">Eltávolítja a társviszony-létesítő szolgáltatás előtagját egy társviszony-létesítő szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="c40d5-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="c40d5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c40d5-110">EXAMPLES</span></span>

### <span data-ttu-id="c40d5-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c40d5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="c40d5-112">Előtag eltávolítása társviszony-szolgáltatási objektumból</span><span class="sxs-lookup"><span data-stu-id="c40d5-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="c40d5-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c40d5-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="c40d5-114">Előtag eltávolítása egy társviszony-szolgáltatáserőforrás-azonosítóból.</span><span class="sxs-lookup"><span data-stu-id="c40d5-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="c40d5-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="c40d5-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="c40d5-116">Előtag eltávolítása egy társviszony-szolgáltatáserőforrás-csoport nevéből és nevéből</span><span class="sxs-lookup"><span data-stu-id="c40d5-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="c40d5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c40d5-117">PARAMETERS</span></span>

### <span data-ttu-id="c40d5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c40d5-118">-AsJob</span></span>
<span data-ttu-id="c40d5-119">Futtassa a háttérben.</span><span class="sxs-lookup"><span data-stu-id="c40d5-119">Run in the background.</span></span>

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

### <span data-ttu-id="c40d5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c40d5-120">-DefaultProfile</span></span>
<span data-ttu-id="c40d5-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c40d5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c40d5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c40d5-122">-Force</span></span>
<span data-ttu-id="c40d5-123">A művelet befejezésének kényszerítése</span><span class="sxs-lookup"><span data-stu-id="c40d5-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="c40d5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c40d5-124">-InputObject</span></span>
<span data-ttu-id="c40d5-125">A Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="c40d5-125">Use a Get-AzPeeringServicePrefix</span></span>

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

### <span data-ttu-id="c40d5-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c40d5-126">-Name</span></span>
<span data-ttu-id="c40d5-127">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="c40d5-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="c40d5-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c40d5-128">-PassThru</span></span>
<span data-ttu-id="c40d5-129">Igaz értéket ad eredményül a sikerhez, a hamis értéket pedig nem sikerült értékhez.</span><span class="sxs-lookup"><span data-stu-id="c40d5-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="c40d5-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="c40d5-130">-PrefixName</span></span>
<span data-ttu-id="c40d5-131">Az előtag neve.</span><span class="sxs-lookup"><span data-stu-id="c40d5-131">The name of prefix.</span></span>

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

### <span data-ttu-id="c40d5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c40d5-132">-ResourceGroupName</span></span>
<span data-ttu-id="c40d5-133">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="c40d5-133">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="c40d5-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c40d5-134">-ResourceId</span></span>
<span data-ttu-id="c40d5-135">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="c40d5-135">The resource id string name.</span></span>

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

### <span data-ttu-id="c40d5-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c40d5-136">-Confirm</span></span>
<span data-ttu-id="c40d5-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c40d5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c40d5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c40d5-138">-WhatIf</span></span>
<span data-ttu-id="c40d5-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c40d5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c40d5-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c40d5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c40d5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c40d5-141">CommonParameters</span></span>
<span data-ttu-id="c40d5-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c40d5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c40d5-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c40d5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c40d5-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c40d5-144">INPUTS</span></span>

### <span data-ttu-id="c40d5-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="c40d5-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="c40d5-146">System.String</span><span class="sxs-lookup"><span data-stu-id="c40d5-146">System.String</span></span>

## <span data-ttu-id="c40d5-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c40d5-147">OUTPUTS</span></span>

### <span data-ttu-id="c40d5-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c40d5-148">System.Boolean</span></span>

## <span data-ttu-id="c40d5-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c40d5-149">NOTES</span></span>

## <span data-ttu-id="c40d5-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c40d5-150">RELATED LINKS</span></span>
