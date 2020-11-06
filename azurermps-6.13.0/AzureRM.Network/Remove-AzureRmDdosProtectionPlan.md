---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 87110fe779e128e8ef5d5d6de0504ec9fdca1b25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505307"
---
# <span data-ttu-id="61729-101">Remove-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="61729-101">Remove-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="61729-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61729-102">SYNOPSIS</span></span>
<span data-ttu-id="61729-103">A DDoS védelmi csomag eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="61729-103">Removes a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61729-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61729-104">SYNTAX</span></span>

```
Remove-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61729-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="61729-105">DESCRIPTION</span></span>
<span data-ttu-id="61729-106">A Remove-AzureRmDdosProtectionPlan parancsmag eltávolítja a DDoS védelmi csomagot.</span><span class="sxs-lookup"><span data-stu-id="61729-106">The Remove-AzureRmDdosProtectionPlan cmdlet removes a DDoS protection plan.</span></span>

## <span data-ttu-id="61729-107">Példák</span><span class="sxs-lookup"><span data-stu-id="61729-107">EXAMPLES</span></span>

### <span data-ttu-id="61729-108">1. példa: üres DDoS védelmi csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="61729-108">Example 1: Remove an empty DDoS protection plan</span></span>
```
D:\> Remove-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="61729-109">Ebben az esetben eltávolítunk egy DDoS védelmi csomagot a megadott módon.</span><span class="sxs-lookup"><span data-stu-id="61729-109">In this case, we remove a DDoS protection plan as specified.</span></span>

### <span data-ttu-id="61729-110">2. példa: a virtuális hálózathoz társított DDoS védelmi csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="61729-110">Example 2: Remove a DDoS protection plan associated with a virtual network</span></span>
```
D:\> $vnet = Get-AzureRmVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = $null
D:\> $vnet.EnableDdosProtection = $false
D:\> $vnet | Set-AzureRmVirtualNetwork


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


D:\> Remove-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="61729-111">A DDoS védelmi csomagok nem törölhetők, ha virtuális hálózattal vannak társítva.</span><span class="sxs-lookup"><span data-stu-id="61729-111">DDoS protection plans cannot be deleted if they are associated with a virtual network.</span></span> <span data-ttu-id="61729-112">Az első lépés a két objektum társításának megszüntetése.</span><span class="sxs-lookup"><span data-stu-id="61729-112">So the first step is to disassociate both objects.</span></span> <span data-ttu-id="61729-113">Itt bemutatjuk a tervhez társított virtuális hálózat legújabb verzióját, és a **DdosProtectionPlan** tulajdonságot üres értékre, a jelölő **EnableDdosProtection** (ez a jelző nem lehet terv nélkül igaz).</span><span class="sxs-lookup"><span data-stu-id="61729-113">Here, we get the most updated version of the virtual network associated with the plan, and we set the property **DdosProtectionPlan** to an empty value and the flag **EnableDdosProtection** (this flag cannot be true without a plan).</span></span>
<span data-ttu-id="61729-114">Ezután a helyi változót a **set-AzureRmVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="61729-114">Then, we persist the new state by piping the local variable into **Set-AzureRmVirtualNetwork**.</span></span> <span data-ttu-id="61729-115">Jelenleg a csomag már nem társítva van a virtuális hálózattal.</span><span class="sxs-lookup"><span data-stu-id="61729-115">At this point, the plan is no longer associated with the virtual network.</span></span>
<span data-ttu-id="61729-116">Ha a tervhez a legutóbb társította, eltávolíthatja a DDoS védelmi csomagot a Remove-AzureRmDdosProtectionPlan.</span><span class="sxs-lookup"><span data-stu-id="61729-116">If this is the last one associated with the plan, we can remove the DDoS protection plan by using the command Remove-AzureRmDdosProtectionPlan.</span></span>

## <span data-ttu-id="61729-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61729-117">PARAMETERS</span></span>

### <span data-ttu-id="61729-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61729-118">-DefaultProfile</span></span>
<span data-ttu-id="61729-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="61729-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61729-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="61729-120">-Name</span></span>
<span data-ttu-id="61729-121">Az eltávolítandó DDoS védelmi csomag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61729-121">Specifies the name of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="61729-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61729-122">-PassThru</span></span>
<span data-ttu-id="61729-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="61729-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="61729-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="61729-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="61729-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61729-125">-ResourceGroupName</span></span>
<span data-ttu-id="61729-126">Az eltávolítani kívánt DDoS védelmi csomag erőforráscsoport-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="61729-126">Specifies the resource group of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="61729-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="61729-127">-Confirm</span></span>
<span data-ttu-id="61729-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="61729-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61729-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61729-129">-WhatIf</span></span>
<span data-ttu-id="61729-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="61729-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61729-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="61729-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61729-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61729-132">CommonParameters</span></span>
<span data-ttu-id="61729-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61729-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61729-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61729-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61729-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61729-135">INPUTS</span></span>

### <span data-ttu-id="61729-136">System. String</span><span class="sxs-lookup"><span data-stu-id="61729-136">System.String</span></span>

## <span data-ttu-id="61729-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61729-137">OUTPUTS</span></span>

### <span data-ttu-id="61729-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="61729-138">System.Boolean</span></span>

## <span data-ttu-id="61729-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61729-139">NOTES</span></span>

## <span data-ttu-id="61729-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61729-140">RELATED LINKS</span></span>

[<span data-ttu-id="61729-141">Új – AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="61729-141">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="61729-142">Get-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="61729-142">Get-AzureRmDdosProtectionPlan</span></span>](./Get-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="61729-143">Új – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="61729-143">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="61729-144">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="61729-144">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="61729-145">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="61729-145">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
