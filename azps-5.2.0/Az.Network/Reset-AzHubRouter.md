---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 039d37f9d9dd7b5af026b7ce2a87113513949b67
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351401"
---
# <span data-ttu-id="e3335-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="e3335-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="e3335-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3335-102">SYNOPSIS</span></span>
<span data-ttu-id="e3335-103">Alaphelyzetbe állítja egy VirtualHub-erőforrás RoutingState-ját.</span><span class="sxs-lookup"><span data-stu-id="e3335-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="e3335-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e3335-104">SYNTAX</span></span>

### <span data-ttu-id="e3335-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e3335-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3335-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="e3335-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3335-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="e3335-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3335-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e3335-108">DESCRIPTION</span></span>
<span data-ttu-id="e3335-109">Csak akkor állítja alaphelyzetbe egy meglévő VirtualHub-erőforrás útválasztási állapotát, ha a virtuális központ Útválasztási állapota nincs kiépítve.</span><span class="sxs-lookup"><span data-stu-id="e3335-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="e3335-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e3335-110">EXAMPLES</span></span>

### <span data-ttu-id="e3335-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e3335-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="e3335-112">Állítsa alaphelyzetbe a virtuális központ útválasztási állapotát annak ResourceGroupName és ResourceName tulajdonságával.</span><span class="sxs-lookup"><span data-stu-id="e3335-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="e3335-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e3335-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="e3335-114">Állítsa alaphelyzetbe a virtuális központ útválasztási állapotát annak ResourceId-ével.</span><span class="sxs-lookup"><span data-stu-id="e3335-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="e3335-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="e3335-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="e3335-116">Bemeneti objektum használatával állítsa alaphelyzetbe a virtuális központ útválasztási állapotát.</span><span class="sxs-lookup"><span data-stu-id="e3335-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="e3335-117">A bemeneti objektum PSVirtualHub típusú.</span><span class="sxs-lookup"><span data-stu-id="e3335-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="e3335-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="e3335-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="e3335-119">Egy meglévő virtuális központi objektum beolvasható, majd bemeneti objektumként átadott a Reset-AzHubRouternek.</span><span class="sxs-lookup"><span data-stu-id="e3335-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="e3335-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3335-120">PARAMETERS</span></span>

### <span data-ttu-id="e3335-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3335-121">-AsJob</span></span>
<span data-ttu-id="e3335-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e3335-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3335-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3335-123">-DefaultProfile</span></span>
<span data-ttu-id="e3335-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3335-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3335-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e3335-125">-Force</span></span>
<span data-ttu-id="e3335-126">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="e3335-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e3335-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3335-127">-InputObject</span></span>
<span data-ttu-id="e3335-128">A módosítva lévő virtuális központi objektum.</span><span class="sxs-lookup"><span data-stu-id="e3335-128">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="e3335-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e3335-129">-Name</span></span>
<span data-ttu-id="e3335-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e3335-130">The resource name.</span></span>

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

### <span data-ttu-id="e3335-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3335-131">-ResourceGroupName</span></span>
<span data-ttu-id="e3335-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e3335-132">The resource group name.</span></span>

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

### <span data-ttu-id="e3335-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3335-133">-ResourceId</span></span>
<span data-ttu-id="e3335-134">A módosítani szükséges virtuális központ erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e3335-134">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="e3335-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3335-135">-Confirm</span></span>
<span data-ttu-id="e3335-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e3335-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3335-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3335-137">-WhatIf</span></span>
<span data-ttu-id="e3335-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e3335-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3335-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3335-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3335-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3335-140">CommonParameters</span></span>
<span data-ttu-id="e3335-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3335-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3335-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3335-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3335-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3335-143">INPUTS</span></span>

### <span data-ttu-id="e3335-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e3335-144">System.String</span></span>

### <span data-ttu-id="e3335-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e3335-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="e3335-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3335-146">OUTPUTS</span></span>

### <span data-ttu-id="e3335-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e3335-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="e3335-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e3335-148">NOTES</span></span>

## <span data-ttu-id="e3335-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3335-149">RELATED LINKS</span></span>

[<span data-ttu-id="e3335-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e3335-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
