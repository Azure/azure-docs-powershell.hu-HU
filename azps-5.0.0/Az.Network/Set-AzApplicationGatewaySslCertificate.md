---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 0fa72c48693335dd3df6ab3c1cf8040c5343cc84
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301781"
---
# <span data-ttu-id="44557-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="44557-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="44557-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="44557-102">SYNOPSIS</span></span>
<span data-ttu-id="44557-103">Egy alkalmazás-átjáró SSL-tanúsítványának frissítése</span><span class="sxs-lookup"><span data-stu-id="44557-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="44557-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="44557-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44557-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="44557-105">DESCRIPTION</span></span>
<span data-ttu-id="44557-106">A **set-AzApplicationGatewaySslCertificate** parancsmag az alkalmazás-ÁTJÁRÓk SSL-tanúsítványát frissíti.</span><span class="sxs-lookup"><span data-stu-id="44557-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="44557-107">Példák</span><span class="sxs-lookup"><span data-stu-id="44557-107">EXAMPLES</span></span>

### <span data-ttu-id="44557-108">Példa 1: meglévő SSL-tanúsítvány frissítése az alkalmazás-átjárón</span><span class="sxs-lookup"><span data-stu-id="44557-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="44557-109">Frissítsen egy meglévő SSL-tanúsítványt a ApplicationGateway01 nevű alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="44557-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="44557-110">2. példa: meglévő SSL-tanúsítvány frissítése a "secretId" (verziószám nélküli) kulccsal az Application Gatewayben</span><span class="sxs-lookup"><span data-stu-id="44557-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="44557-111">A titka és a meglévő SSL-tanúsítvány frissítése a használatával `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="44557-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="44557-112">3. példa: meglévő SSL-tanúsítvány frissítése az Application Gateway segítségével</span><span class="sxs-lookup"><span data-stu-id="44557-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="44557-113">A titka és a meglévő SSL-tanúsítvány frissítése a használatával `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="44557-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="44557-114">Megjegyzés: ha szükséges, hogy az alkalmazás átjárója szinkronizálja a tanúsítványt, kérjük, adja meg a verziószám nélküli secretId.</span><span class="sxs-lookup"><span data-stu-id="44557-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="44557-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="44557-115">PARAMETERS</span></span>

### <span data-ttu-id="44557-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="44557-116">-ApplicationGateway</span></span>
<span data-ttu-id="44557-117">Annak az alkalmazásnak az átjáróját adja meg, amelyhez a Secure Socket Layer (SSL) tanúsítvány van társítva.</span><span class="sxs-lookup"><span data-stu-id="44557-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="44557-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="44557-118">-CertificateFile</span></span>
<span data-ttu-id="44557-119">Az SSL-tanúsítvány elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="44557-119">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="44557-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44557-120">-DefaultProfile</span></span>
<span data-ttu-id="44557-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44557-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44557-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="44557-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="44557-123">A SecretId (URI) a boltozat titkát.</span><span class="sxs-lookup"><span data-stu-id="44557-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="44557-124">Ezt a lehetőséget akkor használja, ha a titok egy bizonyos verzióját kell használnia.</span><span class="sxs-lookup"><span data-stu-id="44557-124">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="44557-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="44557-125">-Name</span></span>
<span data-ttu-id="44557-126">Az SSL-tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="44557-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="44557-127">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="44557-127">-Password</span></span>
<span data-ttu-id="44557-128">Az SSL-tanúsítvány jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="44557-128">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="44557-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44557-129">CommonParameters</span></span>
<span data-ttu-id="44557-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="44557-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44557-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44557-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44557-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="44557-132">INPUTS</span></span>

### <span data-ttu-id="44557-133">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="44557-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="44557-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44557-134">OUTPUTS</span></span>

### <span data-ttu-id="44557-135">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="44557-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="44557-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="44557-136">NOTES</span></span>

## <span data-ttu-id="44557-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44557-137">RELATED LINKS</span></span>

[<span data-ttu-id="44557-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="44557-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="44557-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="44557-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="44557-140">Új – AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="44557-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="44557-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="44557-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


