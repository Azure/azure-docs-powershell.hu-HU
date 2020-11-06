---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: 5dd9b4f8dded86a0a900a3bb3942b633c29f7020
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504208"
---
# <span data-ttu-id="8d6c3-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="8d6c3-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="8d6c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d6c3-102">SYNOPSIS</span></span>
<span data-ttu-id="8d6c3-103">A fő pince-tanúsítványok konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d6c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d6c3-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d6c3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d6c3-105">DESCRIPTION</span></span>
<span data-ttu-id="8d6c3-106">A **New-AzureRmVmssVaultCertificateConfig** parancsmag a Virtual Machine Scale set (VMSS) virtuális gépeken elhelyezni kívánt titkot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="8d6c3-107">A parancsmag kimenete az Add-AzureRmVmssSecret parancsmaggal való használatra szolgál.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="8d6c3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8d6c3-108">EXAMPLES</span></span>

### <span data-ttu-id="8d6c3-109">Példa 1: kulcs boltozatos tanúsítvány-konfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="8d6c3-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="8d6c3-110">Ez a parancs létrehoz egy fő pince-bizonyítvány-konfigurációt, amely a megadott tanúsítvány URL-címében található MyCerts nevű tanúsítványtárolót használja.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="8d6c3-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d6c3-111">PARAMETERS</span></span>

### <span data-ttu-id="8d6c3-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="8d6c3-112">-CertificateStore</span></span>
<span data-ttu-id="8d6c3-113">A tanúsítványtárolót adja meg a virtuális számítógépeken abban a méretarányban, ahol a tanúsítványt felveszi.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="8d6c3-114">Ez csak a Windows virtuális gép méretarányos készletei esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="8d6c3-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="8d6c3-115">-CertificateUrl</span></span>
<span data-ttu-id="8d6c3-116">A kulcs-Boltozatban tárolt tanúsítvány URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="8d6c3-117">Az alábbi, UTF-8 kódolású JSON objektum Base64 kódolása:</span><span class="sxs-lookup"><span data-stu-id="8d6c3-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="8d6c3-118">{"Data": " \<Base64-encoded-certificate\> "; "adattípus": "pfx", "password": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="8d6c3-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="8d6c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d6c3-119">-DefaultProfile</span></span>
<span data-ttu-id="8d6c3-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d6c3-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8d6c3-121">-Confirm</span></span>
<span data-ttu-id="8d6c3-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d6c3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d6c3-123">-WhatIf</span></span>
<span data-ttu-id="8d6c3-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d6c3-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d6c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d6c3-126">CommonParameters</span></span>
<span data-ttu-id="8d6c3-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d6c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d6c3-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d6c3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d6c3-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d6c3-129">INPUTS</span></span>

## <span data-ttu-id="8d6c3-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d6c3-130">OUTPUTS</span></span>

###  
<span data-ttu-id="8d6c3-131">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8d6c3-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d6c3-132">NOTES</span></span>

## <span data-ttu-id="8d6c3-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d6c3-133">RELATED LINKS</span></span>

[<span data-ttu-id="8d6c3-134">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="8d6c3-134">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
