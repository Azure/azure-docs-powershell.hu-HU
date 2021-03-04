---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 3bb2a2d7c8e53cc7ba336234e3c5b24ad58e2faa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941065"
---
# <span data-ttu-id="c2fd8-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c2fd8-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="c2fd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2fd8-102">SYNOPSIS</span></span>
<span data-ttu-id="c2fd8-103">Létrehoz egy Azure Virtual WAN-t.</span><span class="sxs-lookup"><span data-stu-id="c2fd8-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="c2fd8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c2fd8-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2fd8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c2fd8-105">DESCRIPTION</span></span>
<span data-ttu-id="c2fd8-106">Létrehoz egy új Azure VirtualWAN-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="c2fd8-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="c2fd8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c2fd8-107">EXAMPLES</span></span>

### <span data-ttu-id="c2fd8-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="c2fd8-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="c2fd8-109">A fenti "testRG" erőforráscsoportot hoz létre a "Nyugat-Egyesült Államok" régióban, valamint egy Azure Virtuális WAN-t, amely ágat hoz létre az adott erőforráscsoportban az Azure-ban engedélyezett elágaztatási forgalomhoz.</span><span class="sxs-lookup"><span data-stu-id="c2fd8-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="c2fd8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2fd8-110">PARAMETERS</span></span>

### <span data-ttu-id="c2fd8-111">-AllowBranchToBrancTraffic</span><span class="sxs-lookup"><span data-stu-id="c2fd8-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="c2fd8-112">Elágaztatás engedélyezése a VirtualWan-ban.</span><span class="sxs-lookup"><span data-stu-id="c2fd8-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="c2fd8-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="c2fd8-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="c2fd8-114">Vnet-adatforgalom engedélyezése VirtualWanban.</span><span class="sxs-lookup"><span data-stu-id="c2fd8-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="c2fd8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2fd8-115">-AsJob</span></span>
<span data-ttu-id="c2fd8-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c2fd8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2fd8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2fd8-117">-DefaultProfile</span></span>
<span data-ttu-id="c2fd8-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2fd8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2fd8-119">-Location</span><span class="sxs-lookup"><span data-stu-id="c2fd8-119">-Location</span></span>
<span data-ttu-id="c2fd8-120">A VirtualWAN erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="c2fd8-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2fd8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c2fd8-121">-Name</span></span>
<span data-ttu-id="c2fd8-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c2fd8-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2fd8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2fd8-123">-ResourceGroupName</span></span>
<span data-ttu-id="c2fd8-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c2fd8-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2fd8-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2fd8-125">-Tag</span></span>
<span data-ttu-id="c2fd8-126">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="c2fd8-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c2fd8-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="c2fd8-127">-VirtualWANType</span></span>
<span data-ttu-id="c2fd8-128">A virtuális wan típusa.</span><span class="sxs-lookup"><span data-stu-id="c2fd8-128">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="c2fd8-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2fd8-129">-Confirm</span></span>
<span data-ttu-id="c2fd8-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c2fd8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2fd8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2fd8-131">-WhatIf</span></span>
<span data-ttu-id="c2fd8-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c2fd8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2fd8-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c2fd8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2fd8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2fd8-134">CommonParameters</span></span>
<span data-ttu-id="c2fd8-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2fd8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2fd8-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2fd8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2fd8-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2fd8-137">INPUTS</span></span>

### <span data-ttu-id="c2fd8-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="c2fd8-138">None</span></span>

## <span data-ttu-id="c2fd8-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2fd8-139">OUTPUTS</span></span>

### <span data-ttu-id="c2fd8-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c2fd8-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="c2fd8-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c2fd8-141">NOTES</span></span>

## <span data-ttu-id="c2fd8-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2fd8-142">RELATED LINKS</span></span>

[<span data-ttu-id="c2fd8-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c2fd8-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="c2fd8-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c2fd8-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="c2fd8-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c2fd8-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
