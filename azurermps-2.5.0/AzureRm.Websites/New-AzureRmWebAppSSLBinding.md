---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
ms.openlocfilehash: 0a396b93a0ce1435302b1ee2f81d8700ec10a60d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850522"
---
# <span data-ttu-id="18137-101">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="18137-101">New-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="18137-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18137-102">SYNOPSIS</span></span>
<span data-ttu-id="18137-103">Az Azure Web App-hoz létrehoz egy SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="18137-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18137-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18137-104">SYNTAX</span></span>

### <span data-ttu-id="18137-105">S1</span><span class="sxs-lookup"><span data-stu-id="18137-105">S1</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18137-106">S2</span><span class="sxs-lookup"><span data-stu-id="18137-106">S2</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18137-107">S3</span><span class="sxs-lookup"><span data-stu-id="18137-107">S3</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18137-108">S4</span><span class="sxs-lookup"><span data-stu-id="18137-108">S4</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18137-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="18137-109">DESCRIPTION</span></span>
<span data-ttu-id="18137-110">A **New-AzureRmWebAppSSLBinding** parancsmag létrehoz egy Secure Socket Layer (SSL) tanúsítvány-kötést az Azure Web App alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="18137-110">The **New-AzureRmWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="18137-111">A parancsmag két módon hoz létre SSL-kötést:</span><span class="sxs-lookup"><span data-stu-id="18137-111">The cmdlet creates an SSL binding in two ways:</span></span> 

- <span data-ttu-id="18137-112">Egy webalkalmazást meglévő tanúsítványhoz köthet le.</span><span class="sxs-lookup"><span data-stu-id="18137-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="18137-113">Feltöltheti az új tanúsítványt, majd az új tanúsítványhoz rögzítheti a webalkalmazást.</span><span class="sxs-lookup"><span data-stu-id="18137-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>

<span data-ttu-id="18137-114">Attól függetlenül, hogy melyik módszert használja, a tanúsítványnak és a webalkalmazásnak ugyanahhoz az Azure-erőforrás csoporthoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="18137-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="18137-115">Ha van egy webalkalmazása az A erőforráscsoport-ban, és a webalkalmazást egy, a B erőforrás csoportba tartozó tanúsítványba szeretné kötni, az egyetlen mód arra, hogy a tanúsítvány másolatát feltöltse az A erőforrás csoportba.</span><span class="sxs-lookup"><span data-stu-id="18137-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A.</span></span>

<span data-ttu-id="18137-116">Új tanúsítvány feltöltése esetén tartsa szem előtt az alábbi követelményeket az Azure SSL-tanúsítványok esetében:</span><span class="sxs-lookup"><span data-stu-id="18137-116">If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 

- <span data-ttu-id="18137-117">A tanúsítványnak tartalmaznia kell egy titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="18137-117">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="18137-118">A tanúsítványnak a személyes adatok cseréje (PFX) formátumát kell használnia.</span><span class="sxs-lookup"><span data-stu-id="18137-118">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="18137-119">A tanúsítvány tulajdonosának nevének egyeznie kell a webalkalmazás eléréséhez használt tartománnyal.</span><span class="sxs-lookup"><span data-stu-id="18137-119">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="18137-120">A tanúsítványnak legalább 2048 bites titkosítást kell használnia.</span><span class="sxs-lookup"><span data-stu-id="18137-120">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="18137-121">Példák</span><span class="sxs-lookup"><span data-stu-id="18137-121">EXAMPLES</span></span>

### <span data-ttu-id="18137-122">1. példa: tanúsítvány kötése webalkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="18137-122">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="18137-123">Ez a parancs egy meglévő Azure-tanúsítványt (az ujjlenyomat-E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 tartalmazó tanúsítványt) köti össze a ContosoWebApp nevű webalkalmazással.</span><span class="sxs-lookup"><span data-stu-id="18137-123">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

## <span data-ttu-id="18137-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18137-124">PARAMETERS</span></span>

### <span data-ttu-id="18137-125">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="18137-125">-CertificateFilePath</span></span>
<span data-ttu-id="18137-126">A feltölteni kívánt tanúsítvány elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="18137-126">Specifies the file path for the certificate to be uploaded.</span></span>

