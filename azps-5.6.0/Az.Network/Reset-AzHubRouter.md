---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 2261e3e0f9237985459dc69e06ba4f055dd86427
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923946"
---
# <span data-ttu-id="df541-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="df541-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="df541-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df541-102">SYNOPSIS</span></span>
<span data-ttu-id="df541-103">Alaphelyzetbe állítja egy VirtualHub-erőforrás RoutingState-ját.</span><span class="sxs-lookup"><span data-stu-id="df541-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="df541-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="df541-104">SYNTAX</span></span>

### <span data-ttu-id="df541-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df541-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df541-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="df541-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df541-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="df541-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df541-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="df541-108">DESCRIPTION</span></span>
<span data-ttu-id="df541-109">Csak akkor állítja alaphelyzetbe egy meglévő VirtualHub-erőforrás útválasztási állapotát, ha a virtuális központ Útválasztási állapota nincs kiépítve.</span><span class="sxs-lookup"><span data-stu-id="df541-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="df541-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="df541-110">EXAMPLES</span></span>

### <span data-ttu-id="df541-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="df541-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="df541-112">Állítsa alaphelyzetbe a virtuális központ útválasztási állapotát annak ResourceGroupName és ResourceName tulajdonságával.</span><span class="sxs-lookup"><span data-stu-id="df541-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="df541-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="df541-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="df541-114">Állítsa alaphelyzetbe a virtuális központ útválasztási állapotát annak ResourceId-ével.</span><span class="sxs-lookup"><span data-stu-id="df541-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="df541-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="df541-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="df541-116">Bemeneti objektum használatával állítsa alaphelyzetbe a virtuális központ útválasztási állapotát.</span><span class="sxs-lookup"><span data-stu-id="df541-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="df541-117">A bemeneti objektum PSVirtualHub típusú.</span><span class="sxs-lookup"><span data-stu-id="df541-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="df541-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="df541-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="df541-119">Egy meglévő virtuális központi objektum beolvasható, majd bemeneti objektumként átadott a Reset-AzHubRouternek.</span><span class="sxs-lookup"><span data-stu-id="df541-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="df541-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df541-120">PARAMETERS</span></span>

### <span data-ttu-id="df541-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df541-121">-AsJob</span></span>
<span data-ttu-id="df541-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="df541-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df541-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df541-123">-DefaultProfile</span></span>
<span data-ttu-id="df541-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df541-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df541-125">-Force</span><span class="sxs-lookup"><span data-stu-id="df541-125">-Force</span></span>
<span data-ttu-id="df541-126">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="df541-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="df541-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df541-127">-InputObject</span></span>
<span data-ttu-id="df541-128">A módosítva lévő virtuális központi objektum.</span><span class="sxs-lookup"><span data-stu-id="df541-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df541-129">-Name</span><span class="sxs-lookup"><span data-stu-id="df541-129">-Name</span></span>
<span data-ttu-id="df541-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="df541-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df541-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df541-131">-ResourceGroupName</span></span>
<span data-ttu-id="df541-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="df541-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df541-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df541-133">-ResourceId</span></span>
<span data-ttu-id="df541-134">A módosítani szükséges virtuális központ erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="df541-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df541-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df541-135">-Confirm</span></span>
<span data-ttu-id="df541-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="df541-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df541-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df541-137">-WhatIf</span></span>
<span data-ttu-id="df541-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="df541-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df541-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df541-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df541-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df541-140">CommonParameters</span></span>
<span data-ttu-id="df541-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df541-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df541-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df541-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df541-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df541-143">INPUTS</span></span>

### <span data-ttu-id="df541-144">System.String</span><span class="sxs-lookup"><span data-stu-id="df541-144">System.String</span></span>

### <span data-ttu-id="df541-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="df541-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="df541-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df541-146">OUTPUTS</span></span>

### <span data-ttu-id="df541-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="df541-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="df541-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="df541-148">NOTES</span></span>

## <span data-ttu-id="df541-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df541-149">RELATED LINKS</span></span>

[<span data-ttu-id="df541-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="df541-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
