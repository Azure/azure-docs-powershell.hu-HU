---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: d017ef97d7c8a1834a8cab2de979e017251adf7f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018161"
---
# <span data-ttu-id="7c2a7-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7c2a7-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="7c2a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c2a7-102">SYNOPSIS</span></span>
<span data-ttu-id="7c2a7-103">Egy erőforráscsoport vagy-előfizetés virtuális WAN-vagy virtuális WAN-kapcsolatát kapja.</span><span class="sxs-lookup"><span data-stu-id="7c2a7-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="7c2a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c2a7-104">SYNTAX</span></span>

### <span data-ttu-id="7c2a7-105">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7c2a7-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c2a7-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c2a7-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c2a7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c2a7-107">DESCRIPTION</span></span>
<span data-ttu-id="7c2a7-108">Egy erőforráscsoport vagy-előfizetés virtuális WAN-vagy virtuális WAN-kapcsolatát kapja.</span><span class="sxs-lookup"><span data-stu-id="7c2a7-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="7c2a7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7c2a7-109">EXAMPLES</span></span>

### <span data-ttu-id="7c2a7-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7c2a7-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : myVirtualWAN
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="7c2a7-111">Ez a parancs a virtuális WAN nevű myVirtualWAN az erőforráscsoport testRG.</span><span class="sxs-lookup"><span data-stu-id="7c2a7-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="7c2a7-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="7c2a7-112">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualWan -Name test*

Name                       : test1
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test1
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded

Name                       : test2
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test2
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="7c2a7-113">Ez a parancs a virtuális WAN-t a "teszt" kifejezéssel kezdődően kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7c2a7-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="7c2a7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c2a7-114">PARAMETERS</span></span>

### <span data-ttu-id="7c2a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c2a7-115">-DefaultProfile</span></span>
<span data-ttu-id="7c2a7-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c2a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c2a7-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7c2a7-117">-Name</span></span>
<span data-ttu-id="7c2a7-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="7c2a7-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="7c2a7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c2a7-119">-ResourceGroupName</span></span>
<span data-ttu-id="7c2a7-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7c2a7-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="7c2a7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c2a7-121">CommonParameters</span></span>
<span data-ttu-id="7c2a7-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c2a7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c2a7-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7c2a7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c2a7-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c2a7-124">INPUTS</span></span>

### <span data-ttu-id="7c2a7-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="7c2a7-125">None</span></span>

## <span data-ttu-id="7c2a7-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c2a7-126">OUTPUTS</span></span>

### <span data-ttu-id="7c2a7-127">Microsoft. Azure. commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7c2a7-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="7c2a7-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c2a7-128">NOTES</span></span>

## <span data-ttu-id="7c2a7-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c2a7-129">RELATED LINKS</span></span>

[<span data-ttu-id="7c2a7-130">Új – AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7c2a7-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="7c2a7-131">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7c2a7-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="7c2a7-132">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7c2a7-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
