---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 6939f26dc06e0aa5ed56d3e905d30960094e8961
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334614"
---
# <span data-ttu-id="79e9e-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="79e9e-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="79e9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="79e9e-103">SSL-tanúsítványt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="79e9e-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="79e9e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79e9e-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79e9e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79e9e-105">DESCRIPTION</span></span>
<span data-ttu-id="79e9e-106">Az **Add-AzApplicationGatewaySslCertificate parancsmag** hozzáad egy SSL-tanúsítványt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="79e9e-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="79e9e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79e9e-107">EXAMPLES</span></span>

### <span data-ttu-id="79e9e-108">1. példa: SSL-tanúsítvány hozzáadása pfx használatával egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="79e9e-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="79e9e-109">Ez a parancs egy ApplicationGateway01 nevű alkalmazás-átjárót kap, majd hozzáad egy Cert01 nevű SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="79e9e-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="79e9e-110">2. példa: SSL-tanúsítvány hozzáadása a KeyVault Secret (version-less secretId) segítségével egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="79e9e-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.SecretId.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="79e9e-111">Szerezze be a titkos referenciát, és vegye fel az alkalmazás átjárójára `Add-AzApplicationGatewaySslCertificate` `Cert01` névvel.</span><span class="sxs-lookup"><span data-stu-id="79e9e-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="79e9e-112">Megjegyzés: Az itt megadott verziószámú titkos kulcsazonosító miatt az Application Gateway rendszeres időközönként szinkronizálja a tanúsítványt a KeyVaulttal.</span><span class="sxs-lookup"><span data-stu-id="79e9e-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="79e9e-113">3. példa: SSL-tanúsítvány hozzáadása a KeyVault Secret (versioned secretId) használatával egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="79e9e-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="79e9e-114">Szerezze be a titkos referenciát, és vegye fel az alkalmazás átjárójára `Add-AzApplicationGatewaySslCertificate` `Cert01` névvel.</span><span class="sxs-lookup"><span data-stu-id="79e9e-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="79e9e-115">Megjegyzés: Ha szükséges, hogy az Application Gateway szinkronizálja a tanúsítványt a KeyVaulttal, kérjük, adja meg a verziószámtól különböző titkosazonosítót.</span><span class="sxs-lookup"><span data-stu-id="79e9e-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="79e9e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79e9e-116">PARAMETERS</span></span>

### <span data-ttu-id="79e9e-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79e9e-117">-ApplicationGateway</span></span>
<span data-ttu-id="79e9e-118">Megadja annak az alkalmazás-átjárónak a nevét, amelyhez ez a parancsmag SSL-tanúsítványt ad.</span><span class="sxs-lookup"><span data-stu-id="79e9e-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="79e9e-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="79e9e-119">-CertificateFile</span></span>
<span data-ttu-id="79e9e-120">A parancsmag által hozzáadt SSL-tanúsítvány .pfx fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="79e9e-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="79e9e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e9e-121">-DefaultProfile</span></span>
<span data-ttu-id="79e9e-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79e9e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79e9e-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="79e9e-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="79e9e-124">A KeyVault-titkos kulcs titkos azonosítóját (uri).</span><span class="sxs-lookup"><span data-stu-id="79e9e-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="79e9e-125">Akkor használja ezt a beállítást, ha a titkos adatok adott verzióját kell használnia.</span><span class="sxs-lookup"><span data-stu-id="79e9e-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="79e9e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="79e9e-126">-Name</span></span>
<span data-ttu-id="79e9e-127">A parancsmag által megadott SSL-tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="79e9e-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="79e9e-128">-Password</span><span class="sxs-lookup"><span data-stu-id="79e9e-128">-Password</span></span>
<span data-ttu-id="79e9e-129">A parancsmag által megadott SSL-tanúsítvány jelszava.</span><span class="sxs-lookup"><span data-stu-id="79e9e-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="79e9e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e9e-130">CommonParameters</span></span>
<span data-ttu-id="79e9e-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79e9e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e9e-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79e9e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e9e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79e9e-133">INPUTS</span></span>

### <span data-ttu-id="79e9e-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79e9e-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79e9e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79e9e-135">OUTPUTS</span></span>

### <span data-ttu-id="79e9e-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79e9e-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79e9e-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79e9e-137">NOTES</span></span>

## <span data-ttu-id="79e9e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79e9e-138">RELATED LINKS</span></span>

[<span data-ttu-id="79e9e-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="79e9e-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="79e9e-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="79e9e-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="79e9e-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="79e9e-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="79e9e-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="79e9e-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


