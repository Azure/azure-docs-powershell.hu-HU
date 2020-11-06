---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 99d7d4a0feeb0f548ef65d06234eecb1ad2baf6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504671"
---
# <span data-ttu-id="e121e-101">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="e121e-101">New-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="e121e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e121e-102">SYNOPSIS</span></span>
<span data-ttu-id="e121e-103">Az Azure Web App-hoz létrehoz egy SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="e121e-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e121e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e121e-104">SYNTAX</span></span>

### <span data-ttu-id="e121e-105">S1</span><span class="sxs-lookup"><span data-stu-id="e121e-105">S1</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e121e-106">S2</span><span class="sxs-lookup"><span data-stu-id="e121e-106">S2</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e121e-107">S3</span><span class="sxs-lookup"><span data-stu-id="e121e-107">S3</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e121e-108">S4</span><span class="sxs-lookup"><span data-stu-id="e121e-108">S4</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e121e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e121e-109">DESCRIPTION</span></span>
<span data-ttu-id="e121e-110">A **New-AzureRmWebAppSSLBinding** parancsmag létrehoz egy Secure Socket Layer (SSL) tanúsítvány-kötést az Azure Web App alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="e121e-110">The **New-AzureRmWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="e121e-111">A parancsmag két módon hoz létre SSL-kötést:</span><span class="sxs-lookup"><span data-stu-id="e121e-111">The cmdlet creates an SSL binding in two ways:</span></span> 

- <span data-ttu-id="e121e-112">Egy webalkalmazást meglévő tanúsítványhoz köthet le.</span><span class="sxs-lookup"><span data-stu-id="e121e-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="e121e-113">Feltöltheti az új tanúsítványt, majd az új tanúsítványhoz rögzítheti a webalkalmazást.</span><span class="sxs-lookup"><span data-stu-id="e121e-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>

<span data-ttu-id="e121e-114">Attól függetlenül, hogy melyik módszert használja, a tanúsítványnak és a webalkalmazásnak ugyanahhoz az Azure-erőforrás csoporthoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="e121e-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="e121e-115">Ha van egy webalkalmazása az A erőforráscsoport-ban, és a webalkalmazást egy, a B erőforrás csoportba tartozó tanúsítványba szeretné kötni, az egyetlen mód arra, hogy a tanúsítvány másolatát feltöltse az A erőforrás csoportba.</span><span class="sxs-lookup"><span data-stu-id="e121e-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A.</span></span>

<span data-ttu-id="e121e-116">Új tanúsítvány feltöltése esetén tartsa szem előtt az alábbi követelményeket az Azure SSL-tanúsítványok esetében:</span><span class="sxs-lookup"><span data-stu-id="e121e-116">If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 

- <span data-ttu-id="e121e-117">A tanúsítványnak tartalmaznia kell egy titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="e121e-117">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="e121e-118">A tanúsítványnak a személyes adatok cseréje (PFX) formátumát kell használnia.</span><span class="sxs-lookup"><span data-stu-id="e121e-118">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="e121e-119">A tanúsítvány tulajdonosának nevének egyeznie kell a webalkalmazás eléréséhez használt tartománnyal.</span><span class="sxs-lookup"><span data-stu-id="e121e-119">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="e121e-120">A tanúsítványnak legalább 2048 bites titkosítást kell használnia.</span><span class="sxs-lookup"><span data-stu-id="e121e-120">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="e121e-121">Példák</span><span class="sxs-lookup"><span data-stu-id="e121e-121">EXAMPLES</span></span>

### <span data-ttu-id="e121e-122">1. példa: tanúsítvány kötése webalkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="e121e-122">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com" -CertificatePassword "p@ssw0rd"
```

<span data-ttu-id="e121e-123">Ez a parancs egy meglévő Azure-tanúsítványt (az ujjlenyomat-E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 tartalmazó tanúsítványt) köti össze a ContosoWebApp nevű webalkalmazással.</span><span class="sxs-lookup"><span data-stu-id="e121e-123">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

### <span data-ttu-id="e121e-124">2. példa: tanúsítvány feltöltése és webalkalmazáshoz kötése</span><span class="sxs-lookup"><span data-stu-id="e121e-124">Example 2: Upload a certificate and bind it to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com" -CertificatePassword "p@ssw0rd" -CertificateFilePath "C:\Certificates\ContosoWebSite.pfx"
```

<span data-ttu-id="e121e-125">Példa: a E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 az ContosoWebApp nevű webalkalmazáshoz is köti a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="e121e-125">Example 2 also binds the certificate E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="e121e-126">Ebben az esetben azonban a tanúsítvány még nincs feltöltve az Azure-ra.</span><span class="sxs-lookup"><span data-stu-id="e121e-126">In this case, however, the certificate has not yet been uploaded to Azure.</span></span>
<span data-ttu-id="e121e-127">Emiatt a *CertificateFilePath* paraméter a tanúsítvány helyi példányának megadására szolgál. PFX-fájl.</span><span class="sxs-lookup"><span data-stu-id="e121e-127">Because of that, the *CertificateFilePath* parameter is used to specify the local copy of the certificate .PFX file.</span></span>
<span data-ttu-id="e121e-128">Ezt a tanúsítványt az Azure-ra tölti fel a rendszer, majd létrejön az új SSL-kötések.</span><span class="sxs-lookup"><span data-stu-id="e121e-128">This certificate will be uploaded to Azure and then the new SSL bindings will be created.</span></span>

