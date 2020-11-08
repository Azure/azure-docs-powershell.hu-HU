---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: eec1fd885dd193ae69fd119a127634e2cfa19a51
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013968"
---
# <span data-ttu-id="dfe72-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dfe72-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="dfe72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dfe72-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe72-103">Virtuális hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="dfe72-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="dfe72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dfe72-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfe72-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dfe72-105">DESCRIPTION</span></span>
<span data-ttu-id="dfe72-106">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="dfe72-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="dfe72-107">A **Get-AzVirtualNetworkGateway** parancsmag az Azure-átjáró objektumát adja eredményül a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="dfe72-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="dfe72-108">Példák</span><span class="sxs-lookup"><span data-stu-id="dfe72-108">EXAMPLES</span></span>

### <span data-ttu-id="dfe72-109">1: virtuális hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="dfe72-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="dfe72-110">Törli a virtuális hálózati átjáró objektumát a "myGateway" nevű erőforrás-csoport "myRG" Megjegyzés: először törölnie kell a virtuális hálózati átjáróval való összes kapcsolatot a **Remove-AzVirtualNetworkGatewayConnection** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="dfe72-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="dfe72-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dfe72-111">PARAMETERS</span></span>

### <span data-ttu-id="dfe72-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfe72-112">-AsJob</span></span>
<span data-ttu-id="dfe72-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="dfe72-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dfe72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe72-114">-DefaultProfile</span></span>
<span data-ttu-id="dfe72-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dfe72-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfe72-116">-Force</span><span class="sxs-lookup"><span data-stu-id="dfe72-116">-Force</span></span>
<span data-ttu-id="dfe72-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="dfe72-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dfe72-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dfe72-118">-Name</span></span>
<span data-ttu-id="dfe72-119">Annak a virtuális hálózati átjárónak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="dfe72-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dfe72-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dfe72-120">-PassThru</span></span>
<span data-ttu-id="dfe72-121">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="dfe72-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dfe72-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="dfe72-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dfe72-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe72-123">-ResourceGroupName</span></span>
<span data-ttu-id="dfe72-124">A virtuális hálózati átjárót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dfe72-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="dfe72-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dfe72-125">-Confirm</span></span>
<span data-ttu-id="dfe72-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dfe72-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfe72-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfe72-127">-WhatIf</span></span>
<span data-ttu-id="dfe72-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dfe72-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfe72-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dfe72-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfe72-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe72-130">CommonParameters</span></span>
<span data-ttu-id="dfe72-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dfe72-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe72-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfe72-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe72-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfe72-133">INPUTS</span></span>

### <span data-ttu-id="dfe72-134">System. String</span><span class="sxs-lookup"><span data-stu-id="dfe72-134">System.String</span></span>

## <span data-ttu-id="dfe72-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfe72-135">OUTPUTS</span></span>

### <span data-ttu-id="dfe72-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dfe72-136">System.Boolean</span></span>

## <span data-ttu-id="dfe72-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dfe72-137">NOTES</span></span>

## <span data-ttu-id="dfe72-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfe72-138">RELATED LINKS</span></span>

[<span data-ttu-id="dfe72-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dfe72-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="dfe72-140">Új – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dfe72-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="dfe72-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dfe72-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="dfe72-142">Átméretezés-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dfe72-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="dfe72-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dfe72-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
