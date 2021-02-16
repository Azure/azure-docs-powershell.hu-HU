---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: d017ef97d7c8a1834a8cab2de979e017251adf7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151811"
---
# <span data-ttu-id="e1156-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e1156-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="e1156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1156-102">SYNOPSIS</span></span>
<span data-ttu-id="e1156-103">Virtuális WAN-t vagy minden virtuális WAN-t kap egy erőforráscsoportban vagy -előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="e1156-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="e1156-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e1156-104">SYNTAX</span></span>

### <span data-ttu-id="e1156-105">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1156-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1156-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1156-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1156-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e1156-107">DESCRIPTION</span></span>
<span data-ttu-id="e1156-108">Virtuális WAN-t vagy minden virtuális WAN-t kap egy erőforráscsoportban vagy -előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="e1156-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="e1156-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e1156-109">EXAMPLES</span></span>

### <span data-ttu-id="e1156-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="e1156-110">Example 1</span></span>

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

<span data-ttu-id="e1156-111">Ez a parancs a MyVirtualWAN nevű virtuális WAN-t kapja meg az erőforráscsoport tesztRG-ében.</span><span class="sxs-lookup"><span data-stu-id="e1156-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="e1156-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="e1156-112">Example 2</span></span>

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

<span data-ttu-id="e1156-113">Ez a parancs az összes virtuális WAN-t a "teszt" szótól kezdve kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e1156-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="e1156-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1156-114">PARAMETERS</span></span>

### <span data-ttu-id="e1156-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1156-115">-DefaultProfile</span></span>
<span data-ttu-id="e1156-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1156-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1156-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e1156-117">-Name</span></span>
<span data-ttu-id="e1156-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e1156-118">The resource name.</span></span>

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

### <span data-ttu-id="e1156-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1156-119">-ResourceGroupName</span></span>
<span data-ttu-id="e1156-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e1156-120">The resource group name.</span></span>

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

### <span data-ttu-id="e1156-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1156-121">CommonParameters</span></span>
<span data-ttu-id="e1156-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1156-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1156-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1156-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1156-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1156-124">INPUTS</span></span>

### <span data-ttu-id="e1156-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="e1156-125">None</span></span>

## <span data-ttu-id="e1156-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1156-126">OUTPUTS</span></span>

### <span data-ttu-id="e1156-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e1156-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="e1156-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e1156-128">NOTES</span></span>

## <span data-ttu-id="e1156-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1156-129">RELATED LINKS</span></span>

[<span data-ttu-id="e1156-130">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e1156-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="e1156-131">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e1156-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="e1156-132">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e1156-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
