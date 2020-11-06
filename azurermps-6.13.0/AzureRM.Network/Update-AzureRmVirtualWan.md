---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualWan.md
ms.openlocfilehash: 3f62cf755ac06efe9ed5f04a6657a36cfe612abe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494025"
---
# <span data-ttu-id="64f11-101">Update-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="64f11-101">Update-AzureRmVirtualWan</span></span>

## <span data-ttu-id="64f11-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64f11-102">SYNOPSIS</span></span>
<span data-ttu-id="64f11-103">Azure virtuális WAN-kapcsolat frissítése</span><span class="sxs-lookup"><span data-stu-id="64f11-103">Updates an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64f11-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64f11-104">SYNTAX</span></span>

### <span data-ttu-id="64f11-105">ByVirtualWanName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="64f11-105">ByVirtualWanName (Default)</span></span>
```
Update-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64f11-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="64f11-106">ByVirtualWanObject</span></span>
```
Update-AzureRmVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64f11-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="64f11-107">ByVirtualWanResourceId</span></span>
```
Update-AzureRmVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64f11-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="64f11-108">DESCRIPTION</span></span>
<span data-ttu-id="64f11-109">Azure virtuális WAN-kapcsolat frissítése</span><span class="sxs-lookup"><span data-stu-id="64f11-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="64f11-110">Példák</span><span class="sxs-lookup"><span data-stu-id="64f11-110">EXAMPLES</span></span>

### <span data-ttu-id="64f11-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="64f11-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="64f11-112">A fentiekben létrehoz egy erőforráscsoportot "testRG" a "Nyugat-amerikai" tartományban, és egy Azure virtuális WAN-csoportot az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="64f11-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="64f11-113">A VirtualWan új tulajdonságokkal frissülnek.</span><span class="sxs-lookup"><span data-stu-id="64f11-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="64f11-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64f11-114">PARAMETERS</span></span>

### <span data-ttu-id="64f11-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="64f11-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="64f11-116">Elágazási fiók engedélyezése a VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="64f11-116">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="64f11-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="64f11-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="64f11-118">Engedélyezze a vnet, hogy vnet a forgalmat a VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="64f11-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="64f11-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64f11-119">-AsJob</span></span>
<span data-ttu-id="64f11-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="64f11-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64f11-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f11-121">-DefaultProfile</span></span>
<span data-ttu-id="64f11-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64f11-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64f11-123">-Force</span><span class="sxs-lookup"><span data-stu-id="64f11-123">-Force</span></span>
<span data-ttu-id="64f11-124">Ne kérjen megerősítést, ha egy erőforrást szeretne átgondolni?</span><span class="sxs-lookup"><span data-stu-id="64f11-124">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="64f11-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64f11-125">-InputObject</span></span>
<span data-ttu-id="64f11-126">A módosítani kívánt virtuális WAN-objektum</span><span class="sxs-lookup"><span data-stu-id="64f11-126">The virtual wan object to be modified</span></span>

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

### <span data-ttu-id="64f11-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64f11-127">-Name</span></span>
<span data-ttu-id="64f11-128">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="64f11-128">The resource name.</span></span>

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

### <span data-ttu-id="64f11-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64f11-129">-ResourceGroupName</span></span>
<span data-ttu-id="64f11-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="64f11-130">The resource group name.</span></span>

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

### <span data-ttu-id="64f11-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64f11-131">-ResourceId</span></span>
<span data-ttu-id="64f11-132">A virtuális WAN Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="64f11-132">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="64f11-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="64f11-133">-Tag</span></span>
<span data-ttu-id="64f11-134">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="64f11-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64f11-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64f11-135">-Confirm</span></span>
<span data-ttu-id="64f11-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64f11-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64f11-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64f11-137">-WhatIf</span></span>
<span data-ttu-id="64f11-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="64f11-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64f11-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64f11-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64f11-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f11-140">CommonParameters</span></span>
<span data-ttu-id="64f11-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64f11-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f11-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64f11-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f11-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64f11-143">INPUTS</span></span>

### <span data-ttu-id="64f11-144">System. String</span><span class="sxs-lookup"><span data-stu-id="64f11-144">System.String</span></span>

### <span data-ttu-id="64f11-145">Microsoft. Azure. commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="64f11-145">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="64f11-146">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="64f11-146">System.Collections.Hashtable</span></span>

## <span data-ttu-id="64f11-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64f11-147">OUTPUTS</span></span>

### <span data-ttu-id="64f11-148">Microsoft. Azure. commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="64f11-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="64f11-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64f11-149">NOTES</span></span>

## <span data-ttu-id="64f11-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64f11-150">RELATED LINKS</span></span>
