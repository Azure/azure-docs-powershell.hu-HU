---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 1dd4285b75f8c1c067f15be34a334d4d48fb4f7e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479946"
---
# <span data-ttu-id="00e01-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="00e01-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="00e01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00e01-102">SYNOPSIS</span></span>
<span data-ttu-id="00e01-103">Egy alkalmazás-átjáró SSL-tanúsítványát frissíti.</span><span class="sxs-lookup"><span data-stu-id="00e01-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="00e01-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="00e01-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00e01-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="00e01-105">DESCRIPTION</span></span>
<span data-ttu-id="00e01-106">A **Set-AzApplicationGatewaySslCertificate** parancsmag egy alkalmazás-átjáró SSL-tanúsítványát frissíti.</span><span class="sxs-lookup"><span data-stu-id="00e01-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="00e01-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="00e01-107">EXAMPLES</span></span>

### <span data-ttu-id="00e01-108">1. példa: Meglévő SSL-tanúsítvány frissítése az alkalmazás-átjárón</span><span class="sxs-lookup"><span data-stu-id="00e01-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="00e01-109">Frissítsen egy meglévő SSL-tanúsítványt az ApplicationGateway01 nevű alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="00e01-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="00e01-110">2. példa: Meglévő SSL-tanúsítvány frissítése a KeyVault Secret (version-less secretId) használatával az Alkalmazás átjárón</span><span class="sxs-lookup"><span data-stu-id="00e01-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="00e01-111">Szerezze be a titkos tanúsítványt, és frissítsen egy meglévő SSL-tanúsítványt. `Set-AzApplicationGatewaySslCertificate`</span><span class="sxs-lookup"><span data-stu-id="00e01-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="00e01-112">3. példa: Meglévő SSL-tanúsítvány frissítése a KeyVault Secret használatával az alkalmazásátjárón</span><span class="sxs-lookup"><span data-stu-id="00e01-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="00e01-113">Szerezze be a titkos tanúsítványt, és frissítsen egy meglévő SSL-tanúsítványt. `Set-AzApplicationGatewaySslCertificate`</span><span class="sxs-lookup"><span data-stu-id="00e01-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="00e01-114">Megjegyzés: Ha szükséges, hogy az Application Gateway szinkronizálja a tanúsítványt a KeyVaulttal, kérjük, adja meg a verziószámtól különböző titkosazonosítót.</span><span class="sxs-lookup"><span data-stu-id="00e01-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="00e01-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00e01-115">PARAMETERS</span></span>

### <span data-ttu-id="00e01-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00e01-116">-ApplicationGateway</span></span>
<span data-ttu-id="00e01-117">Azt az alkalmazás-átjárót adja meg, amelyhez az SSL-tanúsítvány társítva van.</span><span class="sxs-lookup"><span data-stu-id="00e01-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="00e01-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="00e01-118">-CertificateFile</span></span>
<span data-ttu-id="00e01-119">Az SSL-tanúsítvány elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="00e01-119">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="00e01-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00e01-120">-DefaultProfile</span></span>
<span data-ttu-id="00e01-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00e01-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00e01-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="00e01-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="00e01-123">A KeyVault-titkos kulcs titkos azonosítóját (uri).</span><span class="sxs-lookup"><span data-stu-id="00e01-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="00e01-124">Akkor használja ezt a beállítást, ha a titkos adatok adott verzióját kell használnia.</span><span class="sxs-lookup"><span data-stu-id="00e01-124">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="00e01-125">-Name</span><span class="sxs-lookup"><span data-stu-id="00e01-125">-Name</span></span>
<span data-ttu-id="00e01-126">Az SSL-tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="00e01-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="00e01-127">-Password</span><span class="sxs-lookup"><span data-stu-id="00e01-127">-Password</span></span>
<span data-ttu-id="00e01-128">Megadja az SSL-tanúsítvány jelszavát.</span><span class="sxs-lookup"><span data-stu-id="00e01-128">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="00e01-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00e01-129">CommonParameters</span></span>
<span data-ttu-id="00e01-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00e01-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00e01-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00e01-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00e01-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00e01-132">INPUTS</span></span>

### <span data-ttu-id="00e01-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00e01-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="00e01-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00e01-134">OUTPUTS</span></span>

### <span data-ttu-id="00e01-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00e01-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="00e01-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="00e01-136">NOTES</span></span>

## <span data-ttu-id="00e01-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00e01-137">RELATED LINKS</span></span>

[<span data-ttu-id="00e01-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="00e01-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="00e01-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="00e01-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="00e01-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="00e01-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="00e01-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="00e01-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


