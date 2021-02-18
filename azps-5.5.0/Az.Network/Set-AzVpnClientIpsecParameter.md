---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 658a242b724c57092bd155be69743f2080c07732
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202414"
---
# <span data-ttu-id="7fee0-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="7fee0-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="7fee0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fee0-102">SYNOPSIS</span></span>
<span data-ttu-id="7fee0-103">Beállítja a vpn ipsec paramétereit a meglévő virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7fee0-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="7fee0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7fee0-104">SYNTAX</span></span>

### <span data-ttu-id="7fee0-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7fee0-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fee0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7fee0-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fee0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7fee0-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fee0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7fee0-108">DESCRIPTION</span></span>
<span data-ttu-id="7fee0-109">A **Set-AzVpnClientIpsecParameter** parancsmag beállítja a vpn ipsec paramétereit a meglévő virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7fee0-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="7fee0-110">Virtuális hálózati átjáró létrehozásakor beállítja az alapértelmezett vpn ipsec-házirendeket az Átjárón.</span><span class="sxs-lookup"><span data-stu-id="7fee0-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="7fee0-111">Abban az esetben, ha a Point to site felhasználó bizonyos egyéni ipsec-házirendet szeretne használni a VPN-átjáróhoz való csatlakozáshoz, a felhasználónak előbb be kell állítania ezt az ipsec-házirendet a VPN-átjárón.</span><span class="sxs-lookup"><span data-stu-id="7fee0-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="7fee0-112">**A Set-AzVpnClientIpsecParameter** erre kínál lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="7fee0-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="7fee0-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7fee0-113">EXAMPLES</span></span>

### <span data-ttu-id="7fee0-114">1. példa: Egyéni vpn ipsec-házirendet állít be meglévő virtuális hálózati átjáróra.</span><span class="sxs-lookup"><span data-stu-id="7fee0-114">Example 1: Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="7fee0-115">Ebben a példában az egyéni vpn ipsec-házirendet a ContosoVirtualGateway nevű meglévő virtuális hálózati átjáróra állítja be a ContosoResourceGroup nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="7fee0-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="7fee0-116">New-AzVpnClientIpsecParameter a felhasználó által az ResourceGroup bármely meglévő virtuális hálózati átjárója számára beállítható, a megadott egy vagy több paraméter értékét használó VPN IPsec-paraméterek objektumának létrehozására használható.</span><span class="sxs-lookup"><span data-stu-id="7fee0-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="7fee0-117">Ez a létrehozott VpnClientIPsecParameters objektum át van adva egy Set-AzVpnClientIpsecParameter-parancsnak, amely a megadott Vpn ipsec egyéni házirendet virtuális hálózati átjárón adja meg a fenti példában látható módon.</span><span class="sxs-lookup"><span data-stu-id="7fee0-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="7fee0-118">Ez a parancs a VpnClientIPsecParameters objektumát adja vissza, amely a beállított paramétereket jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="7fee0-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="7fee0-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fee0-119">PARAMETERS</span></span>

### <span data-ttu-id="7fee0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fee0-120">-DefaultProfile</span></span>
<span data-ttu-id="7fee0-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7fee0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fee0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fee0-122">-InputObject</span></span>
<span data-ttu-id="7fee0-123">A virtuális hálózati átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="7fee0-123">The virtual network gateway object</span></span>

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

### <span data-ttu-id="7fee0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fee0-124">-ResourceGroupName</span></span>
<span data-ttu-id="7fee0-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7fee0-125">The resource group name.</span></span>

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

### <span data-ttu-id="7fee0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fee0-126">-ResourceId</span></span>
<span data-ttu-id="7fee0-127">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="7fee0-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7fee0-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="7fee0-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="7fee0-129">A virtuális hálózati átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="7fee0-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="7fee0-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="7fee0-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="7fee0-131">Vpn-ügyfél ipsec-paraméterei.</span><span class="sxs-lookup"><span data-stu-id="7fee0-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="7fee0-132">Ez a paraméterérték a következő PS paranccsal épülhet fel: New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="7fee0-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

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

### <span data-ttu-id="7fee0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fee0-133">-Confirm</span></span>
<span data-ttu-id="7fee0-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7fee0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fee0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fee0-135">-WhatIf</span></span>
<span data-ttu-id="7fee0-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7fee0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fee0-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7fee0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fee0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fee0-138">CommonParameters</span></span>
<span data-ttu-id="7fee0-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fee0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fee0-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fee0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fee0-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7fee0-141">INPUTS</span></span>

### <span data-ttu-id="7fee0-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="7fee0-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="7fee0-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7fee0-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="7fee0-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7fee0-144">System.String</span></span>

## <span data-ttu-id="7fee0-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fee0-145">OUTPUTS</span></span>

### <span data-ttu-id="7fee0-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="7fee0-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="7fee0-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7fee0-147">NOTES</span></span>

## <span data-ttu-id="7fee0-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fee0-148">RELATED LINKS</span></span>

[<span data-ttu-id="7fee0-149">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="7fee0-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="7fee0-150">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="7fee0-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="7fee0-151">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="7fee0-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)
