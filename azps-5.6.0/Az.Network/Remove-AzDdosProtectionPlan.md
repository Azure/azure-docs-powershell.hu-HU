---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
ms.openlocfilehash: 8aad20fc16d160ba024dd3d4a9b6f14b65ad951e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930938"
---
# <span data-ttu-id="894c5-101">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="894c5-101">Remove-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="894c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="894c5-102">SYNOPSIS</span></span>
<span data-ttu-id="894c5-103">Eltávolít egy DDoS védelmi tervet.</span><span class="sxs-lookup"><span data-stu-id="894c5-103">Removes a DDoS protection plan.</span></span>

## <span data-ttu-id="894c5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="894c5-104">SYNTAX</span></span>

```
Remove-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="894c5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="894c5-105">DESCRIPTION</span></span>
<span data-ttu-id="894c5-106">A Remove-AzDdosProtectionPlan eltávolítja a DDoS védelmi tervet.</span><span class="sxs-lookup"><span data-stu-id="894c5-106">The Remove-AzDdosProtectionPlan cmdlet removes a DDoS protection plan.</span></span>

## <span data-ttu-id="894c5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="894c5-107">EXAMPLES</span></span>

### <span data-ttu-id="894c5-108">1. példa: Üres DDoS védelmi terv eltávolítása</span><span class="sxs-lookup"><span data-stu-id="894c5-108">Example 1: Remove an empty DDoS protection plan</span></span>
```
D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="894c5-109">Ebben az esetben eltávolítjuk a DDoS védelmi tervét a megadottak szerint.</span><span class="sxs-lookup"><span data-stu-id="894c5-109">In this case, we remove a DDoS protection plan as specified.</span></span>

### <span data-ttu-id="894c5-110">2. példa: Virtuális hálózathoz társított DDoS védelmi terv eltávolítása</span><span class="sxs-lookup"><span data-stu-id="894c5-110">Example 2: Remove a DDoS protection plan associated with a virtual network</span></span>
```
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = $null
D:\> $vnet.EnableDdosProtection = $false
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"65947351-747e-4686-aa8b-c40da58f6c8b"
ResourceGuid           : fcb7bc1e-ee0d-4005-b3f1-feda76e3756c
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "10.0.0.0/16"
                           ]
                         }
DhcpOptions            : {
                           "DnsServers": [
                             "8.8.8.8"
                           ]
                         }
Subnets                : [
                           {
                             "Name": "SubnetName",
                             "Etag": "W/\"65947351-747e-4686-aa8b-c40da58f6c8b\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
EnableVmProtection     : false


D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="894c5-111">A DDoS védelmi tervek nem törölhetők, ha virtuális hálózathoz vannak társítva.</span><span class="sxs-lookup"><span data-stu-id="894c5-111">DDoS protection plans cannot be deleted if they are associated with a virtual network.</span></span> <span data-ttu-id="894c5-112">Ezért az első lépés a két objektum társításának szétszedése.</span><span class="sxs-lookup"><span data-stu-id="894c5-112">So the first step is to disassociate both objects.</span></span> <span data-ttu-id="894c5-113">Itt a tervhez társított virtuális hálózat legújabb verzióját tudjuk kapni, a **DdosProtectionPlan** tulajdonságot pedig egy üres értékre, az EnableDdosProtection jelölőt pedig az **EnableDdosProtection** jelölőre (ez a jelölő terv nélkül nem lehet igaz).</span><span class="sxs-lookup"><span data-stu-id="894c5-113">Here, we get the most updated version of the virtual network associated with the plan, and we set the property **DdosProtectionPlan** to an empty value and the flag **EnableDdosProtection** (this flag cannot be true without a plan).</span></span>
<span data-ttu-id="894c5-114">Ezután az új állapotot a helyi változó **Set-AzVirtualNetwork** környezetbe való áttűnésének hatékonnyá történő áttűnésének megőrz használatával.</span><span class="sxs-lookup"><span data-stu-id="894c5-114">Then, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span> <span data-ttu-id="894c5-115">Ezen a ponton a terv már nincs társítva a virtuális hálózathoz.</span><span class="sxs-lookup"><span data-stu-id="894c5-115">At this point, the plan is no longer associated with the virtual network.</span></span>
<span data-ttu-id="894c5-116">Ha ez az utolsó társított terv, eltávolíthatja a DDoS védelmi tervet az Remove-AzDdosProtectionPlan paranccsal.</span><span class="sxs-lookup"><span data-stu-id="894c5-116">If this is the last one associated with the plan, we can remove the DDoS protection plan by using the command Remove-AzDdosProtectionPlan.</span></span>

## <span data-ttu-id="894c5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="894c5-117">PARAMETERS</span></span>

### <span data-ttu-id="894c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="894c5-118">-DefaultProfile</span></span>
<span data-ttu-id="894c5-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="894c5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="894c5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="894c5-120">-Name</span></span>
<span data-ttu-id="894c5-121">Az eltávolítható DDoS védelmi terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="894c5-121">Specifies the name of the DDoS protection plan to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="894c5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="894c5-122">-PassThru</span></span>
<span data-ttu-id="894c5-123">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="894c5-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="894c5-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="894c5-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="894c5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="894c5-125">-ResourceGroupName</span></span>
<span data-ttu-id="894c5-126">A DDoS védelmi terv eltávolítható erőforráscsoportját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="894c5-126">Specifies the resource group of the DDoS protection plan to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="894c5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="894c5-127">-Confirm</span></span>
<span data-ttu-id="894c5-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="894c5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="894c5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="894c5-129">-WhatIf</span></span>
<span data-ttu-id="894c5-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="894c5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="894c5-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="894c5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="894c5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="894c5-132">CommonParameters</span></span>
<span data-ttu-id="894c5-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="894c5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="894c5-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="894c5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="894c5-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="894c5-135">INPUTS</span></span>

### <span data-ttu-id="894c5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="894c5-136">System.String</span></span>

## <span data-ttu-id="894c5-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="894c5-137">OUTPUTS</span></span>

### <span data-ttu-id="894c5-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="894c5-138">System.Boolean</span></span>

## <span data-ttu-id="894c5-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="894c5-139">NOTES</span></span>

## <span data-ttu-id="894c5-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="894c5-140">RELATED LINKS</span></span>

[<span data-ttu-id="894c5-141">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="894c5-141">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="894c5-142">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="894c5-142">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="894c5-143">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="894c5-143">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="894c5-144">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="894c5-144">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="894c5-145">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="894c5-145">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)