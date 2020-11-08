---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 9969ee8009e1a0cd3cf5e071f01bd03035455bde
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180500"
---
# <span data-ttu-id="20d5c-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="20d5c-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="20d5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="20d5c-103">Azure virtuális WAN-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="20d5c-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="20d5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20d5c-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20d5c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="20d5c-105">DESCRIPTION</span></span>
<span data-ttu-id="20d5c-106">Új Azure VirtualWAN-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="20d5c-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="20d5c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="20d5c-107">EXAMPLES</span></span>

### <span data-ttu-id="20d5c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="20d5c-108">Example 1</span></span>

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

<span data-ttu-id="20d5c-109">A fenti létrehoz egy erőforráscsoportot "testRG" a "Nyugat-amerikai" tartományban, és egy Azure virtuális WAN-kapcsolattal, amelyben az adott erőforráscsoport engedélyezve van az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="20d5c-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="20d5c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20d5c-110">PARAMETERS</span></span>

### <span data-ttu-id="20d5c-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="20d5c-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="20d5c-112">Elágazási fiók engedélyezése a VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="20d5c-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="20d5c-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="20d5c-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="20d5c-114">Engedélyezze a vnet, hogy vnet a forgalmat a VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="20d5c-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="20d5c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20d5c-115">-AsJob</span></span>
<span data-ttu-id="20d5c-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="20d5c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20d5c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d5c-117">-DefaultProfile</span></span>
<span data-ttu-id="20d5c-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20d5c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20d5c-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="20d5c-119">-Location</span></span>
<span data-ttu-id="20d5c-120">A VirtualWAN-erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="20d5c-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="20d5c-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="20d5c-121">-Name</span></span>
<span data-ttu-id="20d5c-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="20d5c-122">The resource name.</span></span>

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

### <span data-ttu-id="20d5c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20d5c-123">-ResourceGroupName</span></span>
<span data-ttu-id="20d5c-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="20d5c-124">The resource group name.</span></span>

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

### <span data-ttu-id="20d5c-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="20d5c-125">-Tag</span></span>
<span data-ttu-id="20d5c-126">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="20d5c-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="20d5c-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="20d5c-127">-VirtualWANType</span></span>
<span data-ttu-id="20d5c-128">A virtuális WAN típusa.</span><span class="sxs-lookup"><span data-stu-id="20d5c-128">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="20d5c-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="20d5c-129">-Confirm</span></span>
<span data-ttu-id="20d5c-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="20d5c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20d5c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20d5c-131">-WhatIf</span></span>
<span data-ttu-id="20d5c-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="20d5c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20d5c-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="20d5c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20d5c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d5c-134">CommonParameters</span></span>
<span data-ttu-id="20d5c-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20d5c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d5c-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="20d5c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d5c-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20d5c-137">INPUTS</span></span>

### <span data-ttu-id="20d5c-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="20d5c-138">None</span></span>

## <span data-ttu-id="20d5c-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20d5c-139">OUTPUTS</span></span>

### <span data-ttu-id="20d5c-140">Microsoft. Azure. commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="20d5c-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="20d5c-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20d5c-141">NOTES</span></span>

## <span data-ttu-id="20d5c-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20d5c-142">RELATED LINKS</span></span>

[<span data-ttu-id="20d5c-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="20d5c-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="20d5c-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="20d5c-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="20d5c-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="20d5c-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
