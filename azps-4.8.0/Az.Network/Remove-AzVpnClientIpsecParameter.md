---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: cee8d5d1ca76fbf206b4695661cc8f452052e62c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025150"
---
# <span data-ttu-id="21a68-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="21a68-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="21a68-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21a68-102">SYNOPSIS</span></span>
<span data-ttu-id="21a68-103">A virtuális hálózati átjáró erőforrásban beállított virtuális magánhálózati IPSec-házirend eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="21a68-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="21a68-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21a68-104">SYNTAX</span></span>

### <span data-ttu-id="21a68-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="21a68-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a68-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="21a68-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a68-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="21a68-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21a68-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="21a68-108">DESCRIPTION</span></span>
<span data-ttu-id="21a68-109">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="21a68-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="21a68-110">A **Remove-AzVpnClientIpsecParameter** parancsmag eltávolítja a virtuális hálózati átjárón beállított virtuális magánhálózati IPSec-paramétereket, ami a virtuális magánhálózati IPSec-házirend beállítása a VPN-átjárón a VirtualNetworkGateway név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="21a68-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="21a68-111">Példák</span><span class="sxs-lookup"><span data-stu-id="21a68-111">EXAMPLES</span></span>

### <span data-ttu-id="21a68-112">1. példa: a virtuális hálózati átjárón beállított VPN IPSec-paraméterek törlése</span><span class="sxs-lookup"><span data-stu-id="21a68-112">Example 1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```powershell
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="21a68-113">Törli a virtuális hálózati átjárón beállított virtuális magánhálózati IPSec-paramétereket a "myGateway" nevű erőforráscsoport nevében az "myRG" erőforráscsoport között.</span><span class="sxs-lookup"><span data-stu-id="21a68-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="21a68-114">Ez a parancs a bool objektum értékét jeleníti meg, ha az Eltávolítás sikeres volt vagy sikertelen volt.</span><span class="sxs-lookup"><span data-stu-id="21a68-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="21a68-115">Megjegyzés: Ez a funkció a virtuális hálózati átjáró alapértelmezett VPN-házirendjének beállítását fogja eredményezni.</span><span class="sxs-lookup"><span data-stu-id="21a68-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="21a68-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21a68-116">PARAMETERS</span></span>

### <span data-ttu-id="21a68-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a68-117">-DefaultProfile</span></span>
<span data-ttu-id="21a68-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21a68-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21a68-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21a68-119">-InputObject</span></span>
<span data-ttu-id="21a68-120">A virtuális hálózat átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="21a68-120">The virtual network gateway object</span></span>

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

### <span data-ttu-id="21a68-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21a68-121">-ResourceGroupName</span></span>
<span data-ttu-id="21a68-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="21a68-122">The resource group name.</span></span>

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

### <span data-ttu-id="21a68-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21a68-123">-ResourceId</span></span>
<span data-ttu-id="21a68-124">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="21a68-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="21a68-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="21a68-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="21a68-126">A virtuális hálózat átjárójának neve.</span><span class="sxs-lookup"><span data-stu-id="21a68-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="21a68-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="21a68-127">-Confirm</span></span>
<span data-ttu-id="21a68-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="21a68-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21a68-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21a68-129">-WhatIf</span></span>
<span data-ttu-id="21a68-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="21a68-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21a68-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21a68-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21a68-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a68-132">CommonParameters</span></span>
<span data-ttu-id="21a68-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21a68-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a68-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21a68-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a68-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21a68-135">INPUTS</span></span>

### <span data-ttu-id="21a68-136">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="21a68-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="21a68-137">System. String</span><span class="sxs-lookup"><span data-stu-id="21a68-137">System.String</span></span>

## <span data-ttu-id="21a68-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21a68-138">OUTPUTS</span></span>

### <span data-ttu-id="21a68-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="21a68-139">System.Boolean</span></span>

## <span data-ttu-id="21a68-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21a68-140">NOTES</span></span>

## <span data-ttu-id="21a68-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21a68-141">RELATED LINKS</span></span>

[<span data-ttu-id="21a68-142">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="21a68-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="21a68-143">Új – AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="21a68-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="21a68-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="21a68-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
