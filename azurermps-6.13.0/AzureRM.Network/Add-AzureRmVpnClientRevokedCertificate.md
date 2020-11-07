---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: c770bc2bb7c3fde9475ee844e12b8ed8c457dd56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680056"
---
# <span data-ttu-id="1b736-101">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1b736-101">Add-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="1b736-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1b736-102">SYNOPSIS</span></span>
<span data-ttu-id="1b736-103">VPN-ügyfél-visszavonási tanúsítvány felvétele</span><span class="sxs-lookup"><span data-stu-id="1b736-103">Adds a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b736-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1b736-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b736-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1b736-105">DESCRIPTION</span></span>
<span data-ttu-id="1b736-106">A **Add-AzureRmVpnClientRevokedCertificate** parancsmag ügyfél-visszavonási tanúsítványt rendel egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="1b736-106">The **Add-AzureRmVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="1b736-107">Ügyfél – visszavonási tanúsítványok: megakadályozza, hogy az ügyfélszámítógépek a megadott tanúsítványt használják a hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="1b736-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="1b736-108">A parancsmag használatához a tanúsítvány nevét és a tanúsítvány ujjlenyomatát is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="1b736-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="1b736-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1b736-109">EXAMPLES</span></span>

### <span data-ttu-id="1b736-110">1. példa: új ügyfél-visszavonási tanúsítvány hozzáadása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="1b736-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="1b736-111">Ez a parancs új ügyfél-visszavonási tanúsítványt ad hozzá a ContosoVirtualNetwork nevű virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="1b736-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="1b736-112">A tanúsítvány hozzáadásához meg kell adnia a tanúsítvány nevét és a tanúsítvány ujjlenyomatát is.</span><span class="sxs-lookup"><span data-stu-id="1b736-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="1b736-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1b736-113">PARAMETERS</span></span>

### <span data-ttu-id="1b736-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b736-114">-DefaultProfile</span></span>
<span data-ttu-id="1b736-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b736-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b736-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b736-116">-ResourceGroupName</span></span>
<span data-ttu-id="1b736-117">Annak az erőforráscsoportnek a neve, amelyhez a virtuális hálózati átjáró van rendelve.</span><span class="sxs-lookup"><span data-stu-id="1b736-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="1b736-118">Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.</span><span class="sxs-lookup"><span data-stu-id="1b736-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="1b736-119">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="1b736-119">-Thumbprint</span></span>
<span data-ttu-id="1b736-120">A hozzáadott tanúsítvány egyedi azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b736-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="1b736-121">Például:-ujjlenyomat "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" a tanúsítványok ujjlenyomat-információit a következőhöz hasonló Windows PowerShell-parancs segítségével érheti el: `Get-ChildItem -Path Cert:\LocalMachine\Root` .</span><span class="sxs-lookup"><span data-stu-id="1b736-121">For example: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>
<span data-ttu-id="1b736-122">Az előző parancs információt kap a főtanúsítvány-tárolóban talált összes helyi számítógép-tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="1b736-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="1b736-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="1b736-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="1b736-124">Annak a virtuális hálózati átjárónak a nevét adja meg, amelybe a tanúsítványt hozzá kívánja adni.</span><span class="sxs-lookup"><span data-stu-id="1b736-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="1b736-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="1b736-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="1b736-126">A hozzáadni kívánt virtuális magánhálózati ügyfél-tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b736-126">Specifies the name of the VPN client certificate to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b736-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b736-127">CommonParameters</span></span>
<span data-ttu-id="1b736-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1b736-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b736-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b736-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b736-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b736-130">INPUTS</span></span>

### <span data-ttu-id="1b736-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1b736-131">System.String</span></span>

## <span data-ttu-id="1b736-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b736-132">OUTPUTS</span></span>

### <span data-ttu-id="1b736-133">Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1b736-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="1b736-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1b736-134">NOTES</span></span>

## <span data-ttu-id="1b736-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b736-135">RELATED LINKS</span></span>

[<span data-ttu-id="1b736-136">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1b736-136">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="1b736-137">Új – AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1b736-137">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="1b736-138">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1b736-138">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


