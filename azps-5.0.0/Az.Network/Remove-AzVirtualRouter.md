---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 691abfe3f6ca58e1fbef6c1120ce13b64fd62566
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301802"
---
# <span data-ttu-id="2e714-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="2e714-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="2e714-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e714-102">SYNOPSIS</span></span>
<span data-ttu-id="2e714-103">Egy Azure-VirtualRouter törlése</span><span class="sxs-lookup"><span data-stu-id="2e714-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="2e714-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e714-104">SYNTAX</span></span>

### <span data-ttu-id="2e714-105">VirtualRouterNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e714-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e714-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e714-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e714-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e714-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e714-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e714-108">DESCRIPTION</span></span>
<span data-ttu-id="2e714-109">A **Remove-AzVirtualRouter** parancsmag töröl egy Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="2e714-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="2e714-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2e714-110">EXAMPLES</span></span>

### <span data-ttu-id="2e714-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2e714-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="2e714-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="2e714-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="2e714-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="2e714-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="2e714-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e714-114">PARAMETERS</span></span>

### <span data-ttu-id="2e714-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e714-115">-AsJob</span></span>
<span data-ttu-id="2e714-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2e714-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e714-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e714-117">-DefaultProfile</span></span>
<span data-ttu-id="2e714-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e714-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e714-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2e714-119">-Force</span></span>
<span data-ttu-id="2e714-120">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e714-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2e714-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e714-121">-InputObject</span></span>
<span data-ttu-id="2e714-122">A virtuális útválasztó bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="2e714-122">The virtual router input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouter
Parameter Sets: VirtualRouterInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e714-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e714-123">-PassThru</span></span>
<span data-ttu-id="2e714-124">Egy olyan objektumot ad eredményül, amely azt az elemet jeleníti meg, amelyen a művelet végre van hajtva.</span><span class="sxs-lookup"><span data-stu-id="2e714-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="2e714-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e714-125">-ResourceGroupName</span></span>
<span data-ttu-id="2e714-126">A virtuális útválasztó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2e714-126">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e714-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e714-127">-ResourceId</span></span>
<span data-ttu-id="2e714-128">A virtuális útválasztó erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2e714-128">The virtual router resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e714-129">-RouterName</span><span class="sxs-lookup"><span data-stu-id="2e714-129">-RouterName</span></span>
<span data-ttu-id="2e714-130">A virtuális útválasztó neve.</span><span class="sxs-lookup"><span data-stu-id="2e714-130">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e714-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e714-131">-Confirm</span></span>
<span data-ttu-id="2e714-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e714-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e714-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e714-133">-WhatIf</span></span>
<span data-ttu-id="2e714-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e714-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e714-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e714-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e714-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e714-136">CommonParameters</span></span>
<span data-ttu-id="2e714-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e714-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e714-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2e714-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e714-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e714-139">INPUTS</span></span>

### <span data-ttu-id="2e714-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2e714-140">System.String</span></span>

### <span data-ttu-id="2e714-141">Microsoft. Azure. commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="2e714-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="2e714-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e714-142">OUTPUTS</span></span>

### <span data-ttu-id="2e714-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2e714-143">System.Boolean</span></span>

## <span data-ttu-id="2e714-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e714-144">NOTES</span></span>

## <span data-ttu-id="2e714-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e714-145">RELATED LINKS</span></span>
