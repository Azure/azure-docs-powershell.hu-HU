---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: e93bcc320f14a8311a29c6be9824da16506ea499
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303043"
---
# <span data-ttu-id="a5cf5-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a5cf5-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="a5cf5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="a5cf5-103">Azure virtuális WAN-kapcsolat frissítése</span><span class="sxs-lookup"><span data-stu-id="a5cf5-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="a5cf5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5cf5-104">SYNTAX</span></span>

### <span data-ttu-id="a5cf5-105">ByVirtualWanName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5cf5-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5cf5-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="a5cf5-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5cf5-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="a5cf5-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5cf5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5cf5-108">DESCRIPTION</span></span>
<span data-ttu-id="a5cf5-109">Azure virtuális WAN-kapcsolat frissítése</span><span class="sxs-lookup"><span data-stu-id="a5cf5-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="a5cf5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a5cf5-110">EXAMPLES</span></span>

### <span data-ttu-id="a5cf5-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a5cf5-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="a5cf5-112">A fentiekben létrehoz egy erőforráscsoportot "testRG" a "Nyugat-amerikai" tartományban, és egy Azure virtuális WAN-csoportot az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="a5cf5-113">A VirtualWan új tulajdonságokkal frissülnek.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="a5cf5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5cf5-114">PARAMETERS</span></span>

### <span data-ttu-id="a5cf5-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="a5cf5-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="a5cf5-116">Elágazási fiók engedélyezése a VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5cf5-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="a5cf5-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="a5cf5-118">Engedélyezze a vnet, hogy vnet a forgalmat a VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5cf5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5cf5-119">-AsJob</span></span>
<span data-ttu-id="a5cf5-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a5cf5-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5cf5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5cf5-121">-DefaultProfile</span></span>
<span data-ttu-id="a5cf5-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5cf5-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a5cf5-123">-Force</span></span>
<span data-ttu-id="a5cf5-124">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5cf5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5cf5-125">-InputObject</span></span>
<span data-ttu-id="a5cf5-126">A módosítani kívánt virtuális WAN-objektum</span><span class="sxs-lookup"><span data-stu-id="a5cf5-126">The virtual wan object to be modified</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5cf5-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a5cf5-127">-Name</span></span>
<span data-ttu-id="a5cf5-128">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-128">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5cf5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5cf5-129">-ResourceGroupName</span></span>
<span data-ttu-id="a5cf5-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5cf5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5cf5-131">-ResourceId</span></span>
<span data-ttu-id="a5cf5-132">A virtuális WAN Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5cf5-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="a5cf5-133">-Tag</span></span>
<span data-ttu-id="a5cf5-134">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5cf5-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="a5cf5-135">-VirtualWANType</span></span>
<span data-ttu-id="a5cf5-136">A virtuális WAN típusa.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-136">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5cf5-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5cf5-137">-Confirm</span></span>
<span data-ttu-id="a5cf5-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5cf5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5cf5-139">-WhatIf</span></span>
<span data-ttu-id="a5cf5-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5cf5-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5cf5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5cf5-142">CommonParameters</span></span>
<span data-ttu-id="a5cf5-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5cf5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5cf5-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a5cf5-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5cf5-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5cf5-145">INPUTS</span></span>

### <span data-ttu-id="a5cf5-146">Microsoft. Azure. commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a5cf5-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="a5cf5-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a5cf5-147">System.String</span></span>

## <span data-ttu-id="a5cf5-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5cf5-148">OUTPUTS</span></span>

### <span data-ttu-id="a5cf5-149">Microsoft. Azure. commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a5cf5-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="a5cf5-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5cf5-150">NOTES</span></span>

## <span data-ttu-id="a5cf5-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5cf5-151">RELATED LINKS</span></span>

[<span data-ttu-id="a5cf5-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a5cf5-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="a5cf5-153">Új – AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a5cf5-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="a5cf5-154">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="a5cf5-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
