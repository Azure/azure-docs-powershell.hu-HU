---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: bfe1c586d85a44460b1adbb84942be9b556973dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194532"
---
# <span data-ttu-id="9a908-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="9a908-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="9a908-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a908-102">SYNOPSIS</span></span>
<span data-ttu-id="9a908-103">A virtuális hálózat eltávolítása koppintással.</span><span class="sxs-lookup"><span data-stu-id="9a908-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="9a908-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a908-104">SYNTAX</span></span>

### <span data-ttu-id="9a908-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9a908-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a908-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a908-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a908-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a908-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a908-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a908-108">DESCRIPTION</span></span>
<span data-ttu-id="9a908-109">A **Remove-AzVirtualNetworkTap** parancsmag eltávolítja az Azure Virtual networkt.</span><span class="sxs-lookup"><span data-stu-id="9a908-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="9a908-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9a908-110">EXAMPLES</span></span>

### <span data-ttu-id="9a908-111">Példa 1: virtuális hálózat eltávolítása koppintással</span><span class="sxs-lookup"><span data-stu-id="9a908-111">Example 1: Remove a virtual network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="9a908-112">Ez a parancs eltávolítja a VirtualNetworkTap1 az erőforráscsoport ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="9a908-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="9a908-113">Mivel az *erő* paraméter nem használható, a rendszer kérni fogja a felhasználót, hogy erősítse meg ezt a lépést.</span><span class="sxs-lookup"><span data-stu-id="9a908-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="9a908-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a908-114">PARAMETERS</span></span>

### <span data-ttu-id="9a908-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a908-115">-AsJob</span></span>
<span data-ttu-id="9a908-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9a908-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a908-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a908-117">-DefaultProfile</span></span>
<span data-ttu-id="9a908-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a908-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a908-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9a908-119">-Force</span></span>
<span data-ttu-id="9a908-120">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="9a908-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="9a908-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a908-121">-InputObject</span></span>
<span data-ttu-id="9a908-122">Hivatkozás a VirtualNetworkTap erőforrásra</span><span class="sxs-lookup"><span data-stu-id="9a908-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a908-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9a908-123">-Name</span></span>
<span data-ttu-id="9a908-124">A koppintás neve.</span><span class="sxs-lookup"><span data-stu-id="9a908-124">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a908-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a908-125">-PassThru</span></span>
<span data-ttu-id="9a908-126">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9a908-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9a908-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9a908-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9a908-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a908-128">-ResourceGroupName</span></span>
<span data-ttu-id="9a908-129">A virtuális hálózat erőforráscsoport neve koppintással.</span><span class="sxs-lookup"><span data-stu-id="9a908-129">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a908-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a908-130">-ResourceId</span></span>
<span data-ttu-id="9a908-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="9a908-131">VirtualNetworkTap resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a908-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9a908-132">-Confirm</span></span>
<span data-ttu-id="9a908-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9a908-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a908-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a908-134">-WhatIf</span></span>
<span data-ttu-id="9a908-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9a908-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a908-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a908-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a908-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a908-137">CommonParameters</span></span>
<span data-ttu-id="9a908-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a908-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a908-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a908-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a908-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a908-140">INPUTS</span></span>

### <span data-ttu-id="9a908-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9a908-141">System.String</span></span>

### <span data-ttu-id="9a908-142">Microsoft. Azure. commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="9a908-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="9a908-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a908-143">OUTPUTS</span></span>

### <span data-ttu-id="9a908-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a908-144">System.Boolean</span></span>

## <span data-ttu-id="9a908-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a908-145">NOTES</span></span>

## <span data-ttu-id="9a908-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a908-146">RELATED LINKS</span></span>

[<span data-ttu-id="9a908-147">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="9a908-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="9a908-148">Új – AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="9a908-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="9a908-149">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="9a908-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)