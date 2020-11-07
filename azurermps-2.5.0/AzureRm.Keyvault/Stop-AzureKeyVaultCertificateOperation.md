---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/stop-azurekeyvaultcertificateoperation
schema: 2.0.0
ms.openlocfilehash: 7018dc8d6951be8d1a08f4f1d1f5d615810dafab
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849293"
---
# <span data-ttu-id="d022f-101">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="d022f-101">Stop-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="d022f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d022f-102">SYNOPSIS</span></span>
<span data-ttu-id="d022f-103">A Key Vault-ban visszavonja a tanúsítvány működését.</span><span class="sxs-lookup"><span data-stu-id="d022f-103">Cancels a certificate operation in key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d022f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d022f-104">SYNTAX</span></span>

```
Stop-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d022f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d022f-105">DESCRIPTION</span></span>
<span data-ttu-id="d022f-106">A **stop-AzureKeyVaultCertificateOperation** parancsmag az Azure Key Vault szolgáltatásban visszavonja a tanúsítvány működését.</span><span class="sxs-lookup"><span data-stu-id="d022f-106">The **Stop-AzureKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="d022f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d022f-107">EXAMPLES</span></span>

### <span data-ttu-id="d022f-108">Példa 1: a tanúsítvány lemondása</span><span class="sxs-lookup"><span data-stu-id="d022f-108">Example 1: Cancel a certificate operation</span></span>
```
PS C:\>Stop-AzureKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force
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

<span data-ttu-id="d022f-109">Ez a parancs lemondja a TestCert02-tanúsítvány működését.</span><span class="sxs-lookup"><span data-stu-id="d022f-109">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="d022f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d022f-110">PARAMETERS</span></span>

### <span data-ttu-id="d022f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d022f-111">-DefaultProfile</span></span>
<span data-ttu-id="d022f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d022f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d022f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d022f-113">-Force</span></span>
<span data-ttu-id="d022f-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d022f-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d022f-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d022f-115">-Name</span></span>
<span data-ttu-id="d022f-116">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d022f-116">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="d022f-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d022f-117">-VaultName</span></span>
<span data-ttu-id="d022f-118">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d022f-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="d022f-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d022f-119">-Confirm</span></span>
<span data-ttu-id="d022f-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d022f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d022f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d022f-121">-WhatIf</span></span>
<span data-ttu-id="d022f-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d022f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d022f-123">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d022f-123">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d022f-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d022f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d022f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d022f-125">CommonParameters</span></span>
<span data-ttu-id="d022f-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d022f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d022f-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d022f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d022f-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d022f-128">INPUTS</span></span>

## <span data-ttu-id="d022f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d022f-129">OUTPUTS</span></span>

### <span data-ttu-id="d022f-130">Microsoft. Azure. Command. KeyVaultCertificateOperation. models.</span><span class="sxs-lookup"><span data-stu-id="d022f-130">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="d022f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d022f-131">NOTES</span></span>

## <span data-ttu-id="d022f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d022f-132">RELATED LINKS</span></span>

[<span data-ttu-id="d022f-133">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="d022f-133">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="d022f-134">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="d022f-134">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)

