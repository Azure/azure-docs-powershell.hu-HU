---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: f83a0f34e23822d5d6ff7c55236fdb81065b7f8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005909"
---
# <span data-ttu-id="ddefd-101">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ddefd-101">Remove-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="ddefd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddefd-102">SYNOPSIS</span></span>
<span data-ttu-id="ddefd-103">Eltávolít egy meglévő VPN-ügyféltanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="ddefd-103">Removes an existing VPN client root certificate.</span></span>

## <span data-ttu-id="ddefd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ddefd-104">SYNTAX</span></span>

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ddefd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ddefd-105">DESCRIPTION</span></span>
<span data-ttu-id="ddefd-106">A **Remove-AzVpnClientRootCertificate** parancsmag eltávolítja a megadott főtanúsítványt egy virtuális hálózati átjáróból.</span><span class="sxs-lookup"><span data-stu-id="ddefd-106">The **Remove-AzVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="ddefd-107">A főtanúsítványok olyan X.509-tanúsítványok, amelyek azonosítják a legfelső szintű hitelesítésszolgáltatót: az átjárón használt összes többi tanúsítvány megbízik a legfelső szintű tanúsítványban.</span><span class="sxs-lookup"><span data-stu-id="ddefd-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="ddefd-108">Ha eltávolít egy olyan főtanúsítvány-számítógépet, amely hitelesítési célokra használja a tanúsítványt, a továbbiakban nem tud csatlakozni az átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ddefd-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>
<span data-ttu-id="ddefd-109">A **Remove-AzVpnClientRootCertificate** használatakor meg kell adnunk a tanúsítvány nevét és a tanúsítványadatok szövegként való megjelenítését is.</span><span class="sxs-lookup"><span data-stu-id="ddefd-109">When you use **Remove-AzVpnClientRootCertificate**, you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="ddefd-110">A tanúsítványok szövegként való megjelenítéséről a *PublicCertData* paraméter leírásában található további információ.</span><span class="sxs-lookup"><span data-stu-id="ddefd-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="ddefd-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ddefd-111">EXAMPLES</span></span>

### <span data-ttu-id="ddefd-112">1. példa: Ügyfél legfelső szintű tanúsítványának eltávolítása virtuális hálózati átjáróból</span><span class="sxs-lookup"><span data-stu-id="ddefd-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```powershell
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="ddefd-113">Ez a példa eltávolítja a ContosoRootCertificate nevű ügyfélgyanúsítványt a ContosoVirtualGateway virtuális hálózati átjáróból.</span><span class="sxs-lookup"><span data-stu-id="ddefd-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>
<span data-ttu-id="ddefd-114">Az első parancs a **Get-Content** parancsmagot használja a tanúsítvány korábban exportált szövegként való megjelenítéséhez; ezt a szövegként való ábrázolás egy $Text.</span><span class="sxs-lookup"><span data-stu-id="ddefd-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>
<span data-ttu-id="ddefd-115">A második parancs ezután egy hurok segítségével kinyeri az összes szöveget a $Text az első és az utolsó sor kivételével.</span><span class="sxs-lookup"><span data-stu-id="ddefd-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="ddefd-116">Ez a kinyert szöveg egy $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="ddefd-116">This extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="ddefd-117">A harmadik parancs a $CertificateText változóban tárolt információkat és a **Remove-AzVpnClientRootCertificate** parancsmagot használja a tanúsítvány eltávolításához az átjáróból.</span><span class="sxs-lookup"><span data-stu-id="ddefd-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="ddefd-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddefd-118">PARAMETERS</span></span>

### <span data-ttu-id="ddefd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddefd-119">-DefaultProfile</span></span>
<span data-ttu-id="ddefd-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ddefd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddefd-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="ddefd-121">-PublicCertData</span></span>
<span data-ttu-id="ddefd-122">Az eltávolítható főtanúsítvány szöveges ábrázolása.</span><span class="sxs-lookup"><span data-stu-id="ddefd-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="ddefd-123">A szöveg reprezentáció beszerzéséhez exportálja a tanúsítványt .cer formátumban (Base64 kódolással), majd nyissa meg az így kapott fájlt egy szövegszerkesztőben.</span><span class="sxs-lookup"><span data-stu-id="ddefd-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="ddefd-124">Az alábbihoz hasonló kimenetet kell látnia (ne feledje, hogy a tényleges kimenet az itt látható rövidített mintaszövegnél több szövegsort fog tartalmazni): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span><span class="sxs-lookup"><span data-stu-id="ddefd-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="ddefd-125">A PublicCertData-adatbázist a következő Windows PowerShell-parancsokkal tudja lekérni: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="ddefd-125">You can retrieve the PublicCertData using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="ddefd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddefd-126">-ResourceGroupName</span></span>
<span data-ttu-id="ddefd-127">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a virtuális hálózati átjáró hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="ddefd-127">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="ddefd-128">Az erőforráscsoportok a készletkezelés és az általános Azure-felügyelet egyszerűsítése érdekében kategorizálják az elemeket.</span><span class="sxs-lookup"><span data-stu-id="ddefd-128">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="ddefd-129">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="ddefd-129">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="ddefd-130">Annak a virtuális hálózati átjárónak a nevét adja meg, amelyből a tanúsítványt eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="ddefd-130">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="ddefd-131">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="ddefd-131">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="ddefd-132">Annak az ügyfél-főtanúsítványnak a nevét adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="ddefd-132">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ddefd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddefd-133">CommonParameters</span></span>
<span data-ttu-id="ddefd-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddefd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddefd-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddefd-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddefd-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ddefd-136">INPUTS</span></span>

### <span data-ttu-id="ddefd-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ddefd-137">System.String</span></span>

## <span data-ttu-id="ddefd-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddefd-138">OUTPUTS</span></span>

### <span data-ttu-id="ddefd-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ddefd-139">System.Boolean</span></span>

## <span data-ttu-id="ddefd-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ddefd-140">NOTES</span></span>

## <span data-ttu-id="ddefd-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ddefd-141">RELATED LINKS</span></span>

[<span data-ttu-id="ddefd-142">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ddefd-142">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="ddefd-143">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ddefd-143">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="ddefd-144">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ddefd-144">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)


