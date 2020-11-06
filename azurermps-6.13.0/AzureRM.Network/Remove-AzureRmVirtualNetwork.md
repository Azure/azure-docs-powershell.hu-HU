---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
ms.openlocfilehash: b27ad6bfc08f6c6d9304cc78f888870a8a2dbad4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503499"
---
# <span data-ttu-id="b99e0-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b99e0-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="b99e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b99e0-102">SYNOPSIS</span></span>
<span data-ttu-id="b99e0-103">Virtuális hálózat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b99e0-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b99e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b99e0-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b99e0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b99e0-105">DESCRIPTION</span></span>
<span data-ttu-id="b99e0-106">A **Remove-AzureRmVirtualNetwork** parancsmag eltávolítja az Azure virtuális hálózatot.</span><span class="sxs-lookup"><span data-stu-id="b99e0-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="b99e0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b99e0-107">EXAMPLES</span></span>

### <span data-ttu-id="b99e0-108">1: virtuális hálózat létrehozása és törlése</span><span class="sxs-lookup"><span data-stu-id="b99e0-108">1: Create and delete a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="b99e0-109">Ebben a példában egy erőforráscsoport virtuális hálózata jön létre, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="b99e0-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="b99e0-110">Ha a virtuális hálózat törlésekor a kérdését szeretné letiltani, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="b99e0-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="b99e0-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b99e0-111">PARAMETERS</span></span>

### <span data-ttu-id="b99e0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b99e0-112">-AsJob</span></span>
<span data-ttu-id="b99e0-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b99e0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b99e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b99e0-114">-DefaultProfile</span></span>
<span data-ttu-id="b99e0-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b99e0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b99e0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b99e0-116">-Force</span></span>
<span data-ttu-id="b99e0-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="b99e0-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b99e0-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b99e0-118">-Name</span></span>
<span data-ttu-id="b99e0-119">Annak a virtuális hálózatnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="b99e0-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b99e0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b99e0-120">-PassThru</span></span>
<span data-ttu-id="b99e0-121">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="b99e0-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b99e0-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b99e0-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b99e0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b99e0-123">-ResourceGroupName</span></span>
<span data-ttu-id="b99e0-124">Annak a virtuális hálózatnak a neve, amely a parancsmag eltávolítását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b99e0-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b99e0-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b99e0-125">-Confirm</span></span>
<span data-ttu-id="b99e0-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b99e0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b99e0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b99e0-127">-WhatIf</span></span>
<span data-ttu-id="b99e0-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b99e0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b99e0-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b99e0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b99e0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b99e0-130">CommonParameters</span></span>
<span data-ttu-id="b99e0-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b99e0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b99e0-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b99e0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b99e0-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b99e0-133">INPUTS</span></span>

### <span data-ttu-id="b99e0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b99e0-134">System.String</span></span>

## <span data-ttu-id="b99e0-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b99e0-135">OUTPUTS</span></span>

### <span data-ttu-id="b99e0-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b99e0-136">System.Boolean</span></span>

## <span data-ttu-id="b99e0-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b99e0-137">NOTES</span></span>

## <span data-ttu-id="b99e0-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b99e0-138">RELATED LINKS</span></span>

[<span data-ttu-id="b99e0-139">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b99e0-139">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="b99e0-140">Új – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b99e0-140">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="b99e0-141">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b99e0-141">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


