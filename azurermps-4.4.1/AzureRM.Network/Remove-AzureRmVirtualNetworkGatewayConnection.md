---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d2068273c6f46c058ad7586083f6bfa0db037cab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494824"
---
# <span data-ttu-id="367b8-101">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="367b8-101">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="367b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="367b8-102">SYNOPSIS</span></span>
<span data-ttu-id="367b8-103">Virtuális hálózati átjáró-kapcsolat törlése</span><span class="sxs-lookup"><span data-stu-id="367b8-103">Deletes a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="367b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="367b8-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="367b8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="367b8-105">DESCRIPTION</span></span>
<span data-ttu-id="367b8-106">A virtuális hálózati átjáró kapcsolat az Azure-alapú virtuális hálózati átjáróhoz kapcsolt IPsec-alagutat (webhelytől vagy vnet-vnet) jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="367b8-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="367b8-107">A **Remove-AzureRmVirtualNetworkGatewayConnection** parancsmag törli a kapcsolat objektumát a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="367b8-107">The **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="367b8-108">Példák</span><span class="sxs-lookup"><span data-stu-id="367b8-108">EXAMPLES</span></span>

### <span data-ttu-id="367b8-109">1: virtuális hálózati átjáró-kapcsolat törlése</span><span class="sxs-lookup"><span data-stu-id="367b8-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="367b8-110">Törli a virtuális hálózati átjáró kapcsolat objektumát a "myTunnel" nevű erőforráscsoporthoz a "myRG" erőforráscsoport alatt.</span><span class="sxs-lookup"><span data-stu-id="367b8-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="367b8-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="367b8-111">PARAMETERS</span></span>

### <span data-ttu-id="367b8-112">-Force</span><span class="sxs-lookup"><span data-stu-id="367b8-112">-Force</span></span>
<span data-ttu-id="367b8-113">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="367b8-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="367b8-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="367b8-114">-Name</span></span>
<span data-ttu-id="367b8-115">Annak a virtuális hálózati átjáró-kapcsolatnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="367b8-115">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="367b8-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="367b8-116">-PassThru</span></span>
<span data-ttu-id="367b8-117">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="367b8-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="367b8-118">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="367b8-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="367b8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="367b8-119">-ResourceGroupName</span></span>
<span data-ttu-id="367b8-120">A virtuális hálózati átjáró kapcsolatot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="367b8-120">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="367b8-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="367b8-121">-Confirm</span></span>
<span data-ttu-id="367b8-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="367b8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="367b8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="367b8-123">-WhatIf</span></span>
<span data-ttu-id="367b8-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="367b8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="367b8-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="367b8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="367b8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="367b8-126">-DefaultProfile</span></span>
<span data-ttu-id="367b8-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="367b8-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="367b8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367b8-128">CommonParameters</span></span>
<span data-ttu-id="367b8-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="367b8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367b8-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="367b8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367b8-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="367b8-131">INPUTS</span></span>

## <span data-ttu-id="367b8-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="367b8-132">OUTPUTS</span></span>

## <span data-ttu-id="367b8-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="367b8-133">NOTES</span></span>

## <span data-ttu-id="367b8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="367b8-134">RELATED LINKS</span></span>

[<span data-ttu-id="367b8-135">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="367b8-135">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="367b8-136">Új – AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="367b8-136">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="367b8-137">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="367b8-137">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)


