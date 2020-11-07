---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/stop-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: d6def0badcc9973f62beb65dadbb15a39c34e7ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835633"
---
# <span data-ttu-id="f1d53-101">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="f1d53-101">Stop-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="f1d53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1d53-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d53-103">A Key Vault-ban visszavonja a tanúsítvány működését.</span><span class="sxs-lookup"><span data-stu-id="f1d53-103">Cancels a certificate operation in key vault.</span></span>

## <span data-ttu-id="f1d53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1d53-104">SYNTAX</span></span>

### <span data-ttu-id="f1d53-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1d53-105">Default (Default)</span></span>
```
Stop-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1d53-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f1d53-106">InputObject</span></span>
```
Stop-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1d53-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1d53-107">DESCRIPTION</span></span>
<span data-ttu-id="f1d53-108">A **stop-AzKeyVaultCertificateOperation** parancsmag az Azure Key Vault szolgáltatásban visszavonja a tanúsítvány működését.</span><span class="sxs-lookup"><span data-stu-id="f1d53-108">The **Stop-AzKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="f1d53-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f1d53-109">EXAMPLES</span></span>

### <span data-ttu-id="f1d53-110">Példa 1: a tanúsítvány lemondása</span><span class="sxs-lookup"><span data-stu-id="f1d53-110">Example 1: Cancel a certificate operation</span></span>
```powershell
PS C:\> Stop-AzKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force

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

<span data-ttu-id="f1d53-111">Ez a parancs lemondja a TestCert02-tanúsítvány működését.</span><span class="sxs-lookup"><span data-stu-id="f1d53-111">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="f1d53-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1d53-112">PARAMETERS</span></span>

### <span data-ttu-id="f1d53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d53-113">-DefaultProfile</span></span>
<span data-ttu-id="f1d53-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f1d53-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1d53-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f1d53-115">-Force</span></span>
<span data-ttu-id="f1d53-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="f1d53-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d53-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1d53-117">-InputObject</span></span>
<span data-ttu-id="f1d53-118">Operáció objektum</span><span class="sxs-lookup"><span data-stu-id="f1d53-118">Operation object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d53-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f1d53-119">-Name</span></span>
<span data-ttu-id="f1d53-120">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1d53-120">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d53-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f1d53-121">-VaultName</span></span>
<span data-ttu-id="f1d53-122">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1d53-122">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d53-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f1d53-123">-Confirm</span></span>
<span data-ttu-id="f1d53-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f1d53-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d53-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1d53-125">-WhatIf</span></span>
<span data-ttu-id="f1d53-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f1d53-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1d53-127">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f1d53-127">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1d53-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1d53-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d53-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d53-129">CommonParameters</span></span>
<span data-ttu-id="f1d53-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1d53-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d53-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1d53-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d53-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1d53-132">INPUTS</span></span>

### <span data-ttu-id="f1d53-133">Microsoft. Azure. Command. PSKeyVaultCertificateOperation. models.</span><span class="sxs-lookup"><span data-stu-id="f1d53-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="f1d53-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1d53-134">OUTPUTS</span></span>

### <span data-ttu-id="f1d53-135">Microsoft. Azure. Command. PSKeyVaultCertificateOperation. models.</span><span class="sxs-lookup"><span data-stu-id="f1d53-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="f1d53-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1d53-136">NOTES</span></span>

## <span data-ttu-id="f1d53-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1d53-137">RELATED LINKS</span></span>

[<span data-ttu-id="f1d53-138">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="f1d53-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="f1d53-139">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="f1d53-139">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

