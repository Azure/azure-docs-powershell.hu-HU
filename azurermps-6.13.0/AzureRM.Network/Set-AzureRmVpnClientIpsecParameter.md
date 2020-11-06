---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 38dcfdb1188a810b0f154dfed31f8a1ef3206247
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498288"
---
# <span data-ttu-id="3c223-101">Set-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="3c223-101">Set-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="3c223-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c223-102">SYNOPSIS</span></span>
<span data-ttu-id="3c223-103">A meglévő virtuális hálózati átjáró VPN-IPSec-paramétereinek beállítása.</span><span class="sxs-lookup"><span data-stu-id="3c223-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c223-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c223-104">SYNTAX</span></span>

### <span data-ttu-id="3c223-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3c223-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c223-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3c223-106">ByFactoryObject</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c223-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3c223-107">ByResourceId</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c223-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c223-108">DESCRIPTION</span></span>
<span data-ttu-id="3c223-109">A **set-AzureRmVpnClientIpsecParameter** parancsmag a meglévő virtuális hálózati átjáró VPN-IPSec-paramétereit állítja be.</span><span class="sxs-lookup"><span data-stu-id="3c223-109">The **Set-AzureRmVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="3c223-110">A virtuális hálózati átjáró létrehozásakor a rendszer az alapértelmezett VPN-házirendeket az átjárón állítja be.</span><span class="sxs-lookup"><span data-stu-id="3c223-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="3c223-111">Abban az esetben, ha a webhely felhasználója szeretné használni bizonyos egyéni IPSec-házirendeket a VPN-átjáróhoz való csatlakozáshoz, először állítsa be az IPSec-házirendet a VPN-átjáróra.</span><span class="sxs-lookup"><span data-stu-id="3c223-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="3c223-112">A **set-AzureRmVpnClientIpsecParameter** biztosítja ezt a módot.</span><span class="sxs-lookup"><span data-stu-id="3c223-112">**Set-AzureRmVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="3c223-113">Példák</span><span class="sxs-lookup"><span data-stu-id="3c223-113">EXAMPLES</span></span>

### <span data-ttu-id="3c223-114">1. példa: egyéni VPN-házirendet állít be a meglévő virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3c223-114">Example 1 : Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="3c223-115">Ebben a példában az egyéni virtuális magánhálózati IPSec-házirendet az ContosoResourceGroup nevű erőforráscsoport ContosoVirtualGateway nevű meglévő virtuális hálózati átjáróhoz állítja be.</span><span class="sxs-lookup"><span data-stu-id="3c223-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="3c223-116">New-AzureRmVpnClientIpsecParameter parancsmag segítségével létrehozhatja a virtuális magánhálózati IPSec-paramétereket tartalmazó objektumot az átadott egy vagy minden paraméter értékével, amelyet a felhasználó bármely meglévő virtuális hálózati átjáróhoz beállíthat a ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3c223-116">New-AzureRmVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="3c223-117">Ez a létrehozott VpnClientIPsecParameters objektum átkerül Set-AzureRmVpnClientIpsecParameter parancsra, hogy a megadott VPN-alapú IPSec-házirendet a virtuális hálózati átjárón állítsa be a fenti példában látható módon.</span><span class="sxs-lookup"><span data-stu-id="3c223-117">This created VpnClientIPsecParameters object is passed to Set-AzureRmVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="3c223-118">Ez a parancs olyan VpnClientIPsecParameters-objektumot ad eredményül, amely a paraméterek beállítását jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="3c223-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="3c223-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c223-119">PARAMETERS</span></span>

### <span data-ttu-id="3c223-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c223-120">-DefaultProfile</span></span>
<span data-ttu-id="3c223-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c223-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c223-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c223-122">-InputObject</span></span>
<span data-ttu-id="3c223-123">A virtuális hálózat Gateaway objektuma</span><span class="sxs-lookup"><span data-stu-id="3c223-123">The virtual network gateaway object</span></span>

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

### <span data-ttu-id="3c223-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c223-124">-ResourceGroupName</span></span>
<span data-ttu-id="3c223-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3c223-125">The resource group name.</span></span>

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

### <span data-ttu-id="3c223-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c223-126">-ResourceId</span></span>
<span data-ttu-id="3c223-127">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="3c223-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3c223-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="3c223-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="3c223-129">A virtuális hálózat átjárójának neve.</span><span class="sxs-lookup"><span data-stu-id="3c223-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="3c223-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="3c223-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="3c223-131">A VPN-ügyfél IPSec-paraméterei.</span><span class="sxs-lookup"><span data-stu-id="3c223-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="3c223-132">Ezt a paramétert a PS paranccsal lehet használni: új-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="3c223-132">This parameter value can be constructed using PS command let:New-AzureRmVpnClientIpsecParameter</span></span>

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

### <span data-ttu-id="3c223-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3c223-133">-Confirm</span></span>
<span data-ttu-id="3c223-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3c223-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c223-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c223-135">-WhatIf</span></span>
<span data-ttu-id="3c223-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3c223-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c223-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3c223-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c223-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c223-138">CommonParameters</span></span>
<span data-ttu-id="3c223-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c223-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c223-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c223-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c223-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c223-141">INPUTS</span></span>

### <span data-ttu-id="3c223-142">Microsoft. Azure. commands. Network. models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="3c223-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>
<span data-ttu-id="3c223-143">Paraméterek: VpnClientIPsecParameter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3c223-143">Parameters: VpnClientIPsecParameter (ByValue)</span></span>

### <span data-ttu-id="3c223-144">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3c223-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="3c223-145">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3c223-145">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="3c223-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3c223-146">System.String</span></span>

## <span data-ttu-id="3c223-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c223-147">OUTPUTS</span></span>

### <span data-ttu-id="3c223-148">Microsoft. Azure. commands. Network. models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="3c223-148">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="3c223-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c223-149">NOTES</span></span>

## <span data-ttu-id="3c223-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c223-150">RELATED LINKS</span></span>

[<span data-ttu-id="3c223-151">Új – AzureRmVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="3c223-151">New-AzureRmVpnClientIpsecParameters</span></span>](./New-AzureRmVpnClientIpsecParameters.md)
