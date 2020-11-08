---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: efb8640f765468432a2927f865ce9f67c7b9164f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195722"
---
# <span data-ttu-id="4873d-101">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4873d-101">Add-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="4873d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4873d-102">SYNOPSIS</span></span>
<span data-ttu-id="4873d-103">VPN-ügyfél legfelső szintű tanúsítványát adja hozzá.</span><span class="sxs-lookup"><span data-stu-id="4873d-103">Adds a VPN client root certificate.</span></span>

## <span data-ttu-id="4873d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4873d-104">SYNTAX</span></span>

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4873d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4873d-105">DESCRIPTION</span></span>
<span data-ttu-id="4873d-106">Az **Add-AzVpnClientRootCertificate** parancsmag főtanúsítványot ad egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="4873d-106">The **Add-AzVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="4873d-107">A gyökérszintű tanúsítványok olyan X. 509 tanúsítványok, amelyek a legfelső szintű hitelesítésszolgáltatót hitelesítik.</span><span class="sxs-lookup"><span data-stu-id="4873d-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="4873d-108">Tervezéssel minden olyan tanúsítvány, amely az átjárón a legfelső szintű tanúsítványt használja.</span><span class="sxs-lookup"><span data-stu-id="4873d-108">By design, all certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="4873d-109">Ez a parancsmag egy meglévő tanúsítványt rendel el átjáró legfelső szintű tanúsítványként.</span><span class="sxs-lookup"><span data-stu-id="4873d-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="4873d-110">Ha nincs olyan X. 509 tanúsítvány, amellyel létrehozhatja a nyilvános kulcsú infrastruktúráját, vagy használhatja a tanúsítványt Generator (például makecert.exe) segítségével.</span><span class="sxs-lookup"><span data-stu-id="4873d-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>
<span data-ttu-id="4873d-111">Főtanúsítvány hozzáadásához meg kell adnia a tanúsítvány nevét, és csak szöveges formátumban kell megadnia a tanúsítványt (további információt *a PublicCertData* paraméterben talál).</span><span class="sxs-lookup"><span data-stu-id="4873d-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="4873d-112">Az Azure lehetővé teszi, hogy egynél több főtanúsítványt rendeljen egy átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="4873d-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="4873d-113">A több főtanúsítványt gyakran olyan szervezetek telepítik, amelyek egynél több vállalat felhasználóit tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="4873d-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="4873d-114">Példák</span><span class="sxs-lookup"><span data-stu-id="4873d-114">EXAMPLES</span></span>

### <span data-ttu-id="4873d-115">1. példa: az ügyfél legfelső szintű tanúsítványának felvétele virtuális átjáróba</span><span class="sxs-lookup"><span data-stu-id="4873d-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="4873d-116">Ez a példa a ContosoVirtualGateway nevű virtuális átjáróhoz hozzáadja az ügyfél főtanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="4873d-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="4873d-117">Az első parancs a **Get-Content** parancsmagot használva kapja meg a legfelső szintű tanúsítvány korábban exportált szöveges ábrázolását, és tárolja a szöveges adatok a $Text nevű változót.</span><span class="sxs-lookup"><span data-stu-id="4873d-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>
<span data-ttu-id="4873d-118">A második parancs ezután az a – Loop függvénnyel kinyeri az összes szövegrészt, az első és az utolsó soron kívül.</span><span class="sxs-lookup"><span data-stu-id="4873d-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="4873d-119">A kibontott szöveg egy $CertificateText nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="4873d-119">The extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="4873d-120">A harmadik parancs ezután a $CertificateText-ban tárolt szöveget használja az **Add-AzVpnClientRootCertificate** parancsmaggal a főtanúsítványnak az átjáróhoz való hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="4873d-120">The third command then uses the text stored in $CertificateText with the **Add-AzVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="4873d-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4873d-121">PARAMETERS</span></span>

### <span data-ttu-id="4873d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4873d-122">-DefaultProfile</span></span>
<span data-ttu-id="4873d-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4873d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4873d-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="4873d-124">-PublicCertData</span></span>
<span data-ttu-id="4873d-125">A beadni kívánt főtanúsítvány szöveges ábrázolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="4873d-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="4873d-126">A szöveges ábrázolás beolvasásához exportálja a tanúsítványt. cer formátumban (Base64 kódolással), majd nyissa meg az így létrejövő fájlt egy szövegszerkesztőben.</span><span class="sxs-lookup"><span data-stu-id="4873d-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="4873d-127">Ha ezt a lehetőséget választja, az alábbihoz hasonló kimenet jelenik meg (Megjegyzendő, hogy a tényleges kimenet több sornyi szöveget tartalmaz, mint az itt látható):-----a-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----záró TANÚSÍTVÁNYát,-----a PublicCertData az első sor (-----KEZDÉSi tanúsítvány-----) és a fájl utolsó sora (-----záró tanúsítvány-----) közötti sorokból áll.</span><span class="sxs-lookup"><span data-stu-id="4873d-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="4873d-128">Ezeket az adatforrásokat az alábbihoz hasonló Windows PowerShell-parancsok segítségével tudja letölteni: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="4873d-128">You can retrieve this data by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

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

### <span data-ttu-id="4873d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4873d-129">-ResourceGroupName</span></span>
<span data-ttu-id="4873d-130">Annak az erőforráscsoportnek a neve, amelyhez a főtanúsítvány van rendelve.</span><span class="sxs-lookup"><span data-stu-id="4873d-130">Specifies the name of the resource group that the root certificate is assigned to.</span></span>
<span data-ttu-id="4873d-131">Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.</span><span class="sxs-lookup"><span data-stu-id="4873d-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="4873d-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="4873d-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="4873d-133">Annak a virtuális hálózati átjárónak a neve, amelybe a tanúsítványt felveszi.</span><span class="sxs-lookup"><span data-stu-id="4873d-133">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="4873d-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="4873d-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="4873d-135">Annak az ügyfél-főtanúsítványnak a nevét adja meg, amelyre a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="4873d-135">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="4873d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4873d-136">CommonParameters</span></span>
<span data-ttu-id="4873d-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4873d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4873d-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4873d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4873d-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4873d-139">INPUTS</span></span>

### <span data-ttu-id="4873d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4873d-140">System.String</span></span>

## <span data-ttu-id="4873d-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4873d-141">OUTPUTS</span></span>

### <span data-ttu-id="4873d-142">Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4873d-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="4873d-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4873d-143">NOTES</span></span>

## <span data-ttu-id="4873d-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4873d-144">RELATED LINKS</span></span>

[<span data-ttu-id="4873d-145">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4873d-145">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="4873d-146">Új – AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4873d-146">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="4873d-147">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4873d-147">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


