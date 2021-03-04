---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: 80a1c21b118bf8bcc5a613fef2cdfbe382b117a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928585"
---
# <span data-ttu-id="cf1b5-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf1b5-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="cf1b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf1b5-102">SYNOPSIS</span></span>
<span data-ttu-id="cf1b5-103">Virtuális hálózatot kap egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="cf1b5-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="cf1b5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cf1b5-104">SYNTAX</span></span>

### <span data-ttu-id="cf1b5-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="cf1b5-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf1b5-106">Kibontás</span><span class="sxs-lookup"><span data-stu-id="cf1b5-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf1b5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cf1b5-107">DESCRIPTION</span></span>
<span data-ttu-id="cf1b5-108">A **Get-AzVirtualNetwork** parancsmag egy vagy több virtuális hálózatot kap egy erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="cf1b5-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="cf1b5-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cf1b5-109">EXAMPLES</span></span>

### <span data-ttu-id="cf1b5-110">1: Virtuális hálózat lekérése</span><span class="sxs-lookup"><span data-stu-id="cf1b5-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="cf1b5-111">Ez a parancs a MyVirtualNetwork nevű virtuális hálózatot kapja meg a TestResourceGroup erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="cf1b5-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="cf1b5-112">2: Virtuális hálózatok felsorolása szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="cf1b5-112">2: List virtual networks using filter</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork*

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="cf1b5-113">Ez a parancs az összes olyan virtuális hálózatot beveszi, amelyek a "MyVirtualNetwork" kezdetűek.</span><span class="sxs-lookup"><span data-stu-id="cf1b5-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="cf1b5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf1b5-114">PARAMETERS</span></span>

### <span data-ttu-id="cf1b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf1b5-115">-DefaultProfile</span></span>
<span data-ttu-id="cf1b5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf1b5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf1b5-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="cf1b5-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf1b5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cf1b5-118">-Name</span></span>
<span data-ttu-id="cf1b5-119">Annak a virtuális hálózatnak a nevét adja meg, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="cf1b5-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="cf1b5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf1b5-120">-ResourceGroupName</span></span>
<span data-ttu-id="cf1b5-121">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a virtuális hálózat tartozik.</span><span class="sxs-lookup"><span data-stu-id="cf1b5-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="cf1b5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf1b5-122">CommonParameters</span></span>
<span data-ttu-id="cf1b5-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf1b5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf1b5-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf1b5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf1b5-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf1b5-125">INPUTS</span></span>

### <span data-ttu-id="cf1b5-126">System.String</span><span class="sxs-lookup"><span data-stu-id="cf1b5-126">System.String</span></span>

## <span data-ttu-id="cf1b5-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf1b5-127">OUTPUTS</span></span>

### <span data-ttu-id="cf1b5-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf1b5-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="cf1b5-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cf1b5-129">NOTES</span></span>

## <span data-ttu-id="cf1b5-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf1b5-130">RELATED LINKS</span></span>

[<span data-ttu-id="cf1b5-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf1b5-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="cf1b5-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf1b5-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="cf1b5-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf1b5-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