<span data-ttu-id="18137-127">A *CertificateFilePath* paraméter csak akkor szükséges, ha a tanúsítvány még nincs feltöltve az Azure-ra.</span><span class="sxs-lookup"><span data-stu-id="18137-127">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18137-128">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="18137-128">-CertificatePassword</span></span>
<span data-ttu-id="18137-129">A tanúsítvány visszafejtési jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="18137-129">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18137-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18137-130">-DefaultProfile</span></span>
<span data-ttu-id="18137-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18137-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18137-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="18137-132">-Name</span></span>
<span data-ttu-id="18137-133">A webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18137-133">Specifies the name of the Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18137-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18137-134">-ResourceGroupName</span></span>
<span data-ttu-id="18137-135">Annak az erőforráscsoportnek a neve, amelyhez a tanúsítvány van rendelve.</span><span class="sxs-lookup"><span data-stu-id="18137-135">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="18137-136">A *ResourceGroupName* paraméter és a *WebApp* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="18137-136">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18137-137">-Slot</span><span class="sxs-lookup"><span data-stu-id="18137-137">-Slot</span></span>
<span data-ttu-id="18137-138">A webalkalmazás-telepítő bővítőhely nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18137-138">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="18137-139">A Get-AzureRMWebAppSlot parancsmaggal letölthet egy bővítőhelyet.</span><span class="sxs-lookup"><span data-stu-id="18137-139">You can use the Get-AzureRMWebAppSlot cmdlet to get a slot.</span></span>

<span data-ttu-id="18137-140">A telepítő bővítőhelyek segítségével a webes alkalmazások csak akkor érhetők el, ha az alkalmazások nem érhetők el az interneten keresztül.</span><span class="sxs-lookup"><span data-stu-id="18137-140">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="18137-141">Általában a módosításokat egy átmeneti webhelyre telepíti, érvényesíti ezeket a módosításokat, majd üzembe helyezi a termelés (internetről elérhető) webhelyre.</span><span class="sxs-lookup"><span data-stu-id="18137-141">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18137-142">-SslState</span><span class="sxs-lookup"><span data-stu-id="18137-142">-SslState</span></span>
<span data-ttu-id="18137-143">Megadja, hogy engedélyezve van-e a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="18137-143">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="18137-144">Állítsa a *SSLState* paramétert 1-re a tanúsítvány engedélyezéséhez, vagy állítsa a *SSLState* 0-ra a tanúsítvány letiltásához.</span><span class="sxs-lookup"><span data-stu-id="18137-144">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: SslState
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18137-145">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="18137-145">-Thumbprint</span></span>
<span data-ttu-id="18137-146">A tanúsítvány egyedi azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="18137-146">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: S2, S4
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18137-147">-WebApp</span><span class="sxs-lookup"><span data-stu-id="18137-147">-WebApp</span></span>
<span data-ttu-id="18137-148">Egy webalkalmazást ad meg.</span><span class="sxs-lookup"><span data-stu-id="18137-148">Specifies a Web App.</span></span>
<span data-ttu-id="18137-149">Ha egy webalkalmazást szeretne beszerezni, használja az Get-AzureRmWebApp parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="18137-149">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="18137-150">A *WebApp* paraméter nem használható ugyanabban a parancsban, mint a *ResourceGroupName* paraméter és/vagy a *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="18137-150">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18137-151">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="18137-151">-WebAppName</span></span>
<span data-ttu-id="18137-152">Annak a webalkalmazásnak a nevét adja meg, amelyhez az új SSL-kötést létrehozta.</span><span class="sxs-lookup"><span data-stu-id="18137-152">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>

<span data-ttu-id="18137-153">A *WebAppName* paraméter és a *WebApp* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="18137-153">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18137-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18137-154">CommonParameters</span></span>
<span data-ttu-id="18137-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18137-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18137-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18137-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18137-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18137-157">INPUTS</span></span>

### <span data-ttu-id="18137-158">Webhely</span><span class="sxs-lookup"><span data-stu-id="18137-158">Site</span></span>
<span data-ttu-id="18137-159">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="18137-159">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="18137-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18137-160">OUTPUTS</span></span>

## <span data-ttu-id="18137-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18137-161">NOTES</span></span>

## <span data-ttu-id="18137-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18137-162">RELATED LINKS</span></span>

[<span data-ttu-id="18137-163">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="18137-163">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="18137-164">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="18137-164">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="18137-165">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="18137-165">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="18137-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="18137-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


