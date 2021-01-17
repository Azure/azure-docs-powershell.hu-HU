---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: 3cf1bea87824320b659def722d0d0f0166fa177d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339389"
---
# <span data-ttu-id="fb5c5-101">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fb5c5-101">Get-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="fb5c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb5c5-102">SYNOPSIS</span></span>
<span data-ttu-id="fb5c5-103">Információkat kap a VPN-főtanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="fb5c5-103">Gets information about VPN root certificates.</span></span>

## <span data-ttu-id="fb5c5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fb5c5-104">SYNTAX</span></span>

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>] -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb5c5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fb5c5-105">DESCRIPTION</span></span>
<span data-ttu-id="fb5c5-106">A **Get-AzVpnClientRootCertificate** parancsmag a virtuális hálózati átjárókhoz rendelt főtanúsítványok adatait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="fb5c5-106">The **Get-AzVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="fb5c5-107">A főtanúsítványok olyan X.509-tanúsítványok, amelyek azonosítják a legfelső szintű hitelesítésszolgáltatót: az átjárón használt összes többi tanúsítvány megbízik a legfelső szintű tanúsítványban.</span><span class="sxs-lookup"><span data-stu-id="fb5c5-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="fb5c5-108">Alapértelmezés szerint a **Get-AzVpnClientRootCertificate** az átjáróhoz rendelt összes főtanúsítványról ad információkat.</span><span class="sxs-lookup"><span data-stu-id="fb5c5-108">By default, **Get-AzVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="fb5c5-109">(Az átjáróknak több főtanúsítványuk is lehet.) A **VpnClientRootCertificateName** paraméter megadva azonban korlátozhatja a visszaadott adatokat egy adott tanúsítványra.</span><span class="sxs-lookup"><span data-stu-id="fb5c5-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="fb5c5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fb5c5-110">EXAMPLES</span></span>

### <span data-ttu-id="fb5c5-111">1. példa: Információ az összes főtanúsítványról</span><span class="sxs-lookup"><span data-stu-id="fb5c5-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="fb5c5-112">Ez a parancs információkat kap a ContosoVirtualNetwork nevű virtuális hálózati átjáróhoz rendelt összes főtanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="fb5c5-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="fb5c5-113">2. példa: Információk az egyes főtanúsítványokról</span><span class="sxs-lookup"><span data-stu-id="fb5c5-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="fb5c5-114">Ez a parancs az 1. példában látható parancs egy változata.</span><span class="sxs-lookup"><span data-stu-id="fb5c5-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="fb5c5-115">Ebben az esetben azonban a *VpnClientRootCertificateName* paraméter azért szerepel itt, hogy a visszaadott adatokat egy adott gyökértanúsítványra korlátozza: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="fb5c5-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="fb5c5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb5c5-116">PARAMETERS</span></span>

### <span data-ttu-id="fb5c5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb5c5-117">-DefaultProfile</span></span>
<span data-ttu-id="fb5c5-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb5c5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb5c5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb5c5-119">-ResourceGroupName</span></span>
<span data-ttu-id="fb5c5-120">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a virtuális hálózati átjáró hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="fb5c5-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="fb5c5-121">Az erőforráscsoportok a készletkezelés és az általános Azure-felügyelet egyszerűsítése érdekében kategorizálják az elemeket.</span><span class="sxs-lookup"><span data-stu-id="fb5c5-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="fb5c5-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="fb5c5-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="fb5c5-123">Annak a virtuális hálózati átjárónak a nevét adja meg, ahol a főtanúsítvány van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="fb5c5-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="fb5c5-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="fb5c5-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="fb5c5-125">Annak az ügyfél-főtanúsítványnak a neve, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="fb5c5-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb5c5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb5c5-126">CommonParameters</span></span>
<span data-ttu-id="fb5c5-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb5c5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb5c5-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb5c5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb5c5-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb5c5-129">INPUTS</span></span>

### <span data-ttu-id="fb5c5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fb5c5-130">System.String</span></span>

## <span data-ttu-id="fb5c5-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb5c5-131">OUTPUTS</span></span>

### <span data-ttu-id="fb5c5-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fb5c5-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="fb5c5-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fb5c5-133">NOTES</span></span>

## <span data-ttu-id="fb5c5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb5c5-134">RELATED LINKS</span></span>

[<span data-ttu-id="fb5c5-135">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fb5c5-135">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="fb5c5-136">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fb5c5-136">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="fb5c5-137">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fb5c5-137">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


