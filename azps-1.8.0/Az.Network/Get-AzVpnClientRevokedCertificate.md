---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 42b8b0baa223c72642ad27e5ea823ba0dfa9e2df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670448"
---
# <span data-ttu-id="20520-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="20520-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="20520-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20520-102">SYNOPSIS</span></span>
<span data-ttu-id="20520-103">Információt kap a VPN-ügyfél-visszavonási tanúsítványok közül.</span><span class="sxs-lookup"><span data-stu-id="20520-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="20520-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20520-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20520-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="20520-105">DESCRIPTION</span></span>
<span data-ttu-id="20520-106">A **Get-AzVpnClientRevokedCertificate** parancsmag információt ad a virtuális hálózati átjáróhoz rendelt ügyfél-visszavonási tanúsítványok adatairól.</span><span class="sxs-lookup"><span data-stu-id="20520-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="20520-107">Ügyfél – visszavonási tanúsítványok: megakadályozza, hogy az ügyfélszámítógépek a megadott tanúsítványt használják a hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="20520-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="20520-108">A **Get-AzVpnClientRevokedCertificate** lehetővé teszi, hogy az összes ügyfél-visszavonási tanúsítványra vonatkozó információt visszaadja az átjárón, vagy a *VpnClientRevokedCertificateName* paraméter segítségével információkat kaphat egyetlen tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="20520-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="20520-109">Példák</span><span class="sxs-lookup"><span data-stu-id="20520-109">EXAMPLES</span></span>

### <span data-ttu-id="20520-110">1. példa: információk kérése az összes ügyfél-visszavonási tanúsítványról</span><span class="sxs-lookup"><span data-stu-id="20520-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="20520-111">Ez a parancs információt kap a ContosoVirtualNetworkGateway nevű virtuális hálózati átjáróval társított összes ügyfél-visszavonási tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="20520-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="20520-112">2. példa: információk beszerzése bizonyos ügyfél-visszavonási tanúsítványok esetén</span><span class="sxs-lookup"><span data-stu-id="20520-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="20520-113">Ez a parancs a parancs 1.</span><span class="sxs-lookup"><span data-stu-id="20520-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="20520-114">Ebben az esetben azonban a *VpnClientRevokedCertificateName* paraméterrel a visszaadott ügyfél által visszavont tanúsítványra kell korlátozni a visszaadott adatot: az ContosoRevokedClientCertificate nevet tartalmazó tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="20520-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="20520-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20520-115">PARAMETERS</span></span>

### <span data-ttu-id="20520-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20520-116">-DefaultProfile</span></span>
<span data-ttu-id="20520-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20520-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20520-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20520-118">-ResourceGroupName</span></span>
<span data-ttu-id="20520-119">Annak az erőforráscsoportnek a neve, amelyhez a virtuális hálózati átjáró van rendelve.</span><span class="sxs-lookup"><span data-stu-id="20520-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="20520-120">Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.</span><span class="sxs-lookup"><span data-stu-id="20520-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="20520-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="20520-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="20520-122">Annak a virtuális hálózati átjárónak a nevét adja meg, amelyben a visszavont tanúsítvány adatai vannak kiosztva.</span><span class="sxs-lookup"><span data-stu-id="20520-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="20520-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="20520-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="20520-124">Annak a VPN-ügyfélnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="20520-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="20520-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20520-125">CommonParameters</span></span>
<span data-ttu-id="20520-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20520-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20520-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="20520-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20520-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20520-128">INPUTS</span></span>

### <span data-ttu-id="20520-129">System. String</span><span class="sxs-lookup"><span data-stu-id="20520-129">System.String</span></span>

## <span data-ttu-id="20520-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20520-130">OUTPUTS</span></span>

### <span data-ttu-id="20520-131">Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="20520-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="20520-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20520-132">NOTES</span></span>

## <span data-ttu-id="20520-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20520-133">RELATED LINKS</span></span>

[<span data-ttu-id="20520-134">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="20520-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="20520-135">Új – AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="20520-135">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="20520-136">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="20520-136">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


