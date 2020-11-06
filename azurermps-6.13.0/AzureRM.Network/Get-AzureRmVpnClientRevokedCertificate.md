---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: bb6a4c13b65697de624e9a9913e2f0f9cc6ea476
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495064"
---
# <span data-ttu-id="98688-101">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="98688-101">Get-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="98688-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98688-102">SYNOPSIS</span></span>
<span data-ttu-id="98688-103">Információt kap a VPN-ügyfél-visszavonási tanúsítványok közül.</span><span class="sxs-lookup"><span data-stu-id="98688-103">Gets information about VPN client-revocation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98688-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98688-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98688-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="98688-105">DESCRIPTION</span></span>
<span data-ttu-id="98688-106">A **Get-AzureRmVpnClientRevokedCertificate** parancsmag információt ad a virtuális hálózati átjáróhoz rendelt ügyfél-visszavonási tanúsítványok adatairól.</span><span class="sxs-lookup"><span data-stu-id="98688-106">The **Get-AzureRmVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="98688-107">Ügyfél – visszavonási tanúsítványok: megakadályozza, hogy az ügyfélszámítógépek a megadott tanúsítványt használják a hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="98688-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="98688-108">A **Get-AzureRmVpnClientRevokedCertificate** lehetővé teszi, hogy az összes ügyfél-visszavonási tanúsítványra vonatkozó információt visszaadja az átjárón, vagy a *VpnClientRevokedCertificateName* paraméter segítségével információkat kaphat egyetlen tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="98688-108">**Get-AzureRmVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="98688-109">Példák</span><span class="sxs-lookup"><span data-stu-id="98688-109">EXAMPLES</span></span>

### <span data-ttu-id="98688-110">1. példa: információk kérése az összes ügyfél-visszavonási tanúsítványról</span><span class="sxs-lookup"><span data-stu-id="98688-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="98688-111">Ez a parancs információt kap a ContosoVirtualNetworkGateway nevű virtuális hálózati átjáróval társított összes ügyfél-visszavonási tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="98688-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="98688-112">2. példa: információk beszerzése bizonyos ügyfél-visszavonási tanúsítványok esetén</span><span class="sxs-lookup"><span data-stu-id="98688-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="98688-113">Ez a parancs a parancs 1.</span><span class="sxs-lookup"><span data-stu-id="98688-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="98688-114">Ebben az esetben azonban a *VpnClientRevokedCertificateName* paraméterrel a visszaadott ügyfél által visszavont tanúsítványra kell korlátozni a visszaadott adatot: az ContosoRevokedClientCertificate nevet tartalmazó tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="98688-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="98688-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98688-115">PARAMETERS</span></span>

### <span data-ttu-id="98688-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98688-116">-DefaultProfile</span></span>
<span data-ttu-id="98688-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98688-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98688-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98688-118">-ResourceGroupName</span></span>
<span data-ttu-id="98688-119">Annak az erőforráscsoportnek a neve, amelyhez a virtuális hálózati átjáró van rendelve.</span><span class="sxs-lookup"><span data-stu-id="98688-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="98688-120">Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.</span><span class="sxs-lookup"><span data-stu-id="98688-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="98688-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="98688-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="98688-122">Annak a virtuális hálózati átjárónak a nevét adja meg, amelyben a visszavont tanúsítvány adatai vannak kiosztva.</span><span class="sxs-lookup"><span data-stu-id="98688-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="98688-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="98688-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="98688-124">Annak a VPN-ügyfélnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="98688-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="98688-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98688-125">CommonParameters</span></span>
<span data-ttu-id="98688-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98688-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98688-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98688-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98688-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98688-128">INPUTS</span></span>

### <span data-ttu-id="98688-129">System. String</span><span class="sxs-lookup"><span data-stu-id="98688-129">System.String</span></span>

## <span data-ttu-id="98688-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98688-130">OUTPUTS</span></span>

### <span data-ttu-id="98688-131">Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="98688-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="98688-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98688-132">NOTES</span></span>

## <span data-ttu-id="98688-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98688-133">RELATED LINKS</span></span>

[<span data-ttu-id="98688-134">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="98688-134">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="98688-135">Új – AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="98688-135">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="98688-136">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="98688-136">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


