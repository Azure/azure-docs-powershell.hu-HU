---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: 52eae037fb3c41940b1e1b67235f0affe729a41f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670168"
---
# <span data-ttu-id="aa3cc-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="aa3cc-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="aa3cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa3cc-102">SYNOPSIS</span></span>
<span data-ttu-id="aa3cc-103">Eltávolít egy ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="aa3cc-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="aa3cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa3cc-104">SYNTAX</span></span>

### <span data-ttu-id="aa3cc-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aa3cc-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa3cc-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa3cc-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa3cc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa3cc-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa3cc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa3cc-108">DESCRIPTION</span></span>
<span data-ttu-id="aa3cc-109">A **Remove-AzExpressRoutePort** parancsmag eltávolítja a ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="aa3cc-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="aa3cc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="aa3cc-110">EXAMPLES</span></span>

### <span data-ttu-id="aa3cc-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aa3cc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="aa3cc-112">Eltávolítja a $PortName ExpressRoutePort erőforrást az előfizetésben $rg erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="aa3cc-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="aa3cc-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="aa3cc-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="aa3cc-114">Eltávolítja a ExpressRoutePort-erőforrást a InputObject.</span><span class="sxs-lookup"><span data-stu-id="aa3cc-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="aa3cc-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="aa3cc-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="aa3cc-116">Eltávolítja a ExpressRoutePort erőforrást a ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="aa3cc-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="aa3cc-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa3cc-117">PARAMETERS</span></span>

### <span data-ttu-id="aa3cc-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa3cc-118">-AsJob</span></span>
<span data-ttu-id="aa3cc-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="aa3cc-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa3cc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa3cc-120">-DefaultProfile</span></span>
<span data-ttu-id="aa3cc-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa3cc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa3cc-122">-Force</span><span class="sxs-lookup"><span data-stu-id="aa3cc-122">-Force</span></span>
<span data-ttu-id="aa3cc-123">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="aa3cc-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="aa3cc-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa3cc-124">-InputObject</span></span>
<span data-ttu-id="aa3cc-125">Az Express Route port objektum</span><span class="sxs-lookup"><span data-stu-id="aa3cc-125">The express route port object</span></span>

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

### <span data-ttu-id="aa3cc-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aa3cc-126">-Name</span></span>
<span data-ttu-id="aa3cc-127">A ExpressRoutePort neve.</span><span class="sxs-lookup"><span data-stu-id="aa3cc-127">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="aa3cc-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa3cc-128">-PassThru</span></span>
<span data-ttu-id="aa3cc-129">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="aa3cc-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="aa3cc-130">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="aa3cc-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aa3cc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa3cc-131">-ResourceGroupName</span></span>
<span data-ttu-id="aa3cc-132">A ExpressRoutePort erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aa3cc-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="aa3cc-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa3cc-133">-ResourceId</span></span>
<span data-ttu-id="aa3cc-134">Az Express Route port ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa3cc-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="aa3cc-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aa3cc-135">-Confirm</span></span>
<span data-ttu-id="aa3cc-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa3cc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa3cc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa3cc-137">-WhatIf</span></span>
<span data-ttu-id="aa3cc-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aa3cc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa3cc-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aa3cc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa3cc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa3cc-140">CommonParameters</span></span>
<span data-ttu-id="aa3cc-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa3cc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa3cc-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa3cc-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa3cc-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa3cc-143">INPUTS</span></span>

### <span data-ttu-id="aa3cc-144">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="aa3cc-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="aa3cc-145">System. String</span><span class="sxs-lookup"><span data-stu-id="aa3cc-145">System.String</span></span>

## <span data-ttu-id="aa3cc-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa3cc-146">OUTPUTS</span></span>

### <span data-ttu-id="aa3cc-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa3cc-147">System.Boolean</span></span>

## <span data-ttu-id="aa3cc-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa3cc-148">NOTES</span></span>

## <span data-ttu-id="aa3cc-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa3cc-149">RELATED LINKS</span></span>

[<span data-ttu-id="aa3cc-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="aa3cc-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="aa3cc-151">Új – AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="aa3cc-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="aa3cc-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="aa3cc-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
