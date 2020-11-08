---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 78ba1323532faa825e80e456f5ae6544eef3c7de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013966"
---
# <span data-ttu-id="f1646-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f1646-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f1646-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1646-102">SYNOPSIS</span></span>
<span data-ttu-id="f1646-103">Virtuális hálózati átjáró-kapcsolat törlése</span><span class="sxs-lookup"><span data-stu-id="f1646-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="f1646-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1646-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1646-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1646-105">DESCRIPTION</span></span>
<span data-ttu-id="f1646-106">A virtuális hálózati átjáró kapcsolat az Azure-alapú virtuális hálózati átjáróhoz kapcsolt IPsec-alagutat (webhelytől vagy vnet-vnet) jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="f1646-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f1646-107">A **Remove-AzVirtualNetworkGatewayConnection** parancsmag törli a kapcsolat objektumát a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="f1646-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="f1646-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f1646-108">EXAMPLES</span></span>

### <span data-ttu-id="f1646-109">1: virtuális hálózati átjáró-kapcsolat törlése</span><span class="sxs-lookup"><span data-stu-id="f1646-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="f1646-110">Törli a virtuális hálózati átjáró kapcsolat objektumát a "myTunnel" nevű erőforráscsoporthoz a "myRG" erőforráscsoport alatt.</span><span class="sxs-lookup"><span data-stu-id="f1646-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="f1646-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1646-111">PARAMETERS</span></span>

### <span data-ttu-id="f1646-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1646-112">-DefaultProfile</span></span>
<span data-ttu-id="f1646-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1646-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1646-114">-Force</span><span class="sxs-lookup"><span data-stu-id="f1646-114">-Force</span></span>
<span data-ttu-id="f1646-115">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="f1646-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f1646-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f1646-116">-Name</span></span>
<span data-ttu-id="f1646-117">Annak a virtuális hálózati átjáró-kapcsolatnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="f1646-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f1646-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1646-118">-PassThru</span></span>
<span data-ttu-id="f1646-119">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f1646-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f1646-120">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="f1646-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f1646-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1646-121">-ResourceGroupName</span></span>
<span data-ttu-id="f1646-122">A virtuális hálózati átjáró kapcsolatot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1646-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="f1646-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f1646-123">-Confirm</span></span>
<span data-ttu-id="f1646-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f1646-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1646-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1646-125">-WhatIf</span></span>
<span data-ttu-id="f1646-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f1646-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1646-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1646-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1646-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1646-128">CommonParameters</span></span>
<span data-ttu-id="f1646-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1646-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1646-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1646-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1646-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1646-131">INPUTS</span></span>

### <span data-ttu-id="f1646-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f1646-132">System.String</span></span>

## <span data-ttu-id="f1646-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1646-133">OUTPUTS</span></span>

### <span data-ttu-id="f1646-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1646-134">System.Boolean</span></span>

## <span data-ttu-id="f1646-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1646-135">NOTES</span></span>

## <span data-ttu-id="f1646-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1646-136">RELATED LINKS</span></span>

[<span data-ttu-id="f1646-137">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f1646-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f1646-138">Új – AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f1646-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f1646-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f1646-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
