---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 3a598001421bf237f93a63fb4f45d069bf9404ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006006"
---
# <span data-ttu-id="2915a-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2915a-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2915a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2915a-102">SYNOPSIS</span></span>
<span data-ttu-id="2915a-103">Virtuális hálózati átjáró kapcsolatának törlése</span><span class="sxs-lookup"><span data-stu-id="2915a-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="2915a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2915a-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2915a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2915a-105">DESCRIPTION</span></span>
<span data-ttu-id="2915a-106">A virtuális hálózati átjáró kapcsolata az Az Azure virtuális hálózati átjáróhoz csatlakoztatott IPsec-csatornát (Site-to-Site vagy Vnet-to-Vnet) képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="2915a-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="2915a-107">A **Remove-AzVirtualNetworkGatewayConnection** parancsmag a név és az erőforráscsoport neve alapján törli a kapcsolat objektumát.</span><span class="sxs-lookup"><span data-stu-id="2915a-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="2915a-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2915a-108">EXAMPLES</span></span>

### <span data-ttu-id="2915a-109">1. példa: Virtuális hálózati átjáró kapcsolatának törlése</span><span class="sxs-lookup"><span data-stu-id="2915a-109">Example 1: Delete a Virtual Network Gateway Connection</span></span>
```powershell
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="2915a-110">Törli a virtuális hálózati átjáró kapcsolatának "myTunnel" nevű objektumát a "myRG" erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="2915a-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="2915a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2915a-111">PARAMETERS</span></span>

### <span data-ttu-id="2915a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2915a-112">-DefaultProfile</span></span>
<span data-ttu-id="2915a-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2915a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2915a-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2915a-114">-Force</span></span>
<span data-ttu-id="2915a-115">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="2915a-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2915a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2915a-116">-Name</span></span>
<span data-ttu-id="2915a-117">Annak a virtuális hálózati átjárónak a nevét adja meg, amelyről a parancsmag eltávolítja a kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="2915a-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2915a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2915a-118">-PassThru</span></span>
<span data-ttu-id="2915a-119">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="2915a-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2915a-120">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2915a-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2915a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2915a-121">-ResourceGroupName</span></span>
<span data-ttu-id="2915a-122">Annak az erőforráscsoportnak a nevét adja meg, amely a virtuális hálózati átjáró kapcsolatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2915a-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="2915a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2915a-123">-Confirm</span></span>
<span data-ttu-id="2915a-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2915a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2915a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2915a-125">-WhatIf</span></span>
<span data-ttu-id="2915a-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2915a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2915a-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2915a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2915a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2915a-128">CommonParameters</span></span>
<span data-ttu-id="2915a-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2915a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2915a-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2915a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2915a-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2915a-131">INPUTS</span></span>

### <span data-ttu-id="2915a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2915a-132">System.String</span></span>

## <span data-ttu-id="2915a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2915a-133">OUTPUTS</span></span>

### <span data-ttu-id="2915a-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2915a-134">System.Boolean</span></span>

## <span data-ttu-id="2915a-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2915a-135">NOTES</span></span>

## <span data-ttu-id="2915a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2915a-136">RELATED LINKS</span></span>

[<span data-ttu-id="2915a-137">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2915a-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2915a-138">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2915a-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2915a-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2915a-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
