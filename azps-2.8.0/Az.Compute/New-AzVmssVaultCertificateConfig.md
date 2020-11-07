---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 0afd599bd1af9b3f597e9753d1be1e8ae710e5bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667342"
---
# <span data-ttu-id="0af09-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="0af09-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="0af09-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0af09-102">SYNOPSIS</span></span>
<span data-ttu-id="0af09-103">A fő pince-tanúsítványok konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="0af09-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="0af09-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0af09-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0af09-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0af09-105">DESCRIPTION</span></span>
<span data-ttu-id="0af09-106">A **New-AzVmssVaultCertificateConfig** parancsmag a Virtual Machine Scale set (VMSS) virtuális gépeken elhelyezni kívánt titkot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0af09-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="0af09-107">A parancsmag kimenete az Add-AzVmssSecret parancsmaggal való használatra szolgál.</span><span class="sxs-lookup"><span data-stu-id="0af09-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="0af09-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0af09-108">EXAMPLES</span></span>

### <span data-ttu-id="0af09-109">Példa 1: kulcs boltozatos tanúsítvány-konfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="0af09-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="0af09-110">Ez a parancs létrehoz egy fő pince-bizonyítvány-konfigurációt, amely a megadott tanúsítvány URL-címében található MyCerts nevű tanúsítványtárolót használja.</span><span class="sxs-lookup"><span data-stu-id="0af09-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="0af09-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0af09-111">PARAMETERS</span></span>

### <span data-ttu-id="0af09-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="0af09-112">-CertificateStore</span></span>
<span data-ttu-id="0af09-113">A tanúsítványtárolót adja meg a virtuális számítógépeken abban a méretarányban, ahol a tanúsítványt felveszi.</span><span class="sxs-lookup"><span data-stu-id="0af09-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="0af09-114">Ez csak a Windows virtuális gép méretarányos készletei esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="0af09-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="0af09-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="0af09-115">-CertificateUrl</span></span>
<span data-ttu-id="0af09-116">A kulcs-Boltozatban tárolt tanúsítvány URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0af09-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="0af09-117">Ez a következő JSON-objektum Base64 kódolása, amely UTF-8-ban kódolt: {"Data": " \< Base64-kódolt tanúsítvány \> ", "adattípus": "pfx", "password": " \< pfx-fájl – jelszó" \> }</span><span class="sxs-lookup"><span data-stu-id="0af09-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="0af09-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af09-118">-DefaultProfile</span></span>
<span data-ttu-id="0af09-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0af09-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0af09-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0af09-120">-Confirm</span></span>
<span data-ttu-id="0af09-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0af09-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0af09-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0af09-122">-WhatIf</span></span>
<span data-ttu-id="0af09-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0af09-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0af09-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0af09-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0af09-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af09-125">CommonParameters</span></span>
<span data-ttu-id="0af09-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0af09-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af09-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0af09-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af09-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0af09-128">INPUTS</span></span>

### <span data-ttu-id="0af09-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0af09-129">System.String</span></span>

## <span data-ttu-id="0af09-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0af09-130">OUTPUTS</span></span>

### <span data-ttu-id="0af09-131">Microsoft. Azure. Management. kiszámítás. models. VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0af09-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="0af09-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0af09-132">NOTES</span></span>

## <span data-ttu-id="0af09-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0af09-133">RELATED LINKS</span></span>

[<span data-ttu-id="0af09-134">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="0af09-134">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
