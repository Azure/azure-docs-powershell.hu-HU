---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 248e932bfc2c9148122ecad924ae10b3e480fd3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838301"
---
# <span data-ttu-id="ee792-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="ee792-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="ee792-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee792-102">SYNOPSIS</span></span>
<span data-ttu-id="ee792-103">A meglévő virtuális hálózati átjáró VPN-IPSec-paramétereinek beállítása.</span><span class="sxs-lookup"><span data-stu-id="ee792-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="ee792-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee792-104">SYNTAX</span></span>

### <span data-ttu-id="ee792-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee792-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee792-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ee792-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee792-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ee792-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee792-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee792-108">DESCRIPTION</span></span>
<span data-ttu-id="ee792-109">A **set-AzVpnClientIpsecParameter** parancsmag a meglévő virtuális hálózati átjáró VPN-IPSec-paramétereit állítja be.</span><span class="sxs-lookup"><span data-stu-id="ee792-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="ee792-110">A virtuális hálózati átjáró létrehozásakor a rendszer az alapértelmezett VPN-házirendeket az átjárón állítja be.</span><span class="sxs-lookup"><span data-stu-id="ee792-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="ee792-111">Abban az esetben, ha a webhely felhasználója szeretné használni bizonyos egyéni IPSec-házirendeket a VPN-átjáróhoz való csatlakozáshoz, először állítsa be az IPSec-házirendet a VPN-átjáróra.</span><span class="sxs-lookup"><span data-stu-id="ee792-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="ee792-112">A **set-AzVpnClientIpsecParameter** biztosítja ezt a módot.</span><span class="sxs-lookup"><span data-stu-id="ee792-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="ee792-113">Példák</span><span class="sxs-lookup"><span data-stu-id="ee792-113">EXAMPLES</span></span>

### <span data-ttu-id="ee792-114">1. példa: egyéni VPN-házirendet állít be a meglévő virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ee792-114">Example 1 : Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="ee792-115">Ebben a példában az egyéni virtuális magánhálózati IPSec-házirendet az ContosoResourceGroup nevű erőforráscsoport ContosoVirtualGateway nevű meglévő virtuális hálózati átjáróhoz állítja be.</span><span class="sxs-lookup"><span data-stu-id="ee792-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="ee792-116">New-AzVpnClientIpsecParameter parancsmag segítségével létrehozhatja a virtuális magánhálózati IPSec-paramétereket tartalmazó objektumot az átadott egy vagy minden paraméter értékével, amelyet a felhasználó bármely meglévő virtuális hálózati átjáróhoz beállíthat a ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ee792-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="ee792-117">Ez a létrehozott VpnClientIPsecParameters objektum átkerül Set-AzVpnClientIpsecParameter parancsra, hogy a megadott VPN-alapú IPSec-házirendet a virtuális hálózati átjárón állítsa be a fenti példában látható módon.</span><span class="sxs-lookup"><span data-stu-id="ee792-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="ee792-118">Ez a parancs olyan VpnClientIPsecParameters-objektumot ad eredményül, amely a paraméterek beállítását jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="ee792-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="ee792-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee792-119">PARAMETERS</span></span>

### <span data-ttu-id="ee792-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee792-120">-DefaultProfile</span></span>
<span data-ttu-id="ee792-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee792-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee792-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee792-122">-InputObject</span></span>
<span data-ttu-id="ee792-123">A virtuális hálózat átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="ee792-123">The virtual network gateway object</span></span>

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

### <span data-ttu-id="ee792-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee792-124">-ResourceGroupName</span></span>
<span data-ttu-id="ee792-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ee792-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee792-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee792-126">-ResourceId</span></span>
<span data-ttu-id="ee792-127">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="ee792-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ee792-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="ee792-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="ee792-129">A virtuális hálózat átjárójának neve.</span><span class="sxs-lookup"><span data-stu-id="ee792-129">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee792-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="ee792-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="ee792-131">A VPN-ügyfél IPSec-paraméterei.</span><span class="sxs-lookup"><span data-stu-id="ee792-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="ee792-132">Ezt a paramétert a PS paranccsal lehet használni: új-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="ee792-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee792-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee792-133">-Confirm</span></span>
<span data-ttu-id="ee792-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee792-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee792-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee792-135">-WhatIf</span></span>
<span data-ttu-id="ee792-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee792-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee792-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee792-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee792-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee792-138">CommonParameters</span></span>
<span data-ttu-id="ee792-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee792-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee792-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee792-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee792-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee792-141">INPUTS</span></span>

### <span data-ttu-id="ee792-142">Microsoft. Azure. commands. Network. models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="ee792-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="ee792-143">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ee792-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="ee792-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ee792-144">System.String</span></span>

## <span data-ttu-id="ee792-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee792-145">OUTPUTS</span></span>

### <span data-ttu-id="ee792-146">Microsoft. Azure. commands. Network. models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="ee792-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="ee792-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee792-147">NOTES</span></span>

## <span data-ttu-id="ee792-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee792-148">RELATED LINKS</span></span>

[<span data-ttu-id="ee792-149">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="ee792-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="ee792-150">Új – AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="ee792-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="ee792-151">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="ee792-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)
