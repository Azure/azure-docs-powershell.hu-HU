---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184803"
---
# <span data-ttu-id="c22fa-101">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c22fa-101">New-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="c22fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c22fa-102">SYNOPSIS</span></span>
<span data-ttu-id="c22fa-103">Létrehoz egy új VPN-ügyfél főtanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="c22fa-103">Creates a new VPN client root certificate.</span></span>

## <span data-ttu-id="c22fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c22fa-104">SYNTAX</span></span>

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c22fa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c22fa-105">DESCRIPTION</span></span>
<span data-ttu-id="c22fa-106">A **New-AzVpnClientRootCertificate** parancsmag létrehoz egy új virtuális magánhálózati tanúsítványt a virtuális hálózati átjárón való használatra.</span><span class="sxs-lookup"><span data-stu-id="c22fa-106">The **New-AzVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="c22fa-107">A legfelső szintű tanúsítványok olyan X. 509 tanúsítványok, amelyek a legfelső szintű hitelesítésszolgáltatót használják: az átjárón használt összes többi tanúsítvány meghatalmazza a főtanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="c22fa-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="c22fa-108">Ez a parancsmag olyan különálló tanúsítványt hoz létre, amely nem egy virtuális átjáróhoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="c22fa-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="c22fa-109">Ehelyett az **új AzVpnClientRootCertificate** által létrehozott tanúsítványt az New-AzVirtualNetworkGateway parancsmaggal együtt használják új átjáró létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="c22fa-109">Instead, the certificate created by **New-AzVpnClientRootCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="c22fa-110">Tegyük fel például, hogy létrehoz egy új tanúsítványt, és egy $Certificate nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c22fa-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="c22fa-111">Ezt a objektumtípust akkor használhatja, ha új virtuális átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c22fa-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="c22fa-112">Például `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="c22fa-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="c22fa-113">További információt az New-AzVirtualNetworkGateway parancsmag dokumentációjában talál.</span><span class="sxs-lookup"><span data-stu-id="c22fa-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="c22fa-114">Példák</span><span class="sxs-lookup"><span data-stu-id="c22fa-114">EXAMPLES</span></span>

### <span data-ttu-id="c22fa-115">1. példa: az ügyfél legfelső szintű tanúsítványának létrehozása</span><span class="sxs-lookup"><span data-stu-id="c22fa-115">Example 1: Create a client root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="c22fa-116">Ez a példa létrehoz egy ügyfélalkalmazás főtanúsítványát, és a tanúsítvány-objektumot egy $Certificate nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c22fa-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="c22fa-117">Ezt a változót a **New-AzVirtualNetworkGateway** parancsmag használhatja a root tanúsítvány új virtuális hálózati átjáróhoz való hozzáadására.</span><span class="sxs-lookup"><span data-stu-id="c22fa-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="c22fa-118">Az első parancs a **Get-Content** parancsmagot használva kapja meg a legfelső szintű tanúsítvány korábban exportált szövegét. a program a szöveges adatot egy $Text nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c22fa-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="c22fa-119">A második parancs ezután az a – Loop függvénnyel Kinyeri a szöveget az első és az utolsó sor kivételével, a kibontott szöveget a $CertificateText nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c22fa-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="c22fa-120">A harmadik parancs a **New-AzVpnClientRootCertificate** parancsmagot használja a tanúsítvány létrehozásához, és a létrehozott objektumot a $Certificate nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c22fa-120">The third command uses the **New-AzVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="c22fa-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c22fa-121">PARAMETERS</span></span>

### <span data-ttu-id="c22fa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c22fa-122">-DefaultProfile</span></span>
<span data-ttu-id="c22fa-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c22fa-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c22fa-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c22fa-124">-Name</span></span>
<span data-ttu-id="c22fa-125">Az új ügyfél főtanúsítványának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c22fa-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="c22fa-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="c22fa-126">-PublicCertData</span></span>
<span data-ttu-id="c22fa-127">A hozzáadni kívánt főtanúsítvány szöveges ábrázolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="c22fa-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="c22fa-128">A szöveges ábrázolás beolvasásához exportálja a tanúsítványt. cer formátumban (Base64 kódolással), majd nyissa meg az így létrejövő fájlt egy szövegszerkesztőben.</span><span class="sxs-lookup"><span data-stu-id="c22fa-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="c22fa-129">A kimenethez hasonló kimenetet kell látnia (Megjegyzendő, hogy a tényleges kimenet több sornyi szöveget fog tartalmazni, mint az itt látható):-----a tanúsítvány megkezdése-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----záró TANÚSÍTVÁNYát,-----a PublicCertData az első sor (-----KEZDÉSi tanúsítvány-----) és a fájl utolsó sora (-----záró tanúsítvány-----) közötti sorokból áll.</span><span class="sxs-lookup"><span data-stu-id="c22fa-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="c22fa-130">A PublicCertData a következőhöz hasonló Windows PowerShell-parancsokkal lehet letölteni: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i = 1; $i-lt $Text. hossza-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="c22fa-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="c22fa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c22fa-131">CommonParameters</span></span>
<span data-ttu-id="c22fa-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c22fa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c22fa-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c22fa-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c22fa-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c22fa-134">INPUTS</span></span>

### <span data-ttu-id="c22fa-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c22fa-135">System.String</span></span>

## <span data-ttu-id="c22fa-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c22fa-136">OUTPUTS</span></span>

### <span data-ttu-id="c22fa-137">Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c22fa-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="c22fa-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c22fa-138">NOTES</span></span>

## <span data-ttu-id="c22fa-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c22fa-139">RELATED LINKS</span></span>

[<span data-ttu-id="c22fa-140">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c22fa-140">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="c22fa-141">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c22fa-141">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="c22fa-142">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c22fa-142">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)

