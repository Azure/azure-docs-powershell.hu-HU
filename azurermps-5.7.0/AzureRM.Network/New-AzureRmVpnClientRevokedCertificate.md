---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e4b9c5e921ce9a1b46e92b40b6877beb51dc709
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501480"
---
# <span data-ttu-id="c07e7-101">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c07e7-101">New-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="c07e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c07e7-102">SYNOPSIS</span></span>
<span data-ttu-id="c07e7-103">Új VPN-ügyfél-visszavonási tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="c07e7-103">Creates a new VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c07e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c07e7-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c07e7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c07e7-105">DESCRIPTION</span></span>
<span data-ttu-id="c07e7-106">A **New-AzureRmVpnClientRevokedCertificate** parancsmag létrehoz egy új virtuális MAGÁNHÁLÓZATI (VPN) ügyfél-visszavonási tanúsítványt a virtuális hálózati átjáróban való használatra.</span><span class="sxs-lookup"><span data-stu-id="c07e7-106">The **New-AzureRmVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="c07e7-107">Ügyfél – visszavonási tanúsítványok: megakadályozza, hogy az ügyfélszámítógépek a megadott tanúsítványt használják a hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="c07e7-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>

<span data-ttu-id="c07e7-108">Ez a parancsmag olyan különálló tanúsítványt hoz létre, amely nem egy virtuális átjáróhoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="c07e7-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="c07e7-109">Ehelyett az **új AzureRmVpnClientRevokedCertificate** által létrehozott tanúsítvány az New-AzureRmVirtualNetworkGateway parancsmaggal együtt használatos, amikor új átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c07e7-109">Instead, the certificate created by **New-AzureRmVpnClientRevokedCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="c07e7-110">Tegyük fel például, hogy létrehoz egy új tanúsítványt, és egy $Certificate nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c07e7-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="c07e7-111">Az új virtuális átjáró létrehozásakor ezt a objektumtípust használhatja.</span><span class="sxs-lookup"><span data-stu-id="c07e7-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="c07e7-112">Például</span><span class="sxs-lookup"><span data-stu-id="c07e7-112">For instance,</span></span>

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`

<span data-ttu-id="c07e7-113">További információt az New-AzureRmVirtualNetworkGateway parancsmag dokumentációjában talál.</span><span class="sxs-lookup"><span data-stu-id="c07e7-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="c07e7-114">Példák</span><span class="sxs-lookup"><span data-stu-id="c07e7-114">EXAMPLES</span></span>

### <span data-ttu-id="c07e7-115">1. példa: új ügyfél által visszavont tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="c07e7-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="c07e7-116">Ez a parancs új ügyfél által visszavont tanúsítványt hoz létre, és a bizonyítvány-objektumot egy $Certificate nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c07e7-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="c07e7-117">Ezt a változót a **New-AzureRmVirtualNetworkGateway** parancsmag használhatja a tanúsítvány új virtuális hálózati átjáróhoz való hozzáadására.</span><span class="sxs-lookup"><span data-stu-id="c07e7-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="c07e7-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c07e7-118">PARAMETERS</span></span>

### <span data-ttu-id="c07e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c07e7-119">-DefaultProfile</span></span>
<span data-ttu-id="c07e7-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c07e7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07e7-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c07e7-121">-Name</span></span>
<span data-ttu-id="c07e7-122">Az új ügyfél-visszavonási tanúsítvány egyedi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c07e7-122">Specifies a unique name for the new client-revocation certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07e7-123">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="c07e7-123">-Thumbprint</span></span>
<span data-ttu-id="c07e7-124">A hozzáadott tanúsítvány egyedi azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c07e7-124">Specifies the unique identifier of the certificate being added.</span></span>

<span data-ttu-id="c07e7-125">A tanúsítványok ujjlenyomat-adatait a következőhöz hasonló Windows PowerShell-parancs használatával adhatja vissza:</span><span class="sxs-lookup"><span data-stu-id="c07e7-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path Cert:\LocalMachine\Root`

<span data-ttu-id="c07e7-126">Az előző parancs a Root Certificate Store áruházban talált összes helyi számítógép-tanúsítványra vonatkozó információt ad vissza.</span><span class="sxs-lookup"><span data-stu-id="c07e7-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07e7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c07e7-127">CommonParameters</span></span>
<span data-ttu-id="c07e7-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c07e7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c07e7-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c07e7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c07e7-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c07e7-130">INPUTS</span></span>

###  
<span data-ttu-id="c07e7-131">Ez a parancsmag nem fogadja el a csővezetékes bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c07e7-131">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="c07e7-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c07e7-132">OUTPUTS</span></span>

###  
<span data-ttu-id="c07e7-133">Ez a parancsmag a **Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate** objektum új példányait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="c07e7-133">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="c07e7-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c07e7-134">NOTES</span></span>

## <span data-ttu-id="c07e7-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c07e7-135">RELATED LINKS</span></span>

[<span data-ttu-id="c07e7-136">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c07e7-136">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="c07e7-137">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c07e7-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="c07e7-138">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c07e7-138">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


