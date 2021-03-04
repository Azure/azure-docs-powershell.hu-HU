---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: cc607e12873e0b5b738a64d781d16ed73bc72f7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937105"
---
# <span data-ttu-id="e23a4-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="e23a4-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="e23a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e23a4-102">SYNOPSIS</span></span>
<span data-ttu-id="e23a4-103">Kulcstároló tanúsítványkonfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e23a4-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="e23a4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e23a4-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e23a4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e23a4-105">DESCRIPTION</span></span>
<span data-ttu-id="e23a4-106">A **New-AzVmssVaultCertificateConfig** parancsmag megadja a virtuálisgép-mérethalmaz (VMSS) virtuális gépeibe helyezendő titkos halmazt.</span><span class="sxs-lookup"><span data-stu-id="e23a4-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="e23a4-107">A parancsmag kimenete a Add-AzVmssSecret használható.</span><span class="sxs-lookup"><span data-stu-id="e23a4-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="e23a4-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e23a4-108">EXAMPLES</span></span>

### <span data-ttu-id="e23a4-109">1. példa: Kulcstároló tanúsítványkonfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="e23a4-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="e23a4-110">Ez a parancs létrehoz egy kulcstároló tanúsítványkonfigurációt, amely a MyCerts nevű tanúsítványtárat használja a megadott tanúsítvány URL-címében.</span><span class="sxs-lookup"><span data-stu-id="e23a4-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="e23a4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e23a4-111">PARAMETERS</span></span>

### <span data-ttu-id="e23a4-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="e23a4-112">-CertificateStore</span></span>
<span data-ttu-id="e23a4-113">Megadja a tanúsítványt tároló tanúsítványt a virtuális gépeken abban a méretaránykészletben, amelyben a tanúsítványt hozzáadta.</span><span class="sxs-lookup"><span data-stu-id="e23a4-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="e23a4-114">Ez csak a Windows Virtuálisgép-mérethalmazok esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="e23a4-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e23a4-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="e23a4-115">-CertificateUrl</span></span>
<span data-ttu-id="e23a4-116">A kulcstárolóban tárolt tanúsítvány URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e23a4-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="e23a4-117">Ez a következő JSON-objektum alap64 kódolású kódolása, amely UTF-8 kódolású: { "adatok":" \<Base64-encoded-certificate\> ", "dataType":"pfx";"password":" \<pfx-file-password\> " }</span><span class="sxs-lookup"><span data-stu-id="e23a4-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e23a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e23a4-118">-DefaultProfile</span></span>
<span data-ttu-id="e23a4-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e23a4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e23a4-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e23a4-120">-Confirm</span></span>
<span data-ttu-id="e23a4-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e23a4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e23a4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e23a4-122">-WhatIf</span></span>
<span data-ttu-id="e23a4-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e23a4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e23a4-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e23a4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e23a4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e23a4-125">CommonParameters</span></span>
<span data-ttu-id="e23a4-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e23a4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e23a4-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e23a4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e23a4-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e23a4-128">INPUTS</span></span>

### <span data-ttu-id="e23a4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e23a4-129">System.String</span></span>

## <span data-ttu-id="e23a4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e23a4-130">OUTPUTS</span></span>

### <span data-ttu-id="e23a4-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e23a4-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="e23a4-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e23a4-132">NOTES</span></span>

## <span data-ttu-id="e23a4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e23a4-133">RELATED LINKS</span></span>

[<span data-ttu-id="e23a4-134">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="e23a4-134">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
