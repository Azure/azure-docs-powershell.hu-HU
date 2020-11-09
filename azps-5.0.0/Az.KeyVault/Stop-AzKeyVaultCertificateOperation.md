---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/stop-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: e260b32e847705240d93451b32bef9ae31d7fa07
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296828"
---
# <span data-ttu-id="7d752-101">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7d752-101">Stop-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="7d752-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d752-102">SYNOPSIS</span></span>
<span data-ttu-id="7d752-103">A Key Vault-ban visszavonja a tanúsítvány működését.</span><span class="sxs-lookup"><span data-stu-id="7d752-103">Cancels a certificate operation in key vault.</span></span>

## <span data-ttu-id="7d752-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d752-104">SYNTAX</span></span>

### <span data-ttu-id="7d752-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7d752-105">Default (Default)</span></span>
```
Stop-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d752-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7d752-106">InputObject</span></span>
```
Stop-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d752-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d752-107">DESCRIPTION</span></span>
<span data-ttu-id="7d752-108">A **stop-AzKeyVaultCertificateOperation** parancsmag az Azure Key Vault szolgáltatásban visszavonja a tanúsítvány működését.</span><span class="sxs-lookup"><span data-stu-id="7d752-108">The **Stop-AzKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="7d752-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7d752-109">EXAMPLES</span></span>

### <span data-ttu-id="7d752-110">Példa 1: a tanúsítvány lemondása</span><span class="sxs-lookup"><span data-stu-id="7d752-110">Example 1: Cancel a certificate operation</span></span>
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

<span data-ttu-id="7d752-111">Ez a parancs lemondja a TestCert02-tanúsítvány működését.</span><span class="sxs-lookup"><span data-stu-id="7d752-111">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="7d752-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d752-112">PARAMETERS</span></span>

### <span data-ttu-id="7d752-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d752-113">-DefaultProfile</span></span>
<span data-ttu-id="7d752-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7d752-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d752-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7d752-115">-Force</span></span>
<span data-ttu-id="7d752-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="7d752-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7d752-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d752-117">-InputObject</span></span>
<span data-ttu-id="7d752-118">Operáció objektum</span><span class="sxs-lookup"><span data-stu-id="7d752-118">Operation object</span></span>

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

### <span data-ttu-id="7d752-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7d752-119">-Name</span></span>
<span data-ttu-id="7d752-120">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d752-120">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="7d752-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7d752-121">-VaultName</span></span>
<span data-ttu-id="7d752-122">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d752-122">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="7d752-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d752-123">-Confirm</span></span>
<span data-ttu-id="7d752-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d752-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d752-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d752-125">-WhatIf</span></span>
<span data-ttu-id="7d752-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d752-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d752-127">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d752-127">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d752-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d752-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d752-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d752-129">CommonParameters</span></span>
<span data-ttu-id="7d752-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d752-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d752-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7d752-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d752-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d752-132">INPUTS</span></span>

### <span data-ttu-id="7d752-133">Microsoft. Azure. Command. PSKeyVaultCertificateOperation. models.</span><span class="sxs-lookup"><span data-stu-id="7d752-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="7d752-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d752-134">OUTPUTS</span></span>

### <span data-ttu-id="7d752-135">Microsoft. Azure. Command. PSKeyVaultCertificateOperation. models.</span><span class="sxs-lookup"><span data-stu-id="7d752-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="7d752-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d752-136">NOTES</span></span>

## <span data-ttu-id="7d752-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d752-137">RELATED LINKS</span></span>

[<span data-ttu-id="7d752-138">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7d752-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="7d752-139">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7d752-139">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

