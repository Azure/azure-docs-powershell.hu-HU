---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: 7e6ee711de551de00a54930be2bdb285998e3ccb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366839"
---
# <span data-ttu-id="71b7a-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="71b7a-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="71b7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71b7a-102">SYNOPSIS</span></span>
<span data-ttu-id="71b7a-103">Eltávolít egy ExpressRoutePortot.</span><span class="sxs-lookup"><span data-stu-id="71b7a-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="71b7a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="71b7a-104">SYNTAX</span></span>

### <span data-ttu-id="71b7a-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="71b7a-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71b7a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71b7a-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71b7a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71b7a-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71b7a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="71b7a-108">DESCRIPTION</span></span>
<span data-ttu-id="71b7a-109">A **Remove-AzExpressRoutePort** parancsmag eltávolítja az ExpressRoutePortot.</span><span class="sxs-lookup"><span data-stu-id="71b7a-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="71b7a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="71b7a-110">EXAMPLES</span></span>

### <span data-ttu-id="71b7a-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="71b7a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="71b7a-112">Eltávolítja $PortName ExpressRoutePort-erőforrást $rg erőforráscsoportból az előfizetésében.</span><span class="sxs-lookup"><span data-stu-id="71b7a-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="71b7a-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="71b7a-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="71b7a-114">Eltávolítja az ExpressRoutePort erőforrást az InputObjectben.</span><span class="sxs-lookup"><span data-stu-id="71b7a-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="71b7a-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="71b7a-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="71b7a-116">Eltávolítja az ExpressRoutePort erőforrást a ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="71b7a-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="71b7a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71b7a-117">PARAMETERS</span></span>

### <span data-ttu-id="71b7a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71b7a-118">-AsJob</span></span>
<span data-ttu-id="71b7a-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="71b7a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71b7a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71b7a-120">-DefaultProfile</span></span>
<span data-ttu-id="71b7a-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71b7a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71b7a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="71b7a-122">-Force</span></span>
<span data-ttu-id="71b7a-123">Ne kérjen megerősítést, ha erőforrást szeretne törölni</span><span class="sxs-lookup"><span data-stu-id="71b7a-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="71b7a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71b7a-124">-InputObject</span></span>
<span data-ttu-id="71b7a-125">Az express route port objektum</span><span class="sxs-lookup"><span data-stu-id="71b7a-125">The express route port object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71b7a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="71b7a-126">-Name</span></span>
<span data-ttu-id="71b7a-127">Az ExpressRoutePort neve.</span><span class="sxs-lookup"><span data-stu-id="71b7a-127">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b7a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71b7a-128">-PassThru</span></span>
<span data-ttu-id="71b7a-129">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="71b7a-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="71b7a-130">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="71b7a-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="71b7a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71b7a-131">-ResourceGroupName</span></span>
<span data-ttu-id="71b7a-132">Az ExpressRoutePort erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="71b7a-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b7a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71b7a-133">-ResourceId</span></span>
<span data-ttu-id="71b7a-134">Az expressz útvonalport Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="71b7a-134">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b7a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71b7a-135">-Confirm</span></span>
<span data-ttu-id="71b7a-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="71b7a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71b7a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71b7a-137">-WhatIf</span></span>
<span data-ttu-id="71b7a-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="71b7a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71b7a-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71b7a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71b7a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b7a-140">CommonParameters</span></span>
<span data-ttu-id="71b7a-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71b7a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b7a-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71b7a-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b7a-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71b7a-143">INPUTS</span></span>

### <span data-ttu-id="71b7a-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="71b7a-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="71b7a-145">System.String</span><span class="sxs-lookup"><span data-stu-id="71b7a-145">System.String</span></span>

## <span data-ttu-id="71b7a-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71b7a-146">OUTPUTS</span></span>

### <span data-ttu-id="71b7a-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="71b7a-147">System.Boolean</span></span>

## <span data-ttu-id="71b7a-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="71b7a-148">NOTES</span></span>

## <span data-ttu-id="71b7a-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71b7a-149">RELATED LINKS</span></span>

[<span data-ttu-id="71b7a-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="71b7a-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="71b7a-151">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="71b7a-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="71b7a-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="71b7a-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
