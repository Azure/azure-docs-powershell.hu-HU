---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: 3a1d30f3ae44b0e6893682cf0c1d700207682803
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669923"
---
# <span data-ttu-id="d4cdf-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d4cdf-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="d4cdf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4cdf-102">SYNOPSIS</span></span>
<span data-ttu-id="d4cdf-103">Azure virtuális WAN-kapcsolat frissítése</span><span class="sxs-lookup"><span data-stu-id="d4cdf-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="d4cdf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4cdf-104">SYNTAX</span></span>

### <span data-ttu-id="d4cdf-105">ByVirtualWanName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4cdf-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4cdf-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="d4cdf-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4cdf-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="d4cdf-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4cdf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4cdf-108">DESCRIPTION</span></span>
<span data-ttu-id="d4cdf-109">Azure virtuális WAN-kapcsolat frissítése</span><span class="sxs-lookup"><span data-stu-id="d4cdf-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="d4cdf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d4cdf-110">EXAMPLES</span></span>

### <span data-ttu-id="d4cdf-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d4cdf-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="d4cdf-112">A fentiekben létrehoz egy erőforráscsoportot "testRG" a "Nyugat-amerikai" tartományban, és egy Azure virtuális WAN-csoportot az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="d4cdf-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="d4cdf-113">A VirtualWan új tulajdonságokkal frissülnek.</span><span class="sxs-lookup"><span data-stu-id="d4cdf-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="d4cdf-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4cdf-114">PARAMETERS</span></span>

### <span data-ttu-id="d4cdf-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="d4cdf-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="d4cdf-116">Elágazási fiók engedélyezése a VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="d4cdf-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4cdf-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="d4cdf-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="d4cdf-118">Engedélyezze a vnet, hogy vnet a forgalmat a VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="d4cdf-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4cdf-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4cdf-119">-AsJob</span></span>
<span data-ttu-id="d4cdf-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d4cdf-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4cdf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4cdf-121">-DefaultProfile</span></span>
<span data-ttu-id="d4cdf-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4cdf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4cdf-123">-Force</span><span class="sxs-lookup"><span data-stu-id="d4cdf-123">-Force</span></span>
<span data-ttu-id="d4cdf-124">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="d4cdf-124">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="d4cdf-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4cdf-125">-InputObject</span></span>
<span data-ttu-id="d4cdf-126">A módosítani kívánt virtuális WAN-objektum</span><span class="sxs-lookup"><span data-stu-id="d4cdf-126">The virtual wan object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4cdf-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d4cdf-127">-Name</span></span>
<span data-ttu-id="d4cdf-128">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d4cdf-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4cdf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4cdf-129">-ResourceGroupName</span></span>
<span data-ttu-id="d4cdf-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d4cdf-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4cdf-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4cdf-131">-ResourceId</span></span>
<span data-ttu-id="d4cdf-132">A virtuális WAN Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="d4cdf-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4cdf-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="d4cdf-133">-Tag</span></span>
<span data-ttu-id="d4cdf-134">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d4cdf-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4cdf-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d4cdf-135">-Confirm</span></span>
<span data-ttu-id="d4cdf-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d4cdf-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4cdf-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4cdf-137">-WhatIf</span></span>
<span data-ttu-id="d4cdf-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d4cdf-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4cdf-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4cdf-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4cdf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4cdf-140">CommonParameters</span></span>
<span data-ttu-id="d4cdf-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4cdf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4cdf-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4cdf-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4cdf-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4cdf-143">INPUTS</span></span>

### <span data-ttu-id="d4cdf-144">Microsoft. Azure. commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d4cdf-144">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="d4cdf-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d4cdf-145">System.String</span></span>

## <span data-ttu-id="d4cdf-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4cdf-146">OUTPUTS</span></span>

### <span data-ttu-id="d4cdf-147">Microsoft. Azure. commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d4cdf-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="d4cdf-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4cdf-148">NOTES</span></span>

## <span data-ttu-id="d4cdf-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4cdf-149">RELATED LINKS</span></span>

[<span data-ttu-id="d4cdf-150">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d4cdf-150">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="d4cdf-151">Új – AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d4cdf-151">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="d4cdf-152">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d4cdf-152">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
