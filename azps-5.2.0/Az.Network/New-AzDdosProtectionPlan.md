---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
ms.openlocfilehash: 39d45085c7f53bfeec6e18f38602fca48a3cefa3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372706"
---
# <span data-ttu-id="05534-101">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="05534-101">New-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="05534-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05534-102">SYNOPSIS</span></span>
<span data-ttu-id="05534-103">DDoS védelmi tervet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="05534-103">Creates a DDoS protection plan.</span></span>

## <span data-ttu-id="05534-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="05534-104">SYNTAX</span></span>

```
New-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05534-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="05534-105">DESCRIPTION</span></span>
<span data-ttu-id="05534-106">A New-AzDdosProtectionPlan parancsmag létrehoz egy DDoS védelmi tervet.</span><span class="sxs-lookup"><span data-stu-id="05534-106">The New-AzDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="05534-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="05534-107">EXAMPLES</span></span>

### <span data-ttu-id="05534-108">1. példa: DDoS védelmi terv létrehozása és társítása új virtuális hálózathoz</span><span class="sxs-lookup"><span data-stu-id="05534-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="05534-109">Először létrehozunk egy új DDoS Védelmi tervet a **New-AzDdosProtectionPlan paranccsal.**</span><span class="sxs-lookup"><span data-stu-id="05534-109">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="05534-110">Ezután létrehozunk egy új virtuális hálózatot a **New-AzVirtualNetwork** segítségével, és az újonnan létrehozott terv azonosítóját a **DdosProtectionPlanId** paraméterben adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="05534-110">Then, we create a new virtual network with **New-AzVirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="05534-111">Ebben az esetben, mivel a virtuális hálózatot egy tervhez társítjuk, megadhatja az **EnableDdoSProtection paramétert is.**</span><span class="sxs-lookup"><span data-stu-id="05534-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="05534-112">2. példa: DDoS védelmi terv létrehozása és társítása meglévő virtuális hálózattal</span><span class="sxs-lookup"><span data-stu-id="05534-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = New-Object Microsoft.Azure.Commands.Network.Models.PSResourceId
D:\> $vnet.DdosProtectionPlan.Id = $ddosProtectionPlan.Id
D:\> $vnet.EnableDdosProtection = $true
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb"
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
                             "Etag": "W/\"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : true
DdosProtectionPlan     : {
                           "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName"
                         }
EnableVmProtection     : false
```

<span data-ttu-id="05534-113">Először létrehozunk egy új DDoS Védelmi tervet a **New-AzDdosProtectionPlan paranccsal.**</span><span class="sxs-lookup"><span data-stu-id="05534-113">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="05534-114">Másodikként a tervhez társítani kívánt virtuális hálózat legfrissebb verzióját tudjuk szerezni.</span><span class="sxs-lookup"><span data-stu-id="05534-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="05534-115">Frissítjük a **DdosProtectionPlan** tulajdonságot egy **PSResourceId** objektummal, amely az újonnan létrehozott terv azonosítójára hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="05534-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="05534-116">Ebben az esetben, ha a virtuális hálózatot DDoS védelmi tervhez társítjuk, az **EnableDdosProtection** jelzőt is beállíthatjuk igazra.</span><span class="sxs-lookup"><span data-stu-id="05534-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="05534-117">Végül az új állapotot a helyi változó **Set-AzVirtualNetwork-be** való kipipálva történő megőrzésével maradunk meg.</span><span class="sxs-lookup"><span data-stu-id="05534-117">Finally, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span>

## <span data-ttu-id="05534-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05534-118">PARAMETERS</span></span>

### <span data-ttu-id="05534-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05534-119">-AsJob</span></span>
<span data-ttu-id="05534-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="05534-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05534-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05534-121">-DefaultProfile</span></span>
<span data-ttu-id="05534-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05534-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05534-123">-Location</span><span class="sxs-lookup"><span data-stu-id="05534-123">-Location</span></span>
<span data-ttu-id="05534-124">Megadja a létrehozható DDoS védelmi terv helyét.</span><span class="sxs-lookup"><span data-stu-id="05534-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="05534-125">-Name</span><span class="sxs-lookup"><span data-stu-id="05534-125">-Name</span></span>
<span data-ttu-id="05534-126">A létrehozható DDoS védelmi terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="05534-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="05534-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05534-127">-ResourceGroupName</span></span>
<span data-ttu-id="05534-128">A létrehozható DDoS védelmi terv erőforráscsoportját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="05534-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="05534-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="05534-129">-Tag</span></span>
<span data-ttu-id="05534-130">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="05534-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05534-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05534-131">-Confirm</span></span>
<span data-ttu-id="05534-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="05534-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05534-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05534-133">-WhatIf</span></span>
<span data-ttu-id="05534-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="05534-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05534-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="05534-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05534-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05534-136">CommonParameters</span></span>
<span data-ttu-id="05534-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05534-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05534-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05534-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05534-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05534-139">INPUTS</span></span>

### <span data-ttu-id="05534-140">System.String</span><span class="sxs-lookup"><span data-stu-id="05534-140">System.String</span></span>

### <span data-ttu-id="05534-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="05534-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="05534-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05534-142">OUTPUTS</span></span>

### <span data-ttu-id="05534-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="05534-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="05534-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="05534-144">NOTES</span></span>

## <span data-ttu-id="05534-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05534-145">RELATED LINKS</span></span>

[<span data-ttu-id="05534-146">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="05534-146">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="05534-147">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="05534-147">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="05534-148">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="05534-148">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="05534-149">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="05534-149">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="05534-150">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="05534-150">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)