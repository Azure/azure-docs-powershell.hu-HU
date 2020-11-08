---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 89299823-3382-402D-9458-519466748051
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificate.md
ms.openlocfilehash: 194ec896ea8b56b8ae823eb0d262438e01977384
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024751"
---
# <span data-ttu-id="d018b-101">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d018b-101">Add-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="d018b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d018b-102">SYNOPSIS</span></span>
<span data-ttu-id="d018b-103">Tanúsítványt ad hozzá egy kulcs boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="d018b-103">Adds a certificate to a key vault.</span></span>

## <span data-ttu-id="d018b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d018b-104">SYNTAX</span></span>

```
Add-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificatePolicy] <PSKeyVaultCertificatePolicy> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d018b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d018b-105">DESCRIPTION</span></span>
<span data-ttu-id="d018b-106">Az **Add-AzKeyVaultCertificate** parancsmag a tanúsítványok beadásának folyamatát az Azure Key Vault-ban indítja el.</span><span class="sxs-lookup"><span data-stu-id="d018b-106">The **Add-AzKeyVaultCertificate** cmdlet starts the process of enrolling for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="d018b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d018b-107">EXAMPLES</span></span>

### <span data-ttu-id="d018b-108">1. példa: tanúsítvány hozzáadása</span><span class="sxs-lookup"><span data-stu-id="d018b-108">Example 1: Add a certificate</span></span>
```powershell
PS C:\> $Policy = New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
PS C:\> Add-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -CertificatePolicy $Policy

Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : 

PS C:\> Get-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : completed
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : 

PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"

Name        : testCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="d018b-109">Az első parancs a New-AzKeyVaultCertificatePolicy parancsmagot használja a tanúsítványok házirendjének létrehozásához, majd a $Policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d018b-109">The first command uses the New-AzKeyVaultCertificatePolicy cmdlet to create a certificate policy, and then stores it in the $Policy variable.</span></span>
<span data-ttu-id="d018b-110">A második parancs az **Add-AzKeyVaultCertificate** használatával indítja el a folyamatot a tanúsítvány létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="d018b-110">The second command uses **Add-AzKeyVaultCertificate** to start the process to create a certificate.</span></span>
<span data-ttu-id="d018b-111">A harmadik parancs az Get-AzKeyVaultCertificateOperation parancsmag használatával kérdezi le a műveletet annak ellenőrzéséhez, hogy befejeződött-e.</span><span class="sxs-lookup"><span data-stu-id="d018b-111">The third command uses the Get-AzKeyVaultCertificateOperation cmdlet to poll the operation to verify that it's complete.</span></span>
<span data-ttu-id="d018b-112">A végleges parancs az Get-AzKeyVaultCertificate parancsmagot használja a tanúsítvány beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="d018b-112">The final command uses the Get-AzKeyVaultCertificate cmdlet to get the certificate.</span></span>

## <span data-ttu-id="d018b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d018b-113">PARAMETERS</span></span>

### <span data-ttu-id="d018b-114">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d018b-114">-CertificatePolicy</span></span>
<span data-ttu-id="d018b-115">Egy **KeyVaultCertificatePolicy** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d018b-115">Specifies a **KeyVaultCertificatePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d018b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d018b-116">-DefaultProfile</span></span>
<span data-ttu-id="d018b-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d018b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d018b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d018b-118">-Name</span></span>
<span data-ttu-id="d018b-119">A hozzáadni kívánt tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d018b-119">Specifies the name of the certificate to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d018b-120">-Címke</span><span class="sxs-lookup"><span data-stu-id="d018b-120">-Tag</span></span>
<span data-ttu-id="d018b-121">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="d018b-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d018b-122">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="d018b-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d018b-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d018b-123">-VaultName</span></span>
<span data-ttu-id="d018b-124">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d018b-124">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d018b-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d018b-125">-Confirm</span></span>
<span data-ttu-id="d018b-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d018b-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d018b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d018b-127">-WhatIf</span></span>
<span data-ttu-id="d018b-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d018b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d018b-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d018b-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d018b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d018b-130">CommonParameters</span></span>
<span data-ttu-id="d018b-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d018b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d018b-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d018b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d018b-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d018b-133">INPUTS</span></span>

### <span data-ttu-id="d018b-134">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="d018b-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="d018b-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d018b-135">OUTPUTS</span></span>

### <span data-ttu-id="d018b-136">Microsoft. Azure. Command. PSKeyVaultCertificateOperation. models.</span><span class="sxs-lookup"><span data-stu-id="d018b-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="d018b-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d018b-137">NOTES</span></span>

## <span data-ttu-id="d018b-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d018b-138">RELATED LINKS</span></span>

[<span data-ttu-id="d018b-139">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d018b-139">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="d018b-140">Importálás – AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d018b-140">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="d018b-141">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d018b-141">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)
