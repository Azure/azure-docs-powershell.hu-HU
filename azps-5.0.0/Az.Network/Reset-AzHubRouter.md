---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 039d37f9d9dd7b5af026b7ce2a87113513949b67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194528"
---
# <span data-ttu-id="0312e-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="0312e-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="0312e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0312e-102">SYNOPSIS</span></span>
<span data-ttu-id="0312e-103">Visszaállítja egy VirtualHub-erőforrás RoutingState.</span><span class="sxs-lookup"><span data-stu-id="0312e-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="0312e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0312e-104">SYNTAX</span></span>

### <span data-ttu-id="0312e-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0312e-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0312e-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="0312e-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0312e-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="0312e-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0312e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0312e-108">DESCRIPTION</span></span>
<span data-ttu-id="0312e-109">Egy meglévő VirtualHub-erőforrás útválasztási állapotának visszaállítása csak akkor, ha a virtuális hub útválasztási állapota nincs kiépítve.</span><span class="sxs-lookup"><span data-stu-id="0312e-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="0312e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0312e-110">EXAMPLES</span></span>

### <span data-ttu-id="0312e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0312e-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="0312e-112">Állítsa alaphelyzetbe a virtuális hub útválasztási állapotát a ResourceGroupName és a ResourceName segítségével.</span><span class="sxs-lookup"><span data-stu-id="0312e-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="0312e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="0312e-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="0312e-114">Állítsa alaphelyzetbe a virtuális hub útválasztási állapotát a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="0312e-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="0312e-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="0312e-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="0312e-116">A virtuális hub útválasztási állapotának visszaállítása beviteli objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="0312e-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="0312e-117">A beviteli objektum PSVirtualHub típusú.</span><span class="sxs-lookup"><span data-stu-id="0312e-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="0312e-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="0312e-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="0312e-119">A meglévő virtuális hub-objektumok beolvashatók, majd a AzHubRouter alaphelyzetbe kerülnek a beviteli objektumként.</span><span class="sxs-lookup"><span data-stu-id="0312e-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="0312e-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0312e-120">PARAMETERS</span></span>

### <span data-ttu-id="0312e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0312e-121">-AsJob</span></span>
<span data-ttu-id="0312e-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0312e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0312e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0312e-123">-DefaultProfile</span></span>
<span data-ttu-id="0312e-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0312e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0312e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="0312e-125">-Force</span></span>
<span data-ttu-id="0312e-126">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0312e-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0312e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0312e-127">-InputObject</span></span>
<span data-ttu-id="0312e-128">A módosítani kívánt virtuális hub-objektum.</span><span class="sxs-lookup"><span data-stu-id="0312e-128">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="0312e-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0312e-129">-Name</span></span>
<span data-ttu-id="0312e-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0312e-130">The resource name.</span></span>

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

### <span data-ttu-id="0312e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0312e-131">-ResourceGroupName</span></span>
<span data-ttu-id="0312e-132">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0312e-132">The resource group name.</span></span>

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

### <span data-ttu-id="0312e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0312e-133">-ResourceId</span></span>
<span data-ttu-id="0312e-134">A módosítani kívánt virtuális hub erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0312e-134">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="0312e-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0312e-135">-Confirm</span></span>
<span data-ttu-id="0312e-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0312e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0312e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0312e-137">-WhatIf</span></span>
<span data-ttu-id="0312e-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0312e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0312e-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0312e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0312e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0312e-140">CommonParameters</span></span>
<span data-ttu-id="0312e-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0312e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0312e-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0312e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0312e-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0312e-143">INPUTS</span></span>

### <span data-ttu-id="0312e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0312e-144">System.String</span></span>

### <span data-ttu-id="0312e-145">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0312e-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="0312e-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0312e-146">OUTPUTS</span></span>

### <span data-ttu-id="0312e-147">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0312e-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="0312e-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0312e-148">NOTES</span></span>

## <span data-ttu-id="0312e-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0312e-149">RELATED LINKS</span></span>

[<span data-ttu-id="0312e-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0312e-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)