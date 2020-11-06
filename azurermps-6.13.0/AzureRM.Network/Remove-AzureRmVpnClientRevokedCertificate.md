---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: e9095c5f2e8f2a9820214f1144f10f8049f22027
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494031"
---
# <span data-ttu-id="06171-101">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="06171-101">Remove-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="06171-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06171-102">SYNOPSIS</span></span>
<span data-ttu-id="06171-103">A VPN-ügyfél-visszavonási tanúsítvány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="06171-103">Removes a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06171-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06171-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06171-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06171-105">DESCRIPTION</span></span>
<span data-ttu-id="06171-106">A **Remove-AzureRmVpnClientRevokedCertificate** parancsmag egy ügyfél-visszavonási tanúsítványt távolít el egy virtuális hálózati átjáróról.</span><span class="sxs-lookup"><span data-stu-id="06171-106">The **Remove-AzureRmVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="06171-107">Ügyfél – visszavonási tanúsítványok: megakadályozza, hogy az ügyfélszámítógépek a megadott tanúsítványt használják a hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="06171-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="06171-108">Ha eltávolítja az ügyfél-visszavonási tanúsítványt futtató számítógépeket, a korábban betiltott tanúsítvány segítségével virtuális magánhálózati (VPN-) kapcsolatot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="06171-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="06171-109">Példák</span><span class="sxs-lookup"><span data-stu-id="06171-109">EXAMPLES</span></span>

### <span data-ttu-id="06171-110">1. példa: ügyfél-visszavonási tanúsítvány eltávolítása virtuális hálózati átjáróról</span><span class="sxs-lookup"><span data-stu-id="06171-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="06171-111">Ez a parancs eltávolítja a ContosoVirtualNetwork nevű virtuális hálózati átjárótól származó ügyfél-visszavonási tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="06171-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="06171-112">Az ügyfél-visszavonási tanúsítvány eltávolításához meg kell adnia a tanúsítvány nevét és a tanúsítvány ujjlenyomatát is.</span><span class="sxs-lookup"><span data-stu-id="06171-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="06171-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06171-113">PARAMETERS</span></span>

### <span data-ttu-id="06171-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06171-114">-DefaultProfile</span></span>
<span data-ttu-id="06171-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06171-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06171-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06171-116">-ResourceGroupName</span></span>
<span data-ttu-id="06171-117">Annak az erőforráscsoportnek a neve, amelyhez a virtuális hálózati átjáró van rendelve.</span><span class="sxs-lookup"><span data-stu-id="06171-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="06171-118">Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.</span><span class="sxs-lookup"><span data-stu-id="06171-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="06171-119">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="06171-119">-Thumbprint</span></span>
<span data-ttu-id="06171-120">Az eltávolított tanúsítvány egyedi azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="06171-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="06171-121">A tanúsítványok ujjlenyomat-adatait a következőhöz hasonló Windows PowerShell-parancs használatával adhatja vissza: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="06171-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="06171-122">Az előző parancs a Root Certificate Store áruházban talált összes helyi számítógép-tanúsítványra vonatkozó információt ad vissza.</span><span class="sxs-lookup"><span data-stu-id="06171-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="06171-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="06171-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="06171-124">Annak a virtuális hálózati átjárónak a neve, amelyhez a tanúsítvány van rendelve.</span><span class="sxs-lookup"><span data-stu-id="06171-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="06171-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="06171-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="06171-126">A VPN-ügyfél által eltávolított tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06171-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="06171-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06171-127">CommonParameters</span></span>
<span data-ttu-id="06171-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06171-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06171-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06171-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06171-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06171-130">INPUTS</span></span>

### <span data-ttu-id="06171-131">System. String</span><span class="sxs-lookup"><span data-stu-id="06171-131">System.String</span></span>

## <span data-ttu-id="06171-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06171-132">OUTPUTS</span></span>

### <span data-ttu-id="06171-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="06171-133">System.Boolean</span></span>

## <span data-ttu-id="06171-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06171-134">NOTES</span></span>

## <span data-ttu-id="06171-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06171-135">RELATED LINKS</span></span>

[<span data-ttu-id="06171-136">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="06171-136">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="06171-137">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="06171-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="06171-138">Új – AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="06171-138">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)


