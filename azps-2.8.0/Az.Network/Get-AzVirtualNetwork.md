---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: da0dde546d5875c1a29bd02805f40c7f12a68188
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837547"
---
# <span data-ttu-id="44cce-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="44cce-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="44cce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="44cce-102">SYNOPSIS</span></span>
<span data-ttu-id="44cce-103">Virtuális hálózat beolvasása egy erőforráscsoport számára</span><span class="sxs-lookup"><span data-stu-id="44cce-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="44cce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="44cce-104">SYNTAX</span></span>

### <span data-ttu-id="44cce-105">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="44cce-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="44cce-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="44cce-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44cce-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="44cce-107">DESCRIPTION</span></span>
<span data-ttu-id="44cce-108">A **Get-AzVirtualNetwork** parancsmag egy vagy több virtuális hálózattal rendelkezik, és egy erőforráscsoport lesz.</span><span class="sxs-lookup"><span data-stu-id="44cce-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="44cce-109">Példák</span><span class="sxs-lookup"><span data-stu-id="44cce-109">EXAMPLES</span></span>

### <span data-ttu-id="44cce-110">1: virtuális hálózat beolvasása</span><span class="sxs-lookup"><span data-stu-id="44cce-110">1: Retrieve a virtual network</span></span>
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

<span data-ttu-id="44cce-111">Ez a parancs a MyVirtualNetwork nevű virtuális hálózatot kapja az erőforráscsoport TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="44cce-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="44cce-112">2: lista virtuális hálózatai szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="44cce-112">2: List virtual networks using filter</span></span>
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

<span data-ttu-id="44cce-113">Ez a parancs a "MyVirtualNetwork" kezdetű virtuális hálózatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="44cce-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="44cce-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="44cce-114">PARAMETERS</span></span>

### <span data-ttu-id="44cce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44cce-115">-DefaultProfile</span></span>
<span data-ttu-id="44cce-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44cce-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44cce-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="44cce-117">-ExpandResource</span></span>
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

### <span data-ttu-id="44cce-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="44cce-118">-Name</span></span>
<span data-ttu-id="44cce-119">Annak a virtuális hálózatnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="44cce-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="44cce-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44cce-120">-ResourceGroupName</span></span>
<span data-ttu-id="44cce-121">Annak a csoportnak a neve, amelyhez a virtuális hálózat tartozik.</span><span class="sxs-lookup"><span data-stu-id="44cce-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="44cce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44cce-122">CommonParameters</span></span>
<span data-ttu-id="44cce-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="44cce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44cce-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="44cce-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44cce-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="44cce-125">INPUTS</span></span>

### <span data-ttu-id="44cce-126">System. String</span><span class="sxs-lookup"><span data-stu-id="44cce-126">System.String</span></span>

## <span data-ttu-id="44cce-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44cce-127">OUTPUTS</span></span>

### <span data-ttu-id="44cce-128">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="44cce-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="44cce-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="44cce-129">NOTES</span></span>

## <span data-ttu-id="44cce-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44cce-130">RELATED LINKS</span></span>

[<span data-ttu-id="44cce-131">Új – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="44cce-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="44cce-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="44cce-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="44cce-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="44cce-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


