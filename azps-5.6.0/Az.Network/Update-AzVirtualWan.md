---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: eb6611bef2499c9aaf164ddbe2e7a31c63051751
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918353"
---
# <span data-ttu-id="855b4-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="855b4-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="855b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="855b4-102">SYNOPSIS</span></span>
<span data-ttu-id="855b4-103">Frissíti az Azure Virtual WAN-t.</span><span class="sxs-lookup"><span data-stu-id="855b4-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="855b4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="855b4-104">SYNTAX</span></span>

### <span data-ttu-id="855b4-105">ByVirtualWanName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="855b4-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="855b4-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="855b4-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="855b4-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="855b4-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="855b4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="855b4-108">DESCRIPTION</span></span>
<span data-ttu-id="855b4-109">Frissíti az Azure Virtual WAN-t.</span><span class="sxs-lookup"><span data-stu-id="855b4-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="855b4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="855b4-110">EXAMPLES</span></span>

### <span data-ttu-id="855b4-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="855b4-111">Example 1</span></span>

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

<span data-ttu-id="855b4-112">A fenti "testRG" erőforráscsoportot hoz létre a "Nyugat-USA" régióban, és egy Azure Virtuális WAN-t az adott erőforráscsoportban az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="855b4-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="855b4-113">A VirtualWan új tulajdonságokkal frissül.</span><span class="sxs-lookup"><span data-stu-id="855b4-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="855b4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="855b4-114">PARAMETERS</span></span>

### <span data-ttu-id="855b4-115">-AllowBranchToBrancTraffic</span><span class="sxs-lookup"><span data-stu-id="855b4-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="855b4-116">Elágaztatás engedélyezése a VirtualWan-ban.</span><span class="sxs-lookup"><span data-stu-id="855b4-116">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="855b4-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="855b4-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="855b4-118">Vnet-adatforgalom engedélyezése VirtualWanban.</span><span class="sxs-lookup"><span data-stu-id="855b4-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="855b4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="855b4-119">-AsJob</span></span>
<span data-ttu-id="855b4-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="855b4-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="855b4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="855b4-121">-DefaultProfile</span></span>
<span data-ttu-id="855b4-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="855b4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="855b4-123">-Force</span><span class="sxs-lookup"><span data-stu-id="855b4-123">-Force</span></span>
<span data-ttu-id="855b4-124">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="855b4-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="855b4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="855b4-125">-InputObject</span></span>
<span data-ttu-id="855b4-126">A módosítható virtuális wan objektum</span><span class="sxs-lookup"><span data-stu-id="855b4-126">The virtual wan object to be modified</span></span>

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

### <span data-ttu-id="855b4-127">-Name</span><span class="sxs-lookup"><span data-stu-id="855b4-127">-Name</span></span>
<span data-ttu-id="855b4-128">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="855b4-128">The resource name.</span></span>

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

### <span data-ttu-id="855b4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="855b4-129">-ResourceGroupName</span></span>
<span data-ttu-id="855b4-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="855b4-130">The resource group name.</span></span>

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

### <span data-ttu-id="855b4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="855b4-131">-ResourceId</span></span>
<span data-ttu-id="855b4-132">A virtuális wan Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="855b4-132">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="855b4-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="855b4-133">-Tag</span></span>
<span data-ttu-id="855b4-134">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="855b4-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="855b4-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="855b4-135">-VirtualWANType</span></span>
<span data-ttu-id="855b4-136">A virtuális wan típusa.</span><span class="sxs-lookup"><span data-stu-id="855b4-136">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="855b4-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="855b4-137">-Confirm</span></span>
<span data-ttu-id="855b4-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="855b4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="855b4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="855b4-139">-WhatIf</span></span>
<span data-ttu-id="855b4-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="855b4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="855b4-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="855b4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="855b4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="855b4-142">CommonParameters</span></span>
<span data-ttu-id="855b4-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="855b4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="855b4-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="855b4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="855b4-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="855b4-145">INPUTS</span></span>

### <span data-ttu-id="855b4-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="855b4-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="855b4-147">System.String</span><span class="sxs-lookup"><span data-stu-id="855b4-147">System.String</span></span>

## <span data-ttu-id="855b4-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="855b4-148">OUTPUTS</span></span>

### <span data-ttu-id="855b4-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="855b4-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="855b4-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="855b4-150">NOTES</span></span>

## <span data-ttu-id="855b4-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="855b4-151">RELATED LINKS</span></span>

[<span data-ttu-id="855b4-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="855b4-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="855b4-153">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="855b4-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="855b4-154">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="855b4-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
