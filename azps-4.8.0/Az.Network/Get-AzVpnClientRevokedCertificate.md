---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 04bc51a7040cae1310fd3c4fe51fd45c425fad8e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183041"
---
# <span data-ttu-id="01734-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="01734-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="01734-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01734-102">SYNOPSIS</span></span>
<span data-ttu-id="01734-103">Információt kap a VPN-ügyfél-visszavonási tanúsítványok közül.</span><span class="sxs-lookup"><span data-stu-id="01734-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="01734-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01734-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01734-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="01734-105">DESCRIPTION</span></span>
<span data-ttu-id="01734-106">A **Get-AzVpnClientRevokedCertificate** parancsmag információt ad a virtuális hálózati átjáróhoz rendelt ügyfél-visszavonási tanúsítványok adatairól.</span><span class="sxs-lookup"><span data-stu-id="01734-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="01734-107">Ügyfél – visszavonási tanúsítványok: megakadályozza, hogy az ügyfélszámítógépek a megadott tanúsítványt használják a hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="01734-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="01734-108">A **Get-AzVpnClientRevokedCertificate** lehetővé teszi, hogy az összes ügyfél-visszavonási tanúsítványra vonatkozó információt visszaadja az átjárón, vagy a *VpnClientRevokedCertificateName* paraméter segítségével információkat kaphat egyetlen tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="01734-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="01734-109">Példák</span><span class="sxs-lookup"><span data-stu-id="01734-109">EXAMPLES</span></span>

### <span data-ttu-id="01734-110">1. példa: információk kérése az összes ügyfél-visszavonási tanúsítványról</span><span class="sxs-lookup"><span data-stu-id="01734-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="01734-111">Ez a parancs információt kap a ContosoVirtualNetworkGateway nevű virtuális hálózati átjáróval társított összes ügyfél-visszavonási tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="01734-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="01734-112">2. példa: információk beszerzése bizonyos ügyfél-visszavonási tanúsítványok esetén</span><span class="sxs-lookup"><span data-stu-id="01734-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="01734-113">Ez a parancs a parancs 1.</span><span class="sxs-lookup"><span data-stu-id="01734-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="01734-114">Ebben az esetben azonban a *VpnClientRevokedCertificateName* paraméterrel a visszaadott ügyfél által visszavont tanúsítványra kell korlátozni a visszaadott adatot: az ContosoRevokedClientCertificate nevet tartalmazó tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="01734-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="01734-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01734-115">PARAMETERS</span></span>

### <span data-ttu-id="01734-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01734-116">-DefaultProfile</span></span>
<span data-ttu-id="01734-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01734-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01734-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01734-118">-ResourceGroupName</span></span>
<span data-ttu-id="01734-119">Annak az erőforráscsoportnek a neve, amelyhez a virtuális hálózati átjáró van rendelve.</span><span class="sxs-lookup"><span data-stu-id="01734-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="01734-120">Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.</span><span class="sxs-lookup"><span data-stu-id="01734-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="01734-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="01734-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="01734-122">Annak a virtuális hálózati átjárónak a nevét adja meg, amelyben a visszavont tanúsítvány adatai vannak kiosztva.</span><span class="sxs-lookup"><span data-stu-id="01734-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="01734-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="01734-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="01734-124">Annak a VPN-ügyfélnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="01734-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="01734-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01734-125">CommonParameters</span></span>
<span data-ttu-id="01734-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01734-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01734-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="01734-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01734-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01734-128">INPUTS</span></span>

### <span data-ttu-id="01734-129">System. String</span><span class="sxs-lookup"><span data-stu-id="01734-129">System.String</span></span>

## <span data-ttu-id="01734-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01734-130">OUTPUTS</span></span>

### <span data-ttu-id="01734-131">Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="01734-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="01734-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01734-132">NOTES</span></span>

## <span data-ttu-id="01734-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01734-133">RELATED LINKS</span></span>

[<span data-ttu-id="01734-134">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="01734-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="01734-135">Új – AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="01734-135">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="01734-136">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="01734-136">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


