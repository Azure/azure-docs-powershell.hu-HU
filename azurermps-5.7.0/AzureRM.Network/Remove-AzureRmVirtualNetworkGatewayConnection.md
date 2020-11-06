---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 73bb12aebbe4f67c1aba4526f6ed656e5b6feb09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503068"
---
# <span data-ttu-id="4e906-101">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4e906-101">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="4e906-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e906-102">SYNOPSIS</span></span>
<span data-ttu-id="4e906-103">Virtuális hálózati átjáró-kapcsolat törlése</span><span class="sxs-lookup"><span data-stu-id="4e906-103">Deletes a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e906-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e906-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e906-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e906-105">DESCRIPTION</span></span>
<span data-ttu-id="4e906-106">A virtuális hálózati átjáró kapcsolat az Azure-alapú virtuális hálózati átjáróhoz kapcsolt IPsec-alagutat (webhelytől vagy vnet-vnet) jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="4e906-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="4e906-107">A **Remove-AzureRmVirtualNetworkGatewayConnection** parancsmag törli a kapcsolat objektumát a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="4e906-107">The **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="4e906-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4e906-108">EXAMPLES</span></span>

### <span data-ttu-id="4e906-109">1: virtuális hálózati átjáró-kapcsolat törlése</span><span class="sxs-lookup"><span data-stu-id="4e906-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="4e906-110">Törli a virtuális hálózati átjáró kapcsolat objektumát a "myTunnel" nevű erőforráscsoporthoz a "myRG" erőforráscsoport alatt.</span><span class="sxs-lookup"><span data-stu-id="4e906-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="4e906-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e906-111">PARAMETERS</span></span>

### <span data-ttu-id="4e906-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e906-112">-DefaultProfile</span></span>
<span data-ttu-id="4e906-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e906-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e906-114">-Force</span><span class="sxs-lookup"><span data-stu-id="4e906-114">-Force</span></span>
<span data-ttu-id="4e906-115">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="4e906-115">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e906-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e906-116">-Name</span></span>
<span data-ttu-id="4e906-117">Annak a virtuális hálózati átjáró-kapcsolatnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="4e906-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e906-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e906-118">-PassThru</span></span>
<span data-ttu-id="4e906-119">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="4e906-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4e906-120">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4e906-120">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e906-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e906-121">-ResourceGroupName</span></span>
<span data-ttu-id="4e906-122">A virtuális hálózati átjáró kapcsolatot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e906-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e906-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4e906-123">-Confirm</span></span>
<span data-ttu-id="4e906-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4e906-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e906-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e906-125">-WhatIf</span></span>
<span data-ttu-id="4e906-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4e906-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e906-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e906-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e906-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e906-128">CommonParameters</span></span>
<span data-ttu-id="4e906-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e906-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e906-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e906-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e906-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e906-131">INPUTS</span></span>

### <span data-ttu-id="4e906-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="4e906-132">None</span></span>
<span data-ttu-id="4e906-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="4e906-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e906-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e906-134">OUTPUTS</span></span>

## <span data-ttu-id="4e906-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e906-135">NOTES</span></span>

## <span data-ttu-id="4e906-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e906-136">RELATED LINKS</span></span>

[<span data-ttu-id="4e906-137">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4e906-137">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="4e906-138">Új – AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4e906-138">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="4e906-139">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4e906-139">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)