## <span data-ttu-id="e121e-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e121e-129">PARAMETERS</span></span>

### <span data-ttu-id="e121e-130">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e121e-130">-CertificateFilePath</span></span>
<span data-ttu-id="e121e-131">A feltölteni kívánt tanúsítvány elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e121e-131">Specifies the file path for the certificate to be uploaded.</span></span>

<span data-ttu-id="e121e-132">A *CertificateFilePath* paraméter csak akkor szükséges, ha a tanúsítvány még nincs feltöltve az Azure-ra.</span><span class="sxs-lookup"><span data-stu-id="e121e-132">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e121e-133">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e121e-133">-CertificatePassword</span></span>
<span data-ttu-id="e121e-134">A tanúsítvány visszafejtési jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e121e-134">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e121e-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e121e-135">-Name</span></span>
<span data-ttu-id="e121e-136">A webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e121e-136">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e121e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e121e-137">-ResourceGroupName</span></span>
<span data-ttu-id="e121e-138">Annak az erőforráscsoportnek a neve, amelyhez a tanúsítvány van rendelve.</span><span class="sxs-lookup"><span data-stu-id="e121e-138">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="e121e-139">A *ResourceGroupName* paraméter és a *WebApp* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="e121e-139">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e121e-140">-Slot</span><span class="sxs-lookup"><span data-stu-id="e121e-140">-Slot</span></span>
<span data-ttu-id="e121e-141">A webalkalmazás-telepítő bővítőhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e121e-141">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="e121e-142">A Get-AzureRMWebAppSlot parancsmaggal letölthet egy bővítőhelyet.</span><span class="sxs-lookup"><span data-stu-id="e121e-142">You can use the Get-AzureRMWebAppSlot cmdlet to get a slot.</span></span>

<span data-ttu-id="e121e-143">A telepítő bővítőhelyek segítségével a webes alkalmazások csak akkor érhetők el, ha az alkalmazások nem érhetők el az interneten keresztül.</span><span class="sxs-lookup"><span data-stu-id="e121e-143">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="e121e-144">Általában a módosításokat egy átmeneti webhelyre telepíti, érvényesíti ezeket a módosításokat, majd üzembe helyezi a termelés (internetről elérhető) webhelyre.</span><span class="sxs-lookup"><span data-stu-id="e121e-144">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e121e-145">-SslState</span><span class="sxs-lookup"><span data-stu-id="e121e-145">-SslState</span></span>
<span data-ttu-id="e121e-146">Megadja, hogy engedélyezve van-e a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="e121e-146">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="e121e-147">Állítsa a *SSLState* paramétert 1-re a tanúsítvány engedélyezéséhez, vagy állítsa a *SSLState* 0-ra a tanúsítvány letiltásához.</span><span class="sxs-lookup"><span data-stu-id="e121e-147">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e121e-148">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="e121e-148">-Thumbprint</span></span>
<span data-ttu-id="e121e-149">A tanúsítvány egyedi azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e121e-149">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e121e-150">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e121e-150">-WebApp</span></span>
<span data-ttu-id="e121e-151">Egy webalkalmazást ad meg.</span><span class="sxs-lookup"><span data-stu-id="e121e-151">Specifies a Web App.</span></span>
<span data-ttu-id="e121e-152">Ha egy webalkalmazást szeretne beszerezni, használja az Get-AzureRmWebApp parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e121e-152">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="e121e-153">A *WebApp* paraméter nem használható ugyanabban a parancsban, mint a *ResourceGroupName* paraméter és/vagy a *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="e121e-153">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e121e-154">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="e121e-154">-WebAppName</span></span>
<span data-ttu-id="e121e-155">Annak a webalkalmazásnak a nevét adja meg, amelyhez az új SSL-kötést létrehozta.</span><span class="sxs-lookup"><span data-stu-id="e121e-155">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>

<span data-ttu-id="e121e-156">A *WebAppName* paraméter és a *WebApp* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="e121e-156">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e121e-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e121e-157">-DefaultProfile</span></span>
<span data-ttu-id="e121e-158">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e121e-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e121e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e121e-159">CommonParameters</span></span>
<span data-ttu-id="e121e-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e121e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e121e-161">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e121e-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e121e-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e121e-162">INPUTS</span></span>

### <span data-ttu-id="e121e-163">Webhely</span><span class="sxs-lookup"><span data-stu-id="e121e-163">Site</span></span>
<span data-ttu-id="e121e-164">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e121e-164">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e121e-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e121e-165">OUTPUTS</span></span>

## <span data-ttu-id="e121e-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e121e-166">NOTES</span></span>

## <span data-ttu-id="e121e-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e121e-167">RELATED LINKS</span></span>

[<span data-ttu-id="e121e-168">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="e121e-168">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="e121e-169">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="e121e-169">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="e121e-170">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e121e-170">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="e121e-171">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e121e-171">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


