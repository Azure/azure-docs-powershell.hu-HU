---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: 777e03a570f3915d6e0ebe4cbb5c84f9c1824120
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184344"
---
# <span data-ttu-id="9bf0f-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9bf0f-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="9bf0f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9bf0f-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf0f-103">Virtuális hálózat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9bf0f-103">Removes a virtual network.</span></span>

## <span data-ttu-id="9bf0f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9bf0f-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bf0f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9bf0f-105">DESCRIPTION</span></span>
<span data-ttu-id="9bf0f-106">A **Remove-AzVirtualNetwork** parancsmag eltávolítja az Azure virtuális hálózatot.</span><span class="sxs-lookup"><span data-stu-id="9bf0f-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="9bf0f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9bf0f-107">EXAMPLES</span></span>

### <span data-ttu-id="9bf0f-108">1: virtuális hálózat létrehozása és törlése</span><span class="sxs-lookup"><span data-stu-id="9bf0f-108">1: Create and delete a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="9bf0f-109">Ebben a példában egy erőforráscsoport virtuális hálózata jön létre, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="9bf0f-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="9bf0f-110">Ha a virtuális hálózat törlésekor a kérdését szeretné letiltani, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="9bf0f-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="9bf0f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9bf0f-111">PARAMETERS</span></span>

### <span data-ttu-id="9bf0f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bf0f-112">-AsJob</span></span>
<span data-ttu-id="9bf0f-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9bf0f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bf0f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf0f-114">-DefaultProfile</span></span>
<span data-ttu-id="9bf0f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9bf0f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bf0f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9bf0f-116">-Force</span></span>
<span data-ttu-id="9bf0f-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="9bf0f-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9bf0f-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9bf0f-118">-Name</span></span>
<span data-ttu-id="9bf0f-119">Annak a virtuális hálózatnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="9bf0f-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9bf0f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bf0f-120">-PassThru</span></span>
<span data-ttu-id="9bf0f-121">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9bf0f-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9bf0f-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9bf0f-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9bf0f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf0f-123">-ResourceGroupName</span></span>
<span data-ttu-id="9bf0f-124">Annak a virtuális hálózatnak a neve, amely a parancsmag eltávolítását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9bf0f-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9bf0f-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9bf0f-125">-Confirm</span></span>
<span data-ttu-id="9bf0f-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9bf0f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf0f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bf0f-127">-WhatIf</span></span>
<span data-ttu-id="9bf0f-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9bf0f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bf0f-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9bf0f-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf0f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf0f-130">CommonParameters</span></span>
<span data-ttu-id="9bf0f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9bf0f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf0f-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bf0f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf0f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bf0f-133">INPUTS</span></span>

### <span data-ttu-id="9bf0f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9bf0f-134">System.String</span></span>

## <span data-ttu-id="9bf0f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bf0f-135">OUTPUTS</span></span>

### <span data-ttu-id="9bf0f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9bf0f-136">System.Boolean</span></span>

## <span data-ttu-id="9bf0f-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9bf0f-137">NOTES</span></span>

## <span data-ttu-id="9bf0f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9bf0f-138">RELATED LINKS</span></span>

[<span data-ttu-id="9bf0f-139">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9bf0f-139">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="9bf0f-140">Új – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9bf0f-140">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="9bf0f-141">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9bf0f-141">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


