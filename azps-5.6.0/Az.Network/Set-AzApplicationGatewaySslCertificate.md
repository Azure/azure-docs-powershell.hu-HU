---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: f1b944e2673c9682a0194c4996fa4d2b34fae97b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918690"
---
# <span data-ttu-id="87c18-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="87c18-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="87c18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87c18-102">SYNOPSIS</span></span>
<span data-ttu-id="87c18-103">Egy alkalmazás-átjáró SSL-tanúsítványát frissíti.</span><span class="sxs-lookup"><span data-stu-id="87c18-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="87c18-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="87c18-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87c18-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="87c18-105">DESCRIPTION</span></span>
<span data-ttu-id="87c18-106">A **Set-AzApplicationGatewaySslCertificate** parancsmag frissíti egy alkalmazás-átjáró SSL-tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="87c18-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="87c18-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="87c18-107">EXAMPLES</span></span>

### <span data-ttu-id="87c18-108">1. példa: Meglévő SSL-tanúsítvány frissítése az alkalmazás-átjárón</span><span class="sxs-lookup"><span data-stu-id="87c18-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="87c18-109">Frissítse az ApplicationGateway01 nevű alkalmazás-átjáró meglévő SSL-tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="87c18-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="87c18-110">2. példa: Meglévő SSL-tanúsítvány frissítése a KeyVault Secret (version-less secretId) használatával az Alkalmazás átjárón</span><span class="sxs-lookup"><span data-stu-id="87c18-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="87c18-111">Szerezze be a titkos tanúsítványt, és frissítsen egy meglévő SSL-tanúsítványt. `Set-AzApplicationGatewaySslCertificate`</span><span class="sxs-lookup"><span data-stu-id="87c18-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="87c18-112">3. példa: Meglévő SSL-tanúsítvány frissítése a KeyVault-titkosítás használatával az alkalmazásátjárón</span><span class="sxs-lookup"><span data-stu-id="87c18-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="87c18-113">Szerezze be a titkos tanúsítványt, és frissítsen egy meglévő SSL-tanúsítványt. `Set-AzApplicationGatewaySslCertificate`</span><span class="sxs-lookup"><span data-stu-id="87c18-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="87c18-114">Megjegyzés: Ha szükséges, hogy az Application Gateway szinkronizálja a tanúsítványt a KeyVaulttal, kérjük, adja meg a verziószámtól különböző titkosazonosítót.</span><span class="sxs-lookup"><span data-stu-id="87c18-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="87c18-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87c18-115">PARAMETERS</span></span>

### <span data-ttu-id="87c18-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="87c18-116">-ApplicationGateway</span></span>
<span data-ttu-id="87c18-117">Azt az alkalmazás-átjárót adja meg, amelyhez az SSL-tanúsítvány társítva van.</span><span class="sxs-lookup"><span data-stu-id="87c18-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87c18-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="87c18-118">-CertificateFile</span></span>
<span data-ttu-id="87c18-119">Az SSL-tanúsítvány elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="87c18-119">Specifies the path of the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c18-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c18-120">-DefaultProfile</span></span>
<span data-ttu-id="87c18-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87c18-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87c18-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="87c18-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="87c18-123">A KeyVault-titkos kulcs titkos azonosítóját (uri).</span><span class="sxs-lookup"><span data-stu-id="87c18-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="87c18-124">Akkor használja ezt a beállítást, ha a titkos adatok adott verzióját kell használnia.</span><span class="sxs-lookup"><span data-stu-id="87c18-124">Use this option when a specific version of secret needs to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c18-125">-Name</span><span class="sxs-lookup"><span data-stu-id="87c18-125">-Name</span></span>
<span data-ttu-id="87c18-126">Az SSL-tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87c18-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="87c18-127">-Password</span><span class="sxs-lookup"><span data-stu-id="87c18-127">-Password</span></span>
<span data-ttu-id="87c18-128">Megadja az SSL-tanúsítvány jelszavát.</span><span class="sxs-lookup"><span data-stu-id="87c18-128">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c18-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c18-129">CommonParameters</span></span>
<span data-ttu-id="87c18-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87c18-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c18-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87c18-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c18-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87c18-132">INPUTS</span></span>

### <span data-ttu-id="87c18-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="87c18-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="87c18-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87c18-134">OUTPUTS</span></span>

### <span data-ttu-id="87c18-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="87c18-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="87c18-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="87c18-136">NOTES</span></span>

## <span data-ttu-id="87c18-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87c18-137">RELATED LINKS</span></span>

[<span data-ttu-id="87c18-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="87c18-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="87c18-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="87c18-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="87c18-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="87c18-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="87c18-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="87c18-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


