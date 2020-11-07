---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 0889bfa5abfdf90480eb508ebad7a62607912722
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844442"
---
# <span data-ttu-id="f8ce5-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="f8ce5-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="f8ce5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ce5-103">A fő pince-tanúsítványok konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="f8ce5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8ce5-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8ce5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8ce5-105">DESCRIPTION</span></span>
<span data-ttu-id="f8ce5-106">A **New-AzVmssVaultCertificateConfig** parancsmag a Virtual Machine Scale set (VMSS) virtuális gépeken elhelyezni kívánt titkot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="f8ce5-107">A parancsmag kimenete az Add-AzVmssSecret parancsmaggal való használatra szolgál.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="f8ce5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f8ce5-108">EXAMPLES</span></span>

### <span data-ttu-id="f8ce5-109">Példa 1: kulcs boltozatos tanúsítvány-konfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="f8ce5-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="f8ce5-110">Ez a parancs létrehoz egy fő pince-bizonyítvány-konfigurációt, amely a megadott tanúsítvány URL-címében található MyCerts nevű tanúsítványtárolót használja.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="f8ce5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8ce5-111">PARAMETERS</span></span>

### <span data-ttu-id="f8ce5-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="f8ce5-112">-CertificateStore</span></span>
<span data-ttu-id="f8ce5-113">A tanúsítványtárolót adja meg a virtuális számítógépeken abban a méretarányban, ahol a tanúsítványt felveszi.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="f8ce5-114">Ez csak a Windows virtuális gép méretarányos készletei esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ce5-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="f8ce5-115">-CertificateUrl</span></span>
<span data-ttu-id="f8ce5-116">A kulcs-Boltozatban tárolt tanúsítvány URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="f8ce5-117">Az alábbi, UTF-8 kódolású JSON objektum Base64 kódolása:</span><span class="sxs-lookup"><span data-stu-id="f8ce5-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="f8ce5-118">{"Data": " \< Base64-kódolt tanúsítvány \> "," adattípus ":" pfx "," password ":" \< pfx-fájl-jelszó " \> }</span><span class="sxs-lookup"><span data-stu-id="f8ce5-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ce5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8ce5-119">-DefaultProfile</span></span>
<span data-ttu-id="f8ce5-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8ce5-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f8ce5-121">-Confirm</span></span>
<span data-ttu-id="f8ce5-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ce5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8ce5-123">-WhatIf</span></span>
<span data-ttu-id="f8ce5-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8ce5-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ce5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ce5-126">CommonParameters</span></span>
<span data-ttu-id="f8ce5-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8ce5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ce5-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8ce5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ce5-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8ce5-129">INPUTS</span></span>

### <span data-ttu-id="f8ce5-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="f8ce5-130">None</span></span>
<span data-ttu-id="f8ce5-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8ce5-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8ce5-132">OUTPUTS</span></span>

###  
<span data-ttu-id="f8ce5-133">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f8ce5-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f8ce5-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8ce5-134">NOTES</span></span>

## <span data-ttu-id="f8ce5-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8ce5-135">RELATED LINKS</span></span>

[<span data-ttu-id="f8ce5-136">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="f8ce5-136">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
