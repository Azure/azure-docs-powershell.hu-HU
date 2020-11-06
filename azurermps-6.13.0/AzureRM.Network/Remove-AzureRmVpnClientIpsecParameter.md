---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: b88fff9775665f5b20f403d46f11bba89dc61220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495001"
---
# <span data-ttu-id="1fb00-101">Remove-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="1fb00-101">Remove-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="1fb00-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1fb00-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb00-103">A virtuális hálózati átjáró erőforrásban beállított virtuális magánhálózati IPSec-házirend eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="1fb00-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fb00-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1fb00-104">SYNTAX</span></span>

### <span data-ttu-id="1fb00-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1fb00-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fb00-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1fb00-106">ByFactoryObject</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fb00-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1fb00-107">ByResourceId</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fb00-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1fb00-108">DESCRIPTION</span></span>
<span data-ttu-id="1fb00-109">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="1fb00-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="1fb00-110">A **Remove-AzureRmVpnClientIpsecParameter** parancsmag eltávolítja a virtuális hálózati átjárón beállított virtuális magánhálózati IPSec-paramétereket, ami a virtuális magánhálózati IPSec-házirend beállítása a VPN-átjárón a VirtualNetworkGateway név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="1fb00-110">The **Remove-AzureRmVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="1fb00-111">Példák</span><span class="sxs-lookup"><span data-stu-id="1fb00-111">EXAMPLES</span></span>

### <span data-ttu-id="1fb00-112">1: a virtuális hálózati átjárón beállított VPN IPSec-paraméterek törlése</span><span class="sxs-lookup"><span data-stu-id="1fb00-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="1fb00-113">Törli a virtuális hálózati átjárón beállított virtuális magánhálózati IPSec-paramétereket a "myGateway" nevű erőforráscsoport nevében az "myRG" erőforráscsoport között.</span><span class="sxs-lookup"><span data-stu-id="1fb00-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="1fb00-114">Ez a parancs a bool objektum értékét jeleníti meg, ha az Eltávolítás sikeres volt vagy sikertelen volt.</span><span class="sxs-lookup"><span data-stu-id="1fb00-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="1fb00-115">Megjegyzés: Ez a funkció a virtuális hálózati átjáró alapértelmezett VPN-házirendjének beállítását fogja eredményezni.</span><span class="sxs-lookup"><span data-stu-id="1fb00-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="1fb00-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1fb00-116">PARAMETERS</span></span>

### <span data-ttu-id="1fb00-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb00-117">-DefaultProfile</span></span>
<span data-ttu-id="1fb00-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1fb00-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fb00-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fb00-119">-InputObject</span></span>
<span data-ttu-id="1fb00-120">A virtuális hálózat Gateaway objektuma</span><span class="sxs-lookup"><span data-stu-id="1fb00-120">The virtual network gateaway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb00-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb00-121">-ResourceGroupName</span></span>
<span data-ttu-id="1fb00-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="1fb00-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fb00-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fb00-123">-ResourceId</span></span>
<span data-ttu-id="1fb00-124">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="1fb00-124">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb00-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="1fb00-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="1fb00-126">A virtuális hálózat átjárójának neve.</span><span class="sxs-lookup"><span data-stu-id="1fb00-126">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fb00-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1fb00-127">-Confirm</span></span>
<span data-ttu-id="1fb00-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1fb00-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fb00-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fb00-129">-WhatIf</span></span>
<span data-ttu-id="1fb00-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1fb00-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fb00-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1fb00-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fb00-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb00-132">CommonParameters</span></span>
<span data-ttu-id="1fb00-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1fb00-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb00-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb00-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb00-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fb00-135">INPUTS</span></span>

### <span data-ttu-id="1fb00-136">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1fb00-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="1fb00-137">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1fb00-137">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="1fb00-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1fb00-138">System.String</span></span>

## <span data-ttu-id="1fb00-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fb00-139">OUTPUTS</span></span>

### <span data-ttu-id="1fb00-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1fb00-140">System.Boolean</span></span>

## <span data-ttu-id="1fb00-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1fb00-141">NOTES</span></span>

## <span data-ttu-id="1fb00-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1fb00-142">RELATED LINKS</span></span>
