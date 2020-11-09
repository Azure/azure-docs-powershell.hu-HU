---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 9969ee8009e1a0cd3cf5e071f01bd03035455bde
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301430"
---
# <span data-ttu-id="499b1-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="499b1-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="499b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="499b1-102">SYNOPSIS</span></span>
<span data-ttu-id="499b1-103">Azure virtuális WAN-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="499b1-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="499b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="499b1-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="499b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="499b1-105">DESCRIPTION</span></span>
<span data-ttu-id="499b1-106">Új Azure VirtualWAN-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="499b1-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="499b1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="499b1-107">EXAMPLES</span></span>

### <span data-ttu-id="499b1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="499b1-108">Example 1</span></span>

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

<span data-ttu-id="499b1-109">A fenti létrehoz egy erőforráscsoportot "testRG" a "Nyugat-amerikai" tartományban, és egy Azure virtuális WAN-kapcsolattal, amelyben az adott erőforráscsoport engedélyezve van az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="499b1-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="499b1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="499b1-110">PARAMETERS</span></span>

### <span data-ttu-id="499b1-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="499b1-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="499b1-112">Elágazási fiók engedélyezése a VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="499b1-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="499b1-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="499b1-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="499b1-114">Engedélyezze a vnet, hogy vnet a forgalmat a VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="499b1-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="499b1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="499b1-115">-AsJob</span></span>
<span data-ttu-id="499b1-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="499b1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="499b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="499b1-117">-DefaultProfile</span></span>
<span data-ttu-id="499b1-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="499b1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="499b1-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="499b1-119">-Location</span></span>
<span data-ttu-id="499b1-120">A VirtualWAN-erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="499b1-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="499b1-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="499b1-121">-Name</span></span>
<span data-ttu-id="499b1-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="499b1-122">The resource name.</span></span>

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

### <span data-ttu-id="499b1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="499b1-123">-ResourceGroupName</span></span>
<span data-ttu-id="499b1-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="499b1-124">The resource group name.</span></span>

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

### <span data-ttu-id="499b1-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="499b1-125">-Tag</span></span>
<span data-ttu-id="499b1-126">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="499b1-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="499b1-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="499b1-127">-VirtualWANType</span></span>
<span data-ttu-id="499b1-128">A virtuális WAN típusa.</span><span class="sxs-lookup"><span data-stu-id="499b1-128">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="499b1-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="499b1-129">-Confirm</span></span>
<span data-ttu-id="499b1-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="499b1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="499b1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="499b1-131">-WhatIf</span></span>
<span data-ttu-id="499b1-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="499b1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="499b1-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="499b1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="499b1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="499b1-134">CommonParameters</span></span>
<span data-ttu-id="499b1-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="499b1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="499b1-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="499b1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="499b1-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="499b1-137">INPUTS</span></span>

### <span data-ttu-id="499b1-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="499b1-138">None</span></span>

## <span data-ttu-id="499b1-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="499b1-139">OUTPUTS</span></span>

### <span data-ttu-id="499b1-140">Microsoft. Azure. commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="499b1-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="499b1-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="499b1-141">NOTES</span></span>

## <span data-ttu-id="499b1-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="499b1-142">RELATED LINKS</span></span>

[<span data-ttu-id="499b1-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="499b1-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="499b1-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="499b1-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="499b1-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="499b1-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
