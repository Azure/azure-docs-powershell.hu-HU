---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: 847f1c06975e9bef570c5ab3fdaf5f6f3e4a99d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837258"
---
# <span data-ttu-id="23bd8-101">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="23bd8-101">Get-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="23bd8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="23bd8-103">Információt kap a virtuális magánhálózati tanúsítványokról.</span><span class="sxs-lookup"><span data-stu-id="23bd8-103">Gets information about VPN root certificates.</span></span>

## <span data-ttu-id="23bd8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23bd8-104">SYNTAX</span></span>

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>] -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23bd8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="23bd8-105">DESCRIPTION</span></span>
<span data-ttu-id="23bd8-106">A **Get-AzVpnClientRootCertificate** parancsmag információt ad a virtuális hálózati átjáróhoz rendelt főtanúsítványokról.</span><span class="sxs-lookup"><span data-stu-id="23bd8-106">The **Get-AzVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="23bd8-107">A legfelső szintű tanúsítványok olyan X. 509 tanúsítványok, amelyek a legfelső szintű hitelesítésszolgáltatót használják: az átjárón használt összes többi tanúsítvány meghatalmazza a főtanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="23bd8-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="23bd8-108">A **Get-AzVpnClientRootCertificate** alapértelmezés szerint információt ad az átjáróhoz rendelt összes főtanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="23bd8-108">By default, **Get-AzVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="23bd8-109">(Az átjárók több főtanúsítványt is tartalmazhatnak.) A **VpnClientRootCertificateName** paraméterrel azonban korlátozhatja, hogy egy adott tanúsítványra korlátozza a visszaadott adatot.</span><span class="sxs-lookup"><span data-stu-id="23bd8-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="23bd8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="23bd8-110">EXAMPLES</span></span>

### <span data-ttu-id="23bd8-111">1. példa: információk kérése az összes főtanúsítványról</span><span class="sxs-lookup"><span data-stu-id="23bd8-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="23bd8-112">Ez a parancs információt kap a ContosoVirtualNetwork nevű virtuális hálózati átjáróhoz rendelt összes főtanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="23bd8-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="23bd8-113">2. példa: információk kérése bizonyos főtanúsítványokról</span><span class="sxs-lookup"><span data-stu-id="23bd8-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="23bd8-114">Ez a parancs a parancs 1.</span><span class="sxs-lookup"><span data-stu-id="23bd8-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="23bd8-115">Ebben az esetben azonban a *VpnClientRootCertificateName* paramétert a program úgy számítja ki, hogy egy adott főtanúsítványra korlátozza a visszaadott adatot: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="23bd8-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="23bd8-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23bd8-116">PARAMETERS</span></span>

### <span data-ttu-id="23bd8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23bd8-117">-DefaultProfile</span></span>
<span data-ttu-id="23bd8-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23bd8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23bd8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23bd8-119">-ResourceGroupName</span></span>
<span data-ttu-id="23bd8-120">Annak az erőforráscsoportnek a neve, amelyhez a virtuális hálózati átjáró van rendelve.</span><span class="sxs-lookup"><span data-stu-id="23bd8-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="23bd8-121">Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.</span><span class="sxs-lookup"><span data-stu-id="23bd8-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="23bd8-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="23bd8-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="23bd8-123">Annak a virtuális hálózati átjárónak a nevét adja meg, ahol a főtanúsítvány van társítva.</span><span class="sxs-lookup"><span data-stu-id="23bd8-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="23bd8-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="23bd8-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="23bd8-125">Annak az ügyfél-főtanúsítványnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="23bd8-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="23bd8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23bd8-126">CommonParameters</span></span>
<span data-ttu-id="23bd8-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23bd8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23bd8-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="23bd8-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23bd8-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23bd8-129">INPUTS</span></span>

### <span data-ttu-id="23bd8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="23bd8-130">System.String</span></span>

## <span data-ttu-id="23bd8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23bd8-131">OUTPUTS</span></span>

### <span data-ttu-id="23bd8-132">Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="23bd8-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="23bd8-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23bd8-133">NOTES</span></span>

## <span data-ttu-id="23bd8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23bd8-134">RELATED LINKS</span></span>

[<span data-ttu-id="23bd8-135">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="23bd8-135">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="23bd8-136">Új – AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="23bd8-136">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="23bd8-137">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="23bd8-137">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


