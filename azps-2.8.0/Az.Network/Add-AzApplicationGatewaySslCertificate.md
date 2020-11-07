---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 7dddb6a5b38414d658cc405820327c0d6df43a6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837411"
---
# <span data-ttu-id="9624a-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9624a-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="9624a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9624a-102">SYNOPSIS</span></span>
<span data-ttu-id="9624a-103">SSL-tanúsítványt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="9624a-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="9624a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9624a-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9624a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9624a-105">DESCRIPTION</span></span>
<span data-ttu-id="9624a-106">Az **Add-AzApplicationGatewaySslCertificate** PARANCSMAG egy SSL-tanúsítványt ad az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="9624a-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="9624a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9624a-107">EXAMPLES</span></span>

### <span data-ttu-id="9624a-108">1. példa: SSL-tanúsítvány felvétele a pfx-ből egy alkalmazás-átjáróba.</span><span class="sxs-lookup"><span data-stu-id="9624a-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="9624a-109">Ez a parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja, majd hozzáadja a Cert01 nevű SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="9624a-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="9624a-110">2. példa: SSL-tanúsítvány felvétele a secretId (verziószám nélküli) titkos kulccsal az alkalmazás-átjáróba.</span><span class="sxs-lookup"><span data-stu-id="9624a-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="9624a-111">Adja meg a titkot, és hivatkozzon arra az `Add-AzApplicationGatewaySslCertificate` alkalmazásba, és írja be az alkalmazás-átjáróba a nevet `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="9624a-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="9624a-112">Megjegyzés: mivel itt a verzió-kevésbé secretId van megadva, az Application Gateway rendszeresen szinkronizálja a tanúsítványt a Tárcsázóval.</span><span class="sxs-lookup"><span data-stu-id="9624a-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="9624a-113">3. példa: SSL-tanúsítvány hozzáadása egy secretId (verziószámozással) egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="9624a-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="9624a-114">Adja meg a titkot, és hivatkozzon arra az `Add-AzApplicationGatewaySslCertificate` alkalmazásba, és írja be az alkalmazás-átjáróba a nevet `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="9624a-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="9624a-115">Megjegyzés: ha szükséges, hogy az alkalmazás átjárója szinkronizálja a tanúsítványt, kérjük, adja meg a verziószám nélküli secretId.</span><span class="sxs-lookup"><span data-stu-id="9624a-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="9624a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9624a-116">PARAMETERS</span></span>

### <span data-ttu-id="9624a-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9624a-117">-ApplicationGateway</span></span>
<span data-ttu-id="9624a-118">Annak az alkalmazás-átjárónak a nevét adja meg, amelyre a parancsmag hozzáadja az SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="9624a-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="9624a-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9624a-119">-CertificateFile</span></span>
<span data-ttu-id="9624a-120">A parancsmag által hozzáadott SSL-tanúsítvány. pfx fájlja.</span><span class="sxs-lookup"><span data-stu-id="9624a-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9624a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9624a-121">-DefaultProfile</span></span>
<span data-ttu-id="9624a-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9624a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9624a-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="9624a-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="9624a-124">A SecretId (URI) a boltozat titkát.</span><span class="sxs-lookup"><span data-stu-id="9624a-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="9624a-125">Ezt a lehetőséget akkor használja, ha a titok egy bizonyos verzióját kell használnia.</span><span class="sxs-lookup"><span data-stu-id="9624a-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="9624a-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9624a-126">-Name</span></span>
<span data-ttu-id="9624a-127">Annak az SSL-tanúsítványnak a neve, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="9624a-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9624a-128">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="9624a-128">-Password</span></span>
<span data-ttu-id="9624a-129">Annak az SSL-tanúsítványnak a jelszava, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="9624a-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9624a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9624a-130">CommonParameters</span></span>
<span data-ttu-id="9624a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9624a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9624a-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9624a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9624a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9624a-133">INPUTS</span></span>

### <span data-ttu-id="9624a-134">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9624a-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9624a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9624a-135">OUTPUTS</span></span>

### <span data-ttu-id="9624a-136">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9624a-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9624a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9624a-137">NOTES</span></span>

## <span data-ttu-id="9624a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9624a-138">RELATED LINKS</span></span>

[<span data-ttu-id="9624a-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9624a-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9624a-140">Új – AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9624a-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9624a-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9624a-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9624a-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9624a-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


