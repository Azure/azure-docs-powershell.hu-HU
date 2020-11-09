---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: a5a1533038f8e11a30dd3fdeedd590b8186597b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302755"
---
# <span data-ttu-id="7c99f-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7c99f-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="7c99f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c99f-102">SYNOPSIS</span></span>
<span data-ttu-id="7c99f-103">Az Azure Application Gateway rendszerhez létrehoz egy SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="7c99f-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="7c99f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c99f-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c99f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c99f-105">DESCRIPTION</span></span>
<span data-ttu-id="7c99f-106">A **New-AzApplicationGatewaySslCertificate** parancsmag létrehoz egy SSL-tanúsítványt egy Azure Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="7c99f-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="7c99f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7c99f-107">EXAMPLES</span></span>

### <span data-ttu-id="7c99f-108">1. példa: SSL-tanúsítvány létrehozása Azure Application Gateway rendszerhez</span><span class="sxs-lookup"><span data-stu-id="7c99f-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="7c99f-109">Ez a parancs létrehoz egy Cert01 nevű SSL-tanúsítványt az alapértelmezett alkalmazás-átjáróhoz, és az eredményt az $Cert nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7c99f-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="7c99f-110">2. példa: hozzon létre egy SSL-tanúsítványt a secretId (verziószám nélküli) és a Hozzáadás egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7c99f-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="7c99f-111">Hozza létre a titkot, és hozzon létre egy SSL-tanúsítványt a használatával `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="7c99f-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="7c99f-112">Megjegyzés: mivel itt a verzió-kevésbé secretId van megadva, az Application Gateway rendszeresen szinkronizálja a tanúsítványt a Tárcsázóval.</span><span class="sxs-lookup"><span data-stu-id="7c99f-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="7c99f-113">3. példa: hozzon létre egy SSL-tanúsítványt, és adjon hozzá egy alkalmazás-átjárót a kulccsal.</span><span class="sxs-lookup"><span data-stu-id="7c99f-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="7c99f-114">Hozza létre a titkot, és hozzon létre egy SSL-tanúsítványt a használatával `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="7c99f-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="7c99f-115">Megjegyzés: ha szükséges, hogy az alkalmazás átjárója szinkronizálja a tanúsítványt, kérjük, adja meg a verziószám nélküli secretId.</span><span class="sxs-lookup"><span data-stu-id="7c99f-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="7c99f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c99f-116">PARAMETERS</span></span>

### <span data-ttu-id="7c99f-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7c99f-117">-CertificateFile</span></span>
<span data-ttu-id="7c99f-118">Annak az SSL-tanúsítványnak a. PFX fájljának elérési útját adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7c99f-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7c99f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c99f-119">-DefaultProfile</span></span>
<span data-ttu-id="7c99f-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c99f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c99f-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="7c99f-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="7c99f-122">A SecretId (URI) a boltozat titkát.</span><span class="sxs-lookup"><span data-stu-id="7c99f-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="7c99f-123">Ezt a lehetőséget akkor használja, ha a titok egy bizonyos verzióját kell használnia.</span><span class="sxs-lookup"><span data-stu-id="7c99f-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="7c99f-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7c99f-124">-Name</span></span>
<span data-ttu-id="7c99f-125">Annak az SSL-tanúsítványnak a neve, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7c99f-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7c99f-126">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="7c99f-126">-Password</span></span>
<span data-ttu-id="7c99f-127">Annak az SSL-nek a jelszava, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7c99f-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7c99f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c99f-128">CommonParameters</span></span>
<span data-ttu-id="7c99f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c99f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c99f-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c99f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c99f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c99f-131">INPUTS</span></span>

### <span data-ttu-id="7c99f-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="7c99f-132">None</span></span>

## <span data-ttu-id="7c99f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c99f-133">OUTPUTS</span></span>

### <span data-ttu-id="7c99f-134">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7c99f-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="7c99f-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c99f-135">NOTES</span></span>

## <span data-ttu-id="7c99f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c99f-136">RELATED LINKS</span></span>

[<span data-ttu-id="7c99f-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7c99f-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7c99f-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7c99f-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7c99f-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7c99f-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="7c99f-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7c99f-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


