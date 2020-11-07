---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: 7815755d9ec5fffe973e0ecb044409f945ee5faa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837825"
---
# <span data-ttu-id="9d64b-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9d64b-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="9d64b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d64b-102">SYNOPSIS</span></span>
<span data-ttu-id="9d64b-103">Virtuális hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="9d64b-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="9d64b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d64b-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d64b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d64b-105">DESCRIPTION</span></span>
<span data-ttu-id="9d64b-106">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9d64b-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="9d64b-107">A **Get-AzVirtualNetworkGateway** parancsmag az Azure-átjáró objektumát adja eredményül a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="9d64b-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="9d64b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9d64b-108">EXAMPLES</span></span>

### <span data-ttu-id="9d64b-109">1: virtuális hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="9d64b-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="9d64b-110">Törli a virtuális hálózati átjáró objektumát a "myGateway" nevű erőforrás-csoport "myRG" Megjegyzés: először törölnie kell a virtuális hálózati átjáróval való összes kapcsolatot a **Remove-AzVirtualNetworkGatewayConnection** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="9d64b-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="9d64b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d64b-111">PARAMETERS</span></span>

### <span data-ttu-id="9d64b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d64b-112">-AsJob</span></span>
<span data-ttu-id="9d64b-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9d64b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d64b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d64b-114">-DefaultProfile</span></span>
<span data-ttu-id="9d64b-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d64b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d64b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9d64b-116">-Force</span></span>
<span data-ttu-id="9d64b-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="9d64b-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9d64b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9d64b-118">-Name</span></span>
<span data-ttu-id="9d64b-119">Annak a virtuális hálózati átjárónak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="9d64b-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9d64b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d64b-120">-PassThru</span></span>
<span data-ttu-id="9d64b-121">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9d64b-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9d64b-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9d64b-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9d64b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d64b-123">-ResourceGroupName</span></span>
<span data-ttu-id="9d64b-124">A virtuális hálózati átjárót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d64b-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="9d64b-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9d64b-125">-Confirm</span></span>
<span data-ttu-id="9d64b-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9d64b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d64b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d64b-127">-WhatIf</span></span>
<span data-ttu-id="9d64b-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9d64b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d64b-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9d64b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d64b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d64b-130">CommonParameters</span></span>
<span data-ttu-id="9d64b-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d64b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d64b-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d64b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d64b-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d64b-133">INPUTS</span></span>

### <span data-ttu-id="9d64b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9d64b-134">System.String</span></span>

## <span data-ttu-id="9d64b-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d64b-135">OUTPUTS</span></span>

### <span data-ttu-id="9d64b-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9d64b-136">System.Boolean</span></span>

## <span data-ttu-id="9d64b-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d64b-137">NOTES</span></span>

## <span data-ttu-id="9d64b-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d64b-138">RELATED LINKS</span></span>

[<span data-ttu-id="9d64b-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9d64b-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9d64b-140">Új – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9d64b-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9d64b-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9d64b-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9d64b-142">Átméretezés-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9d64b-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9d64b-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9d64b-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
