---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
ms.openlocfilehash: 5fc8f30a2ef8a0ee276c9fb7ac3f1e2a503f6ec4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939473"
---
# <span data-ttu-id="7b41d-101">Remove-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="7b41d-101">Remove-AzRouteServer</span></span>

## <span data-ttu-id="7b41d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b41d-102">SYNOPSIS</span></span>
<span data-ttu-id="7b41d-103">Töröl egy Azure RouteServer-kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="7b41d-103">Deletes an Azure RouteServer.</span></span>

## <span data-ttu-id="7b41d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7b41d-104">SYNTAX</span></span>

### <span data-ttu-id="7b41d-105">RouteServerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7b41d-105">RouteServerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b41d-106">RouteServerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b41d-106">RouteServerInputObjectParameterSet</span></span>
```
Remove-AzRouteServer -InputObject <PSRouteServer> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b41d-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b41d-107">RouteServerResourceIdParameterSet</span></span>
```
Remove-AzRouteServer -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b41d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7b41d-108">DESCRIPTION</span></span>
<span data-ttu-id="7b41d-109">A **Remove-AzRouteServer** parancsmag töröl egy Azure RouteServer-kiszolgálót</span><span class="sxs-lookup"><span data-stu-id="7b41d-109">The **Remove-AzRouteServer** cmdlet deletes an Azure RouteServer</span></span>

## <span data-ttu-id="7b41d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7b41d-110">EXAMPLES</span></span>

### <span data-ttu-id="7b41d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7b41d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="7b41d-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="7b41d-112">Example 2</span></span>
```powershell
PS C:\> $routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Remove-AzRouteServer -ResourceId $routeServerId
```

### <span data-ttu-id="7b41d-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="7b41d-113">Example 3</span></span>
```powershell
PS C:\> $routeServer = Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
Remove-AzRouteServer -InputObject $routeServer
```

## <span data-ttu-id="7b41d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b41d-114">PARAMETERS</span></span>

### <span data-ttu-id="7b41d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b41d-115">-AsJob</span></span>
<span data-ttu-id="7b41d-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7b41d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b41d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b41d-117">-DefaultProfile</span></span>
<span data-ttu-id="7b41d-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b41d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b41d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7b41d-119">-Force</span></span>
<span data-ttu-id="7b41d-120">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="7b41d-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7b41d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b41d-121">-InputObject</span></span>
<span data-ttu-id="7b41d-122">Az útvonalkiszolgáló bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="7b41d-122">The route server input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteServer
Parameter Sets: RouteServerInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b41d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b41d-123">-PassThru</span></span>
<span data-ttu-id="7b41d-124">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amelyen a műveletet végre kell hajtanunk.</span><span class="sxs-lookup"><span data-stu-id="7b41d-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="7b41d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b41d-125">-ResourceGroupName</span></span>
<span data-ttu-id="7b41d-126">Az útvonal-kiszolgáló erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="7b41d-126">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b41d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b41d-127">-ResourceId</span></span>
<span data-ttu-id="7b41d-128">Az útvonalkiszolgáló-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7b41d-128">The route server resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b41d-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="7b41d-129">-RouteServerName</span></span>
<span data-ttu-id="7b41d-130">Az útvonalkiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="7b41d-130">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b41d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b41d-131">-Confirm</span></span>
<span data-ttu-id="7b41d-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7b41d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b41d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b41d-133">-WhatIf</span></span>
<span data-ttu-id="7b41d-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7b41d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b41d-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b41d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b41d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b41d-136">CommonParameters</span></span>
<span data-ttu-id="7b41d-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b41d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b41d-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b41d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b41d-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b41d-139">INPUTS</span></span>

### <span data-ttu-id="7b41d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7b41d-140">System.String</span></span>

### <span data-ttu-id="7b41d-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="7b41d-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="7b41d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b41d-142">OUTPUTS</span></span>

### <span data-ttu-id="7b41d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7b41d-143">System.Boolean</span></span>

## <span data-ttu-id="7b41d-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7b41d-144">NOTES</span></span>

## <span data-ttu-id="7b41d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b41d-145">RELATED LINKS</span></span>
