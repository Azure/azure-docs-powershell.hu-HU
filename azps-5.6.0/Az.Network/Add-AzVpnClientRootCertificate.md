---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: 38a6abb631a77d41e38026edd3bef5abe9c70c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932442"
---
# <span data-ttu-id="979a5-101">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="979a5-101">Add-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="979a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="979a5-102">SYNOPSIS</span></span>
<span data-ttu-id="979a5-103">HOZZÁAD egy VPN-ügyfél legfelső szintű tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="979a5-103">Adds a VPN client root certificate.</span></span>

## <span data-ttu-id="979a5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="979a5-104">SYNTAX</span></span>

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="979a5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="979a5-105">DESCRIPTION</span></span>
<span data-ttu-id="979a5-106">Az **Add-AzVpnClientRootCertificate** parancsmag hozzáad egy főtanúsítványt egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="979a5-106">The **Add-AzVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="979a5-107">A főtanúsítványok olyan X.509-es tanúsítványok, amelyek azonosítják a legfelső szintű hitelesítésszolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="979a5-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="979a5-108">Az átjárón használt összes tanúsítvány terv szerint megbízik a főtanúsítványban.</span><span class="sxs-lookup"><span data-stu-id="979a5-108">By design, all certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="979a5-109">Ez a parancsmag egy meglévő tanúsítványt rendel hozzá átjáró-főtanúsítványként.</span><span class="sxs-lookup"><span data-stu-id="979a5-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="979a5-110">Ha nem rendelkezik X.509-es tanúsítvánnyal, létrehozhat egyet a nyilvános kulcsú infrastruktúrán keresztül, vagy használhat egy tanúsítványkészítőt, például az makecert.exe.</span><span class="sxs-lookup"><span data-stu-id="979a5-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>
<span data-ttu-id="979a5-111">Gyökértanúsítvány hozzáadásához meg kell adnia a tanúsítvány nevét, és csak szövegesen kell megadnia a tanúsítványt (további információért lásd a *PublicCertData* paramétert).</span><span class="sxs-lookup"><span data-stu-id="979a5-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="979a5-112">Az Azure lehetővé teszi több főtanúsítvány hozzárendelését egy átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="979a5-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="979a5-113">Több főtanúsítványt gyakran helyeznek üzembe olyan szervezetek, amelyek egynél több cég felhasználóit is magukban foglalják.</span><span class="sxs-lookup"><span data-stu-id="979a5-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="979a5-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="979a5-114">EXAMPLES</span></span>

### <span data-ttu-id="979a5-115">1. példa: Ügyfél legfelső szintű tanúsítványának hozzáadása virtuális átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="979a5-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="979a5-116">Ebben a példában egy ügyfél-főtanúsítványt ad hozzá a ContosoVirtualGateway nevű virtuális átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="979a5-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="979a5-117">Az első parancs **a Get-Content** parancsmag használatával bekéri a legfelső szintű tanúsítvány korábban exportált szövegét, és tárolja a $Text.</span><span class="sxs-lookup"><span data-stu-id="979a5-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>
<span data-ttu-id="979a5-118">A második parancs ezután egy hurok segítségével kinyeri az összes szöveget, kivéve az első és az utolsó sort.</span><span class="sxs-lookup"><span data-stu-id="979a5-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="979a5-119">A kinyert szöveget egy $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="979a5-119">The extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="979a5-120">A harmadik parancs ezután a $CertificateText-ben tárolt szöveget használja az **Add-AzVpnClientRootCertificate** parancsmaggal a legfelső szintű tanúsítvány hozzáadásához az átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="979a5-120">The third command then uses the text stored in $CertificateText with the **Add-AzVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="979a5-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="979a5-121">PARAMETERS</span></span>

### <span data-ttu-id="979a5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="979a5-122">-DefaultProfile</span></span>
<span data-ttu-id="979a5-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="979a5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="979a5-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="979a5-124">-PublicCertData</span></span>
<span data-ttu-id="979a5-125">A hozzáadni szükséges főtanúsítvány szövegként való ábrázolása.</span><span class="sxs-lookup"><span data-stu-id="979a5-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="979a5-126">A szöveg reprezentáció beszerzéséhez exportálja a tanúsítványt .cer formátumban (Base64 kódolással), majd nyissa meg az így kapott fájlt egy szövegszerkesztőben.</span><span class="sxs-lookup"><span data-stu-id="979a5-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="979a5-127">Ha így van, az alábbihoz hasonló kimenetet fog látni (vegye figyelembe, hogy a tényleges kimenet sokkal több szövegsort fog tartalmazni, mint az itt látható rövidített minta): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span><span class="sxs-lookup"><span data-stu-id="979a5-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="979a5-128">Ezek az adatok az ehhez hasonló Windows PowerShell-parancsokkal szerezhetők be: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="979a5-128">You can retrieve this data by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
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

### <span data-ttu-id="979a5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="979a5-129">-ResourceGroupName</span></span>
<span data-ttu-id="979a5-130">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a főtanúsítvány hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="979a5-130">Specifies the name of the resource group that the root certificate is assigned to.</span></span>
<span data-ttu-id="979a5-131">Az erőforráscsoportok a készletkezelés és az általános Azure-felügyelet egyszerűsítése érdekében kategorizálják az elemeket.</span><span class="sxs-lookup"><span data-stu-id="979a5-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="979a5-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="979a5-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="979a5-133">Annak a virtuális hálózati átjárónak a nevét adja meg, ahol a tanúsítványt hozzáadta.</span><span class="sxs-lookup"><span data-stu-id="979a5-133">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="979a5-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="979a5-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="979a5-135">Annak az ügyfél-főtanúsítványnak a nevét adja meg, amelybe a parancsmag hozzáadja.</span><span class="sxs-lookup"><span data-stu-id="979a5-135">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="979a5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="979a5-136">CommonParameters</span></span>
<span data-ttu-id="979a5-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="979a5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="979a5-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="979a5-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="979a5-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="979a5-139">INPUTS</span></span>

### <span data-ttu-id="979a5-140">System.String</span><span class="sxs-lookup"><span data-stu-id="979a5-140">System.String</span></span>

## <span data-ttu-id="979a5-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="979a5-141">OUTPUTS</span></span>

### <span data-ttu-id="979a5-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="979a5-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="979a5-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="979a5-143">NOTES</span></span>

## <span data-ttu-id="979a5-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="979a5-144">RELATED LINKS</span></span>

[<span data-ttu-id="979a5-145">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="979a5-145">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="979a5-146">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="979a5-146">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="979a5-147">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="979a5-147">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


