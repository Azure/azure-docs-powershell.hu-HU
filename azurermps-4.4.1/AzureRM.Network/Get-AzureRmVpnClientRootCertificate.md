---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 14fcaa1d52d2491d807e654d98308236bf901d3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495547"
---
# <span data-ttu-id="a7026-101">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a7026-101">Get-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="a7026-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7026-102">SYNOPSIS</span></span>
<span data-ttu-id="a7026-103">Információt kap a virtuális magánhálózati tanúsítványokról.</span><span class="sxs-lookup"><span data-stu-id="a7026-103">Gets information about VPN root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7026-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7026-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRootCertificate [-VpnClientRootCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7026-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7026-105">DESCRIPTION</span></span>
<span data-ttu-id="a7026-106">A **Get-AzureRmVpnClientRootCertificate** parancsmag információt ad a virtuális hálózati átjáróhoz rendelt főtanúsítványokról.</span><span class="sxs-lookup"><span data-stu-id="a7026-106">The **Get-AzureRmVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="a7026-107">A legfelső szintű tanúsítványok olyan X. 509 tanúsítványok, amelyek a legfelső szintű hitelesítésszolgáltatót használják: az átjárón használt összes többi tanúsítvány meghatalmazza a főtanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="a7026-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="a7026-108">A **Get-AzureRmVpnClientRootCertificate** alapértelmezés szerint információt ad az átjáróhoz rendelt összes főtanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="a7026-108">By default, **Get-AzureRmVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="a7026-109">(Az átjárók több főtanúsítványt is tartalmazhatnak.) A **VpnClientRootCertificateName** paraméterrel azonban korlátozhatja, hogy egy adott tanúsítványra korlátozza a visszaadott adatot.</span><span class="sxs-lookup"><span data-stu-id="a7026-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="a7026-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a7026-110">EXAMPLES</span></span>

### <span data-ttu-id="a7026-111">1. példa: információk kérése az összes főtanúsítványról</span><span class="sxs-lookup"><span data-stu-id="a7026-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="a7026-112">Ez a parancs információt kap a ContosoVirtualNetwork nevű virtuális hálózati átjáróhoz rendelt összes főtanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="a7026-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="a7026-113">2. példa: információk kérése bizonyos főtanúsítványokról</span><span class="sxs-lookup"><span data-stu-id="a7026-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="a7026-114">Ez a parancs a parancs 1.</span><span class="sxs-lookup"><span data-stu-id="a7026-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="a7026-115">Ebben az esetben azonban a *VpnClientRootCertificateName* paramétert a program úgy számítja ki, hogy egy adott főtanúsítványra korlátozza a visszaadott adatot: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="a7026-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="a7026-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7026-116">PARAMETERS</span></span>

### <span data-ttu-id="a7026-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7026-117">-ResourceGroupName</span></span>
<span data-ttu-id="a7026-118">Annak az erőforráscsoportnek a neve, amelyhez a virtuális hálózati átjáró van rendelve.</span><span class="sxs-lookup"><span data-stu-id="a7026-118">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="a7026-119">Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.</span><span class="sxs-lookup"><span data-stu-id="a7026-119">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="a7026-120">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="a7026-120">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="a7026-121">Annak a virtuális hálózati átjárónak a nevét adja meg, ahol a főtanúsítvány van társítva.</span><span class="sxs-lookup"><span data-stu-id="a7026-121">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="a7026-122">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="a7026-122">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="a7026-123">Annak az ügyfél-főtanúsítványnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="a7026-123">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a7026-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7026-124">-DefaultProfile</span></span>
<span data-ttu-id="a7026-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7026-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7026-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7026-126">CommonParameters</span></span>
<span data-ttu-id="a7026-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7026-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7026-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7026-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7026-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7026-129">INPUTS</span></span>

## <span data-ttu-id="a7026-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7026-130">OUTPUTS</span></span>

###  
<span data-ttu-id="a7026-131">A **Get-AzureRmVpnClientRootCertificate** a **Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate** objektum példányait kapja.</span><span class="sxs-lookup"><span data-stu-id="a7026-131">**Get-AzureRmVpnClientRootCertificate** gets instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="a7026-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7026-132">NOTES</span></span>

## <span data-ttu-id="a7026-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7026-133">RELATED LINKS</span></span>

[<span data-ttu-id="a7026-134">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a7026-134">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="a7026-135">Új – AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a7026-135">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="a7026-136">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a7026-136">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


