---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: c5ceef5ec70ac337180c8e2fcf6bb567c68391a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918721"
---
# <span data-ttu-id="e193e-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e193e-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="e193e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e193e-102">SYNOPSIS</span></span>
<span data-ttu-id="e193e-103">Információkat kap a VPN-ügyfél-visszavonási tanúsítványokról.</span><span class="sxs-lookup"><span data-stu-id="e193e-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="e193e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e193e-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e193e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e193e-105">DESCRIPTION</span></span>
<span data-ttu-id="e193e-106">A **Get-AzVpnClientRevokedCertificate parancsmag** a virtuális hálózati átjáróhoz rendelt ügyfél-visszavonási tanúsítványok adatait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="e193e-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="e193e-107">Az ügyfél-visszavonási tanúsítványok megakadályozzák, hogy az ügyfélszámítógépek a megadott tanúsítványt használják hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="e193e-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="e193e-108">**A Get-AzVpnClientRevokedCertificate** lehetővé teszi, hogy az átjáróban lévő összes ügyfél-visszavonási tanúsítvány adatait visszaadja, vagy a *VpnClientRevokedCertificateName* paraméter használatával információt kap egy tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="e193e-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="e193e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e193e-109">EXAMPLES</span></span>

### <span data-ttu-id="e193e-110">1. példa: Információ az összes ügyfél-visszavonási tanúsítványról</span><span class="sxs-lookup"><span data-stu-id="e193e-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="e193e-111">Ez a parancs információkat kap a ContosoVirtualNetworkGateway nevű virtuális hálózati átjáróhoz társított összes ügyfél-visszavonási tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="e193e-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="e193e-112">2. példa: Információk lekérte az egyes ügyfél-visszavonási tanúsítványokról</span><span class="sxs-lookup"><span data-stu-id="e193e-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="e193e-113">Ez a parancs az 1. példában látható parancs egy változata.</span><span class="sxs-lookup"><span data-stu-id="e193e-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="e193e-114">Ebben az esetben azonban a *VpnClientRevokedCertificateName* paraméter egy adott ügyfél által visszavont tanúsítványra korlátozza a visszaadott adatokat: a ContosoRevokedClientCertificate nevű tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="e193e-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="e193e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e193e-115">PARAMETERS</span></span>

### <span data-ttu-id="e193e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e193e-116">-DefaultProfile</span></span>
<span data-ttu-id="e193e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e193e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e193e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e193e-118">-ResourceGroupName</span></span>
<span data-ttu-id="e193e-119">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a virtuális hálózati átjáró hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="e193e-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="e193e-120">Az erőforráscsoportok a készletkezelés és az általános Azure-felügyelet egyszerűsítése érdekében kategorizálják az elemeket.</span><span class="sxs-lookup"><span data-stu-id="e193e-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="e193e-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="e193e-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="e193e-122">Annak a virtuális hálózati átjárónak a nevét adja meg, ahol a visszavont tanúsítvány adatai hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="e193e-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="e193e-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="e193e-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="e193e-124">Annak a VPN-ügyfélalkalmazásnak a nevét adja meg, amelybe a parancsmagot beállítja.</span><span class="sxs-lookup"><span data-stu-id="e193e-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e193e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e193e-125">CommonParameters</span></span>
<span data-ttu-id="e193e-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e193e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e193e-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e193e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e193e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e193e-128">INPUTS</span></span>

### <span data-ttu-id="e193e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e193e-129">System.String</span></span>

## <span data-ttu-id="e193e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e193e-130">OUTPUTS</span></span>

### <span data-ttu-id="e193e-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e193e-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="e193e-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e193e-132">NOTES</span></span>

## <span data-ttu-id="e193e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e193e-133">RELATED LINKS</span></span>

[<span data-ttu-id="e193e-134">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e193e-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="e193e-135">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e193e-135">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="e193e-136">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e193e-136">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


