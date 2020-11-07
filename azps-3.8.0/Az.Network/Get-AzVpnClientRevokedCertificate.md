---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 04bc51a7040cae1310fd3c4fe51fd45c425fad8e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845901"
---
# <span data-ttu-id="75ba9-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="75ba9-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="75ba9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="75ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="75ba9-103">Információt kap a VPN-ügyfél-visszavonási tanúsítványok közül.</span><span class="sxs-lookup"><span data-stu-id="75ba9-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="75ba9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="75ba9-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75ba9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="75ba9-105">DESCRIPTION</span></span>
<span data-ttu-id="75ba9-106">A **Get-AzVpnClientRevokedCertificate** parancsmag információt ad a virtuális hálózati átjáróhoz rendelt ügyfél-visszavonási tanúsítványok adatairól.</span><span class="sxs-lookup"><span data-stu-id="75ba9-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="75ba9-107">Ügyfél – visszavonási tanúsítványok: megakadályozza, hogy az ügyfélszámítógépek a megadott tanúsítványt használják a hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="75ba9-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="75ba9-108">A **Get-AzVpnClientRevokedCertificate** lehetővé teszi, hogy az összes ügyfél-visszavonási tanúsítványra vonatkozó információt visszaadja az átjárón, vagy a *VpnClientRevokedCertificateName* paraméter segítségével információkat kaphat egyetlen tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="75ba9-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="75ba9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="75ba9-109">EXAMPLES</span></span>

### <span data-ttu-id="75ba9-110">1. példa: információk kérése az összes ügyfél-visszavonási tanúsítványról</span><span class="sxs-lookup"><span data-stu-id="75ba9-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="75ba9-111">Ez a parancs információt kap a ContosoVirtualNetworkGateway nevű virtuális hálózati átjáróval társított összes ügyfél-visszavonási tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="75ba9-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="75ba9-112">2. példa: információk beszerzése bizonyos ügyfél-visszavonási tanúsítványok esetén</span><span class="sxs-lookup"><span data-stu-id="75ba9-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="75ba9-113">Ez a parancs a parancs 1.</span><span class="sxs-lookup"><span data-stu-id="75ba9-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="75ba9-114">Ebben az esetben azonban a *VpnClientRevokedCertificateName* paraméterrel a visszaadott ügyfél által visszavont tanúsítványra kell korlátozni a visszaadott adatot: az ContosoRevokedClientCertificate nevet tartalmazó tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="75ba9-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="75ba9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="75ba9-115">PARAMETERS</span></span>

### <span data-ttu-id="75ba9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75ba9-116">-DefaultProfile</span></span>
<span data-ttu-id="75ba9-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75ba9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75ba9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75ba9-118">-ResourceGroupName</span></span>
<span data-ttu-id="75ba9-119">Annak az erőforráscsoportnek a neve, amelyhez a virtuális hálózati átjáró van rendelve.</span><span class="sxs-lookup"><span data-stu-id="75ba9-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="75ba9-120">Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.</span><span class="sxs-lookup"><span data-stu-id="75ba9-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="75ba9-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="75ba9-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="75ba9-122">Annak a virtuális hálózati átjárónak a nevét adja meg, amelyben a visszavont tanúsítvány adatai vannak kiosztva.</span><span class="sxs-lookup"><span data-stu-id="75ba9-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="75ba9-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="75ba9-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="75ba9-124">Annak a VPN-ügyfélnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="75ba9-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="75ba9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ba9-125">CommonParameters</span></span>
<span data-ttu-id="75ba9-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="75ba9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ba9-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="75ba9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ba9-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="75ba9-128">INPUTS</span></span>

### <span data-ttu-id="75ba9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="75ba9-129">System.String</span></span>

## <span data-ttu-id="75ba9-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75ba9-130">OUTPUTS</span></span>

### <span data-ttu-id="75ba9-131">Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="75ba9-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="75ba9-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="75ba9-132">NOTES</span></span>

## <span data-ttu-id="75ba9-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75ba9-133">RELATED LINKS</span></span>

[<span data-ttu-id="75ba9-134">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="75ba9-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="75ba9-135">Új – AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="75ba9-135">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="75ba9-136">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="75ba9-136">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


