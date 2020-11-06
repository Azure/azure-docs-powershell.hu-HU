---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRoutePort.md
ms.openlocfilehash: 5a9e4f7a4a3d7b8173cf7ef797edfc354d655cc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495017"
---
# <span data-ttu-id="fd7a6-101">Remove-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fd7a6-101">Remove-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="fd7a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd7a6-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7a6-103">Eltávolít egy ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="fd7a6-103">Removes an ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd7a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd7a6-104">SYNTAX</span></span>

### <span data-ttu-id="fd7a6-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd7a6-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd7a6-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd7a6-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd7a6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd7a6-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd7a6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd7a6-108">DESCRIPTION</span></span>
<span data-ttu-id="fd7a6-109">A **Remove-AzureRmExpressRoutePort** parancsmag eltávolítja a ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="fd7a6-109">The **Remove-AzureRmExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="fd7a6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fd7a6-110">EXAMPLES</span></span>

### <span data-ttu-id="fd7a6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fd7a6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="fd7a6-112">Eltávolítja a $PortName ExpressRoutePort erőforrást az előfizetésben $rg erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="fd7a6-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="fd7a6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="fd7a6-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -InputObject $erPort
```
<span data-ttu-id="fd7a6-114">Eltávolítja a ExpressRoutePort-erőforrást a InputObject.</span><span class="sxs-lookup"><span data-stu-id="fd7a6-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="fd7a6-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="fd7a6-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="fd7a6-116">Eltávolítja a ExpressRoutePort erőforrást a ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="fd7a6-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="fd7a6-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd7a6-117">PARAMETERS</span></span>

### <span data-ttu-id="fd7a6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd7a6-118">-AsJob</span></span>
<span data-ttu-id="fd7a6-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fd7a6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd7a6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7a6-120">-DefaultProfile</span></span>
<span data-ttu-id="fd7a6-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd7a6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd7a6-122">-Force</span><span class="sxs-lookup"><span data-stu-id="fd7a6-122">-Force</span></span>
<span data-ttu-id="fd7a6-123">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="fd7a6-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="fd7a6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd7a6-124">-InputObject</span></span>
<span data-ttu-id="fd7a6-125">Az Express Route port objektum</span><span class="sxs-lookup"><span data-stu-id="fd7a6-125">The express route port object</span></span>

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

### <span data-ttu-id="fd7a6-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd7a6-126">-Name</span></span>
<span data-ttu-id="fd7a6-127">A ExpressRoutePort neve.</span><span class="sxs-lookup"><span data-stu-id="fd7a6-127">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="fd7a6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd7a6-128">-PassThru</span></span>
<span data-ttu-id="fd7a6-129">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="fd7a6-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="fd7a6-130">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="fd7a6-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fd7a6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd7a6-131">-ResourceGroupName</span></span>
<span data-ttu-id="fd7a6-132">A ExpressRoutePort erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fd7a6-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="fd7a6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd7a6-133">-ResourceId</span></span>
<span data-ttu-id="fd7a6-134">Az Express Route port ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd7a6-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="fd7a6-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fd7a6-135">-Confirm</span></span>
<span data-ttu-id="fd7a6-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd7a6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd7a6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd7a6-137">-WhatIf</span></span>
<span data-ttu-id="fd7a6-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fd7a6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd7a6-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd7a6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd7a6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7a6-140">CommonParameters</span></span>
<span data-ttu-id="fd7a6-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd7a6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7a6-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd7a6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7a6-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd7a6-143">INPUTS</span></span>

### <span data-ttu-id="fd7a6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fd7a6-144">System.String</span></span>

### <span data-ttu-id="fd7a6-145">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fd7a6-145">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="fd7a6-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd7a6-146">OUTPUTS</span></span>

### <span data-ttu-id="fd7a6-147">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="fd7a6-147">System.Object</span></span>
## <span data-ttu-id="fd7a6-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd7a6-148">NOTES</span></span>

## <span data-ttu-id="fd7a6-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd7a6-149">RELATED LINKS</span></span>
