---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 3f09656caaccb103afa096ca0995489b3768e40e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837851"
---
# <span data-ttu-id="f83e5-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f83e5-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="f83e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f83e5-102">SYNOPSIS</span></span>
<span data-ttu-id="f83e5-103">Helyi hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="f83e5-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="f83e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f83e5-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f83e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f83e5-105">DESCRIPTION</span></span>
<span data-ttu-id="f83e5-106">A helyi hálózat átjárója a helyszíni VPN-eszközt jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="f83e5-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="f83e5-107">A **Remove-AzLocalNetworkGateway** parancsmag a helyszíni átjáró név és erőforrás csoport neve alapján történő törlésére szolgáló objektumot törli.</span><span class="sxs-lookup"><span data-stu-id="f83e5-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="f83e5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f83e5-108">EXAMPLES</span></span>

### <span data-ttu-id="f83e5-109">1: helyi hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="f83e5-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="f83e5-110">Törli a helyi hálózati átjáró objektumát a "myLocalGW" nevű erőforrás-csoport "myRG" Megjegyzés: először törölnie kell a helyi hálózati átjáróval való összes kapcsolatot a **Remove-AzVirtualNetworkGatewayConnection** parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="f83e5-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="f83e5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f83e5-111">PARAMETERS</span></span>

### <span data-ttu-id="f83e5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f83e5-112">-AsJob</span></span>
<span data-ttu-id="f83e5-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f83e5-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f83e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f83e5-114">-DefaultProfile</span></span>
<span data-ttu-id="f83e5-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f83e5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f83e5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f83e5-116">-Force</span></span>
<span data-ttu-id="f83e5-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="f83e5-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f83e5-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f83e5-118">-Name</span></span>
<span data-ttu-id="f83e5-119">A parancsmag által eltávolított helyi hálózati átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f83e5-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f83e5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f83e5-120">-PassThru</span></span>
<span data-ttu-id="f83e5-121">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f83e5-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f83e5-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="f83e5-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f83e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f83e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="f83e5-124">A helyi hálózati átjárót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f83e5-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="f83e5-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f83e5-125">-Confirm</span></span>
<span data-ttu-id="f83e5-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f83e5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f83e5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f83e5-127">-WhatIf</span></span>
<span data-ttu-id="f83e5-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f83e5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f83e5-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f83e5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f83e5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f83e5-130">CommonParameters</span></span>
<span data-ttu-id="f83e5-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f83e5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f83e5-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f83e5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f83e5-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f83e5-133">INPUTS</span></span>

### <span data-ttu-id="f83e5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f83e5-134">System.String</span></span>

## <span data-ttu-id="f83e5-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f83e5-135">OUTPUTS</span></span>

### <span data-ttu-id="f83e5-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f83e5-136">System.Boolean</span></span>

## <span data-ttu-id="f83e5-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f83e5-137">NOTES</span></span>

## <span data-ttu-id="f83e5-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f83e5-138">RELATED LINKS</span></span>

[<span data-ttu-id="f83e5-139">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f83e5-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="f83e5-140">Új – AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f83e5-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="f83e5-141">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f83e5-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
