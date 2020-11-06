---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 79a9f0cb2b46150c7746112553949b1bbcbaf1dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495047"
---
# <span data-ttu-id="48baa-101">New-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="48baa-101">New-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="48baa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48baa-102">SYNOPSIS</span></span>
<span data-ttu-id="48baa-103">DDoS védelmi csomagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="48baa-103">Creates a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48baa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48baa-104">SYNTAX</span></span>

```
New-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48baa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48baa-105">DESCRIPTION</span></span>
<span data-ttu-id="48baa-106">Az New-AzureRmDdosProtectionPlan parancsmag egy DDoS védelmi csomagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="48baa-106">The New-AzureRmDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="48baa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="48baa-107">EXAMPLES</span></span>

### <span data-ttu-id="48baa-108">1. példa: DDoS védelmi terv létrehozása és társítása új virtuális hálózattal</span><span class="sxs-lookup"><span data-stu-id="48baa-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzureRmVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzureRmvirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="48baa-109">Először új DDoS védelmi csomagot hozunk létre a **New-AzureRmDdosProtectionPlan** paranccsal.</span><span class="sxs-lookup"><span data-stu-id="48baa-109">First, we create a new DDoS Protection plan with the **New-AzureRmDdosProtectionPlan** command.</span></span>
<span data-ttu-id="48baa-110">Ezután új virtuális hálózatot hozunk létre a **New-AzureRmvirtualNetwork** , és az újonnan létrehozott terv azonosítóját adjuk meg a **DdosProtectionPlanId** paraméterben.</span><span class="sxs-lookup"><span data-stu-id="48baa-110">Then, we create a new virtual network with **New-AzureRmvirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="48baa-111">Ebben az esetben, mivel a virtuális hálózatot egy tervvel társítjuk, a **EnableDdoSProtection** paramétert is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="48baa-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="48baa-112">2. példa: DDoS védelmi terv létrehozása és társítása meglévő virtuális hálózattal</span><span class="sxs-lookup"><span data-stu-id="48baa-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $vnet = Get-AzureRmVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = New-Object Microsoft.Azure.Commands.Network.Models.PSResourceId
D:\> $vnet.DdosProtectionPlan.Id = $ddosProtectionPlan.Id
D:\> $vnet.EnableDdosProtection = $true
D:\> $vnet | Set-AzureRmVirtualNetwork


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

<span data-ttu-id="48baa-113">Először új DDoS védelmi csomagot hozunk létre a **New-AzureRmDdosProtectionPlan** paranccsal.</span><span class="sxs-lookup"><span data-stu-id="48baa-113">First, we create a new DDoS Protection plan with the **New-AzureRmDdosProtectionPlan** command.</span></span>
<span data-ttu-id="48baa-114">Másodszor a csomaghoz társítani kívánt virtuális hálózat legújabb verzióját fogjuk kapni.</span><span class="sxs-lookup"><span data-stu-id="48baa-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="48baa-115">Frissítjük a tulajdonság **DdosProtectionPlan** egy olyan **PSResourceId** -objektummal, amely az újonnan létrehozott csomag azonosítójának hivatkozását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="48baa-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="48baa-116">Ebben az esetben, ha a virtuális hálózatot egy DDoS védelmi csomaggal társítjuk, akkor a jelölő **EnableDdosProtection** is igaz értékre állíthatja.</span><span class="sxs-lookup"><span data-stu-id="48baa-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="48baa-117">Végül a helyi változót a **set-AzureRmVirtualNetwork-** ban tartjuk fenn.</span><span class="sxs-lookup"><span data-stu-id="48baa-117">Finally, we persist the new state by piping the local variable into **Set-AzureRmVirtualNetwork**.</span></span>

## <span data-ttu-id="48baa-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48baa-118">PARAMETERS</span></span>

### <span data-ttu-id="48baa-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48baa-119">-AsJob</span></span>
<span data-ttu-id="48baa-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="48baa-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48baa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48baa-121">-DefaultProfile</span></span>
<span data-ttu-id="48baa-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48baa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48baa-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="48baa-123">-Location</span></span>
<span data-ttu-id="48baa-124">A létrehozandó DDoS védelmi terv helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="48baa-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="48baa-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="48baa-125">-Name</span></span>
<span data-ttu-id="48baa-126">A létrehozandó DDoS védelmi terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="48baa-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="48baa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48baa-127">-ResourceGroupName</span></span>
<span data-ttu-id="48baa-128">Itt adhatja meg a létrehozandó DDoS védelmi csomag erőforrás-csoportját.</span><span class="sxs-lookup"><span data-stu-id="48baa-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="48baa-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="48baa-129">-Tag</span></span>
<span data-ttu-id="48baa-130">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="48baa-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="48baa-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="48baa-131">-Confirm</span></span>
<span data-ttu-id="48baa-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="48baa-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48baa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48baa-133">-WhatIf</span></span>
<span data-ttu-id="48baa-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="48baa-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48baa-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48baa-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48baa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48baa-136">CommonParameters</span></span>
<span data-ttu-id="48baa-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48baa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48baa-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48baa-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48baa-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48baa-139">INPUTS</span></span>

### <span data-ttu-id="48baa-140">System. String</span><span class="sxs-lookup"><span data-stu-id="48baa-140">System.String</span></span>

### <span data-ttu-id="48baa-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="48baa-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="48baa-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48baa-142">OUTPUTS</span></span>

### <span data-ttu-id="48baa-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="48baa-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="48baa-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48baa-144">NOTES</span></span>

## <span data-ttu-id="48baa-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48baa-145">RELATED LINKS</span></span>

[<span data-ttu-id="48baa-146">Get-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="48baa-146">Get-AzureRmDdosProtectionPlan</span></span>](./Get-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="48baa-147">Remove-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="48baa-147">Remove-AzureRmDdosProtectionPlan</span></span>](./Remove-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="48baa-148">Új – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48baa-148">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="48baa-149">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48baa-149">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="48baa-150">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48baa-150">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
