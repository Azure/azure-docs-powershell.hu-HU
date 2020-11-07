---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/stop-AzKeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: e1a4efc9709b7168e5de46ea0e19e2059f15243c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843846"
---
# <span data-ttu-id="0a822-101">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="0a822-101">Stop-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="0a822-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a822-102">SYNOPSIS</span></span>
<span data-ttu-id="0a822-103">A Key Vault-ban visszavonja a tanúsítvány működését.</span><span class="sxs-lookup"><span data-stu-id="0a822-103">Cancels a certificate operation in key vault.</span></span>

## <span data-ttu-id="0a822-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a822-104">SYNTAX</span></span>

```
Stop-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a822-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a822-105">DESCRIPTION</span></span>
<span data-ttu-id="0a822-106">A **stop-AzKeyVaultCertificateOperation** parancsmag az Azure Key Vault szolgáltatásban visszavonja a tanúsítvány működését.</span><span class="sxs-lookup"><span data-stu-id="0a822-106">The **Stop-AzKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="0a822-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0a822-107">EXAMPLES</span></span>

### <span data-ttu-id="0a822-108">Példa 1: a tanúsítvány lemondása</span><span class="sxs-lookup"><span data-stu-id="0a822-108">Example 1: Cancel a certificate operation</span></span>
```
PS C:\>Stop-AzKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force
Status                    : inProgress
CancellationRequested     : True
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCVr6EVwsd48qDVORsF4V4w4N1aQCUirFW7b+kwoTvSOL4SfMiWcPmno0uxmQQoh
                            gz157bC3sKFLyBUsGCmS4i7uWkBOSEpCh8L3FKU4XMqRROlUM9AqswzB0e1sURCqevEJA80xFpfTgkeqpm44m4jr6p7gu+h1PBf9Dt7b43Gybde5DUlGrrOiTkOIAF0eU2iNVeHOapoj8m1XHmzO1BARs
                            oa0pSDxO/aMgeuq/QPkWG64Iiw55U20byKZ86u3Y4g192HsPwsrHkf9ZSYR2M9BYM3YGoT/dkCmAtP4LQAsOwf1+S0a/TwRtrnoOHbPFI6HYSY3TY1iqzZ9xItfgalAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAjxUX5PGhri9qJTxSleGEbMVkxhhn3nuPUgxujEzrcQVr
                            fZAACJHbOnga/QYwpxumKWnkX9YdWxb58PPn+nLV2gYP3eYEyJ4DR9XDcKpoQxZahUdqD3JZXhWPIcN05tw9Fuq8ziw94BjLZW3h3iDamqkBnysJYW58FBp1H8Ejqk0Iynbo0V223Innq/7QB2fVwe3ZJ
                            JecT8YxHJjVQ5psdDpEWgLUG/DFiAPHdwupI7JjvtvQmT3AotL0x5GNx2bWNH5hHIXsX4bnbxZgNQnTB2w3tQ3QeuKt8fUx2S0xtxPllaCUul6efa84TNqdMcMfyxCarIwDP6qdhS+CDU1uUA==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="0a822-109">Ez a parancs lemondja a TestCert02-tanúsítvány működését.</span><span class="sxs-lookup"><span data-stu-id="0a822-109">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="0a822-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a822-110">PARAMETERS</span></span>

### <span data-ttu-id="0a822-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a822-111">-DefaultProfile</span></span>
<span data-ttu-id="0a822-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0a822-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a822-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0a822-113">-Force</span></span>
<span data-ttu-id="0a822-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0a822-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a822-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0a822-115">-Name</span></span>
<span data-ttu-id="0a822-116">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a822-116">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a822-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0a822-117">-VaultName</span></span>
<span data-ttu-id="0a822-118">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a822-118">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a822-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0a822-119">-Confirm</span></span>
<span data-ttu-id="0a822-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0a822-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a822-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a822-121">-WhatIf</span></span>
<span data-ttu-id="0a822-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0a822-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a822-123">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0a822-123">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a822-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a822-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a822-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a822-125">CommonParameters</span></span>
<span data-ttu-id="0a822-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a822-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a822-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a822-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a822-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a822-128">INPUTS</span></span>

### <span data-ttu-id="0a822-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="0a822-129">None</span></span>
<span data-ttu-id="0a822-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0a822-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0a822-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a822-131">OUTPUTS</span></span>

### <span data-ttu-id="0a822-132">Microsoft. Azure. Command. KeyVaultCertificateOperation. models.</span><span class="sxs-lookup"><span data-stu-id="0a822-132">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="0a822-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a822-133">NOTES</span></span>

## <span data-ttu-id="0a822-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a822-134">RELATED LINKS</span></span>

[<span data-ttu-id="0a822-135">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="0a822-135">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="0a822-136">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="0a822-136">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

