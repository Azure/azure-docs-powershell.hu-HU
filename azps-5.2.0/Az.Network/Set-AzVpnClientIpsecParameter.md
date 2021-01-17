---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 658a242b724c57092bd155be69743f2080c07732
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365075"
---
# <span data-ttu-id="b0f5a-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="b0f5a-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="b0f5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="b0f5a-103">Beállítja a vpn ipsec paramétereit a meglévő virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="b0f5a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b0f5a-104">SYNTAX</span></span>

### <span data-ttu-id="b0f5a-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0f5a-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0f5a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b0f5a-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0f5a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b0f5a-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0f5a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b0f5a-108">DESCRIPTION</span></span>
<span data-ttu-id="b0f5a-109">A **Set-AzVpnClientIpsecParameter** parancsmag beállítja a vpn ipsec paramétereit a meglévő virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="b0f5a-110">Virtuális hálózati átjáró létrehozásakor beállítja az alapértelmezett vpn ipsec-házirendeket az Átjárón.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="b0f5a-111">Abban az esetben, ha a Point to site felhasználó bizonyos egyéni ipsec-házirendet szeretne használni a VPN-átjáróhoz való csatlakozáshoz, a felhasználónak előbb be kell állítania ezt az ipsec-házirendet a VPN-átjárón.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="b0f5a-112">**A Set-AzVpnClientIpsecParameter** erre kínál lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="b0f5a-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b0f5a-113">EXAMPLES</span></span>

### <span data-ttu-id="b0f5a-114">1. példa: Egyéni vpn ipsec-házirendet állít be meglévő virtuális hálózati átjáróra.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-114">Example 1: Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="b0f5a-115">Ebben a példában az egyéni vpn ipsec-házirendet a ContosoVirtualGateway nevű meglévő virtuális hálózati átjáróra állítja be a ContosoResourceGroup nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="b0f5a-116">New-AzVpnClientIpsecParameter a vpn ipsec paraméterobjektumának létrehozásához a felhasználó által az ResourceGroup bármely meglévő virtuális hálózati átjárója számára beállítható, átadott egy vagy az összes paraméter értékét használja.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="b0f5a-117">Ez a létrehozott VpnClientIPsecParameters objektum át van adva egy Set-AzVpnClientIpsecParameter-parancsnak, amely a megadott Vpn ipsec egyéni házirendet virtuális hálózati átjárón adja meg a fenti példában látható módon.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="b0f5a-118">Ez a parancs a VpnClientIPsecParameters objektumát adja vissza, amely a beállított paramétereket jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="b0f5a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0f5a-119">PARAMETERS</span></span>

### <span data-ttu-id="b0f5a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0f5a-120">-DefaultProfile</span></span>
<span data-ttu-id="b0f5a-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0f5a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0f5a-122">-InputObject</span></span>
<span data-ttu-id="b0f5a-123">A virtuális hálózati átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="b0f5a-123">The virtual network gateway object</span></span>

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

### <span data-ttu-id="b0f5a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0f5a-124">-ResourceGroupName</span></span>
<span data-ttu-id="b0f5a-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-125">The resource group name.</span></span>

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

### <span data-ttu-id="b0f5a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0f5a-126">-ResourceId</span></span>
<span data-ttu-id="b0f5a-127">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b0f5a-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="b0f5a-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="b0f5a-129">A virtuális hálózati átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="b0f5a-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="b0f5a-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="b0f5a-131">Vpn-ügyfél ipsec-paraméterei.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="b0f5a-132">Ez a paraméterérték a következő PS paranccsal épülhet fel: New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="b0f5a-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

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

### <span data-ttu-id="b0f5a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0f5a-133">-Confirm</span></span>
<span data-ttu-id="b0f5a-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0f5a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0f5a-135">-WhatIf</span></span>
<span data-ttu-id="b0f5a-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0f5a-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0f5a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0f5a-138">CommonParameters</span></span>
<span data-ttu-id="b0f5a-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0f5a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0f5a-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0f5a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0f5a-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0f5a-141">INPUTS</span></span>

### <span data-ttu-id="b0f5a-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="b0f5a-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="b0f5a-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b0f5a-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="b0f5a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b0f5a-144">System.String</span></span>

## <span data-ttu-id="b0f5a-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0f5a-145">OUTPUTS</span></span>

### <span data-ttu-id="b0f5a-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="b0f5a-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="b0f5a-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b0f5a-147">NOTES</span></span>

## <span data-ttu-id="b0f5a-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0f5a-148">RELATED LINKS</span></span>

[<span data-ttu-id="b0f5a-149">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="b0f5a-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="b0f5a-150">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="b0f5a-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="b0f5a-151">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="b0f5a-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)
