---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: a0c4e6835525dfbecd4bb7eca239f8327df6ff8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679390"
---
# <span data-ttu-id="34f6a-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="34f6a-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="34f6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="34f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="34f6a-103">Beállítja a virtuális hálózati átjáró VPN-ügyfél címének készletét.</span><span class="sxs-lookup"><span data-stu-id="34f6a-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34f6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="34f6a-104">SYNTAX</span></span>

### <span data-ttu-id="34f6a-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="34f6a-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34f6a-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="34f6a-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34f6a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="34f6a-107">DESCRIPTION</span></span>
<span data-ttu-id="34f6a-108">A **set-AzureRmVirtualNetworkVpnClientConfig** parancsmag egy virtuális hálózati átjáró ügyfél-címkészlet beállítása.</span><span class="sxs-lookup"><span data-stu-id="34f6a-108">The **Set-AzureRmVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="34f6a-109">Az átjáróhoz csatlakozó virtuális magánhálózati (VPN) ügyfelekhez az adott címkészlet IP-címe lesz társítva.</span><span class="sxs-lookup"><span data-stu-id="34f6a-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="34f6a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="34f6a-110">EXAMPLES</span></span>

### <span data-ttu-id="34f6a-111">1. példa: VPN-ügyfél címkészlet hozzárendelése virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="34f6a-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="34f6a-112">Ebben a példában a VPN-ügyfél címkészletet egy ContosoVirtualGateway nevű virtuális hálózati átjáróhoz rendeli.</span><span class="sxs-lookup"><span data-stu-id="34f6a-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="34f6a-113">Az első parancs létrehozza az átjáróra mutató objektumot, az objektum pedig egy $Gateway nevű változóban.</span><span class="sxs-lookup"><span data-stu-id="34f6a-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="34f6a-114">A példában szereplő második parancs a **set-AzureRmVirtualNetworkGatewayVpnClientConfig** parancsmagot használja a 10.0.0.0/16 a ContosoVirtualGateway-hoz rendelt címkészlet hozzárendeléséhez.</span><span class="sxs-lookup"><span data-stu-id="34f6a-114">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="34f6a-115">2. példa: külső RADIUS-alapú hitelesítés beállítása meglévő átjárón</span><span class="sxs-lookup"><span data-stu-id="34f6a-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="34f6a-116">Ebben a példában a VPN-ügyfél címkészletet egy ContosoVirtualGateway nevű virtuális hálózati átjáróhoz rendeli.</span><span class="sxs-lookup"><span data-stu-id="34f6a-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="34f6a-117">Az első parancs létrehozza az átjáróra mutató objektumot, az objektum pedig egy $Gateway nevű változóban.</span><span class="sxs-lookup"><span data-stu-id="34f6a-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="34f6a-118">A példában szereplő második parancs a **set-AzureRmVirtualNetworkGatewayVpnClientConfig** parancsmagot használja a 10.0.0.0/16 a ContosoVirtualGateway-hoz rendelt címkészlet hozzárendeléséhez.</span><span class="sxs-lookup"><span data-stu-id="34f6a-118">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="34f6a-119">A VPN-ügyfelek hitelesítéséhez a "TestRadiusServer" külső RADIUS-kiszolgálót is be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="34f6a-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="34f6a-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="34f6a-120">PARAMETERS</span></span>

### <span data-ttu-id="34f6a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f6a-121">-DefaultProfile</span></span>
<span data-ttu-id="34f6a-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="34f6a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34f6a-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="34f6a-123">-RadiusServerAddress</span></span>
<span data-ttu-id="34f6a-124">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="34f6a-124">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34f6a-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="34f6a-125">-RadiusServerSecret</span></span>
<span data-ttu-id="34f6a-126">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="34f6a-126">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34f6a-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="34f6a-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="34f6a-128">Annak a virtuális hálózati átjárónak az objektum hivatkozását adja meg, amely a parancsmag által módosított VPN-ügyfél konfigurációs beállításait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="34f6a-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="34f6a-129">A virtuális hálózati átjáróhoz az Get-AzureRmVirtualNetworkGateway használatával hozhat létre objektum-hivatkozást, és megadhatja az átjáró nevét.</span><span class="sxs-lookup"><span data-stu-id="34f6a-129">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34f6a-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="34f6a-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="34f6a-131">Az átjáróhoz csatlakozó ügyfeleknek kiosztani kívánt IP-címeket adja meg.</span><span class="sxs-lookup"><span data-stu-id="34f6a-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34f6a-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="34f6a-132">-Confirm</span></span>
<span data-ttu-id="34f6a-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="34f6a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34f6a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34f6a-134">-WhatIf</span></span>
<span data-ttu-id="34f6a-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="34f6a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34f6a-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="34f6a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34f6a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f6a-137">CommonParameters</span></span>
<span data-ttu-id="34f6a-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="34f6a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f6a-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34f6a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f6a-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="34f6a-140">INPUTS</span></span>

###  
<span data-ttu-id="34f6a-141">Ez a parancsmag a **Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway** objektum pipeline-példányait fogadja el.</span><span class="sxs-lookup"><span data-stu-id="34f6a-141">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="34f6a-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34f6a-142">OUTPUTS</span></span>

###  
<span data-ttu-id="34f6a-143">Ez a parancsmag módosítja a **Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway** objektum meglévő példányait.</span><span class="sxs-lookup"><span data-stu-id="34f6a-143">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="34f6a-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="34f6a-144">NOTES</span></span>

## <span data-ttu-id="34f6a-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34f6a-145">RELATED LINKS</span></span>

[<span data-ttu-id="34f6a-146">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="34f6a-146">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="34f6a-147">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="34f6a-147">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="34f6a-148">Átméretezés-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="34f6a-148">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


