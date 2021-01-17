---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 31d9c5d5c627f4d3451c47584b09760655e77342
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379300"
---
# <span data-ttu-id="c7c6d-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c7c6d-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c7c6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c6d-103">Ssl-tanúsítványt hoz létre egy Azure-alkalmazás átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="c7c6d-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="c7c6d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c7c6d-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7c6d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c7c6d-105">DESCRIPTION</span></span>
<span data-ttu-id="c7c6d-106">A **New-AzApplicationGatewaySslCertificate** parancsmag ssl-tanúsítványt hoz létre egy Azure-alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="c7c6d-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="c7c6d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c7c6d-107">EXAMPLES</span></span>

### <span data-ttu-id="c7c6d-108">1. példa: Hozzon létre egy SSL-tanúsítványt egy Azure-alkalmazás átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="c7c6d-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="c7c6d-109">Ez a parancs létrehoz egy Cert01 nevű SSL-tanúsítványt az alapértelmezett alkalmazás-átjáróhoz, és az eredményt a következő nevű változóban $Cert.</span><span class="sxs-lookup"><span data-stu-id="c7c6d-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="c7c6d-110">2. példa: SSL-tanúsítvány létrehozása a KeyVault Secret (version-less secretId) segítségével, és hozzáadás egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="c7c6d-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="c7c6d-111">Szerezze be a titkos tanúsítványt, és hozzon létre egy SSL-tanúsítványt a `New-AzApplicationGatewaySslCertificate` segítségével.</span><span class="sxs-lookup"><span data-stu-id="c7c6d-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="c7c6d-112">Megjegyzés: Az itt megadott verziószámú titkos kulcsazonosító miatt az Application Gateway rendszeres időközönként szinkronizálja a tanúsítványt a KeyVaulttal.</span><span class="sxs-lookup"><span data-stu-id="c7c6d-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="c7c6d-113">3. példa: Hozzon létre egy SSL-tanúsítványt a KeyVault Secret segítségével, és vegyen fel egy alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="c7c6d-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="c7c6d-114">Szerezze be a titkos tanúsítványt, és hozzon létre egy SSL-tanúsítványt a `New-AzApplicationGatewaySslCertificate` segítségével.</span><span class="sxs-lookup"><span data-stu-id="c7c6d-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="c7c6d-115">Megjegyzés: Ha szükséges, hogy az Application Gateway szinkronizálja a tanúsítványt a KeyVaulttal, kérjük, adja meg a verziószámtól különböző titkosazonosítót.</span><span class="sxs-lookup"><span data-stu-id="c7c6d-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="c7c6d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7c6d-116">PARAMETERS</span></span>

### <span data-ttu-id="c7c6d-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c7c6d-117">-CertificateFile</span></span>
<span data-ttu-id="c7c6d-118">A parancsmag által létrehozott SSL-tanúsítvány .pfx fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7c6d-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c7c6d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c6d-119">-DefaultProfile</span></span>
<span data-ttu-id="c7c6d-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7c6d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7c6d-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="c7c6d-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="c7c6d-122">A KeyVault-titkos kulcs titkos azonosítóját (uri).</span><span class="sxs-lookup"><span data-stu-id="c7c6d-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="c7c6d-123">Akkor használja ezt a beállítást, ha a titkos adatok adott verzióját kell használnia.</span><span class="sxs-lookup"><span data-stu-id="c7c6d-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="c7c6d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c7c6d-124">-Name</span></span>
<span data-ttu-id="c7c6d-125">A parancsmag által létrehozott SSL-tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="c7c6d-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c7c6d-126">-Password</span><span class="sxs-lookup"><span data-stu-id="c7c6d-126">-Password</span></span>
<span data-ttu-id="c7c6d-127">A parancsmag által létrehozott SSL-jelszó megadása.</span><span class="sxs-lookup"><span data-stu-id="c7c6d-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c7c6d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c6d-128">CommonParameters</span></span>
<span data-ttu-id="c7c6d-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7c6d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c6d-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7c6d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c6d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7c6d-131">INPUTS</span></span>

### <span data-ttu-id="c7c6d-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="c7c6d-132">None</span></span>

## <span data-ttu-id="c7c6d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7c6d-133">OUTPUTS</span></span>

### <span data-ttu-id="c7c6d-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c7c6d-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c7c6d-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c7c6d-135">NOTES</span></span>

## <span data-ttu-id="c7c6d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7c6d-136">RELATED LINKS</span></span>

[<span data-ttu-id="c7c6d-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c7c6d-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c7c6d-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c7c6d-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c7c6d-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c7c6d-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c7c6d-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c7c6d-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


