---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 17ace5a209a34fc65d79efaac0bfb477e00b2472
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670252"
---
# <span data-ttu-id="b5fff-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b5fff-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="b5fff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5fff-102">SYNOPSIS</span></span>
<span data-ttu-id="b5fff-103">Azure virtuális WAN-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b5fff-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="b5fff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5fff-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5fff-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5fff-105">DESCRIPTION</span></span>
<span data-ttu-id="b5fff-106">Új Azure VirtualWAN-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="b5fff-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="b5fff-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b5fff-107">EXAMPLES</span></span>

### <span data-ttu-id="b5fff-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b5fff-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="b5fff-109">A fenti létrehoz egy erőforráscsoportot "testRG" a "Nyugat-amerikai" tartományban, és egy Azure virtuális WAN-kapcsolattal, amelyben az adott erőforráscsoport engedélyezve van az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="b5fff-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="b5fff-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5fff-110">PARAMETERS</span></span>

### <span data-ttu-id="b5fff-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="b5fff-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="b5fff-112">Elágazási fiók engedélyezése a VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="b5fff-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="b5fff-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="b5fff-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="b5fff-114">Engedélyezze a vnet, hogy vnet a forgalmat a VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="b5fff-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="b5fff-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5fff-115">-AsJob</span></span>
<span data-ttu-id="b5fff-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b5fff-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5fff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5fff-117">-DefaultProfile</span></span>
<span data-ttu-id="b5fff-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5fff-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5fff-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="b5fff-119">-Location</span></span>
<span data-ttu-id="b5fff-120">A VirtualWAN-erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="b5fff-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fff-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b5fff-121">-Name</span></span>
<span data-ttu-id="b5fff-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b5fff-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5fff-123">-ResourceGroupName</span></span>
<span data-ttu-id="b5fff-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b5fff-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fff-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="b5fff-125">-Tag</span></span>
<span data-ttu-id="b5fff-126">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="b5fff-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b5fff-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b5fff-127">-Confirm</span></span>
<span data-ttu-id="b5fff-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b5fff-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5fff-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5fff-129">-WhatIf</span></span>
<span data-ttu-id="b5fff-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b5fff-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5fff-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5fff-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5fff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5fff-132">CommonParameters</span></span>
<span data-ttu-id="b5fff-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5fff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5fff-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5fff-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5fff-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5fff-135">INPUTS</span></span>

### <span data-ttu-id="b5fff-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="b5fff-136">None</span></span>

## <span data-ttu-id="b5fff-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5fff-137">OUTPUTS</span></span>

### <span data-ttu-id="b5fff-138">Microsoft. Azure. commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b5fff-138">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="b5fff-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5fff-139">NOTES</span></span>

## <span data-ttu-id="b5fff-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5fff-140">RELATED LINKS</span></span>

[<span data-ttu-id="b5fff-141">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b5fff-141">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="b5fff-142">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b5fff-142">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="b5fff-143">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b5fff-143">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
