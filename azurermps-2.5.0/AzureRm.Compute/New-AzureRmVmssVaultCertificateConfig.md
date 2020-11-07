---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssvaultcertificateconfig
schema: 2.0.0
ms.openlocfilehash: 9ae4e22cde856129d21965b7e7f2fc9af647572a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850105"
---
# <span data-ttu-id="b32a7-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="b32a7-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="b32a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b32a7-102">SYNOPSIS</span></span>
<span data-ttu-id="b32a7-103">A fő pince-tanúsítványok konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="b32a7-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b32a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b32a7-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b32a7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b32a7-105">DESCRIPTION</span></span>
<span data-ttu-id="b32a7-106">A **New-AzureRmVmssVaultCertificateConfig** parancsmag a Virtual Machine Scale set (VMSS) virtuális gépeken elhelyezni kívánt titkot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b32a7-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="b32a7-107">A parancsmag kimenete az Add-AzureRmVmssSecret parancsmaggal való használatra szolgál.</span><span class="sxs-lookup"><span data-stu-id="b32a7-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="b32a7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b32a7-108">EXAMPLES</span></span>

### <span data-ttu-id="b32a7-109">Példa 1: kulcs boltozatos tanúsítvány-konfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="b32a7-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="b32a7-110">Ez a parancs létrehoz egy fő pince-bizonyítvány-konfigurációt, amely a megadott tanúsítvány URL-címében található MyCerts nevű tanúsítványtárolót használja.</span><span class="sxs-lookup"><span data-stu-id="b32a7-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="b32a7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b32a7-111">PARAMETERS</span></span>

### <span data-ttu-id="b32a7-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="b32a7-112">-CertificateStore</span></span>
<span data-ttu-id="b32a7-113">A tanúsítványtárolót adja meg a virtuális számítógépeken abban a méretarányban, ahol a tanúsítványt felveszi.</span><span class="sxs-lookup"><span data-stu-id="b32a7-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="b32a7-114">Ez csak a Windows virtuális gép méretarányos készletei esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="b32a7-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="b32a7-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="b32a7-115">-CertificateUrl</span></span>
<span data-ttu-id="b32a7-116">A kulcs-Boltozatban tárolt tanúsítvány URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b32a7-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="b32a7-117">Az alábbi, UTF-8 kódolású JSON objektum Base64 kódolása:</span><span class="sxs-lookup"><span data-stu-id="b32a7-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="b32a7-118">{"Data": " \<Base64-encoded-certificate\> "; "adattípus": "pfx", "password": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="b32a7-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="b32a7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b32a7-119">-DefaultProfile</span></span>
<span data-ttu-id="b32a7-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b32a7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b32a7-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b32a7-121">-Confirm</span></span>
<span data-ttu-id="b32a7-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b32a7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b32a7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b32a7-123">-WhatIf</span></span>
<span data-ttu-id="b32a7-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b32a7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b32a7-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b32a7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b32a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b32a7-126">CommonParameters</span></span>
<span data-ttu-id="b32a7-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b32a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b32a7-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b32a7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b32a7-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b32a7-129">INPUTS</span></span>

### <span data-ttu-id="b32a7-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="b32a7-130">None</span></span>
<span data-ttu-id="b32a7-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b32a7-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b32a7-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b32a7-132">OUTPUTS</span></span>

###  
<span data-ttu-id="b32a7-133">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b32a7-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b32a7-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b32a7-134">NOTES</span></span>

## <span data-ttu-id="b32a7-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b32a7-135">RELATED LINKS</span></span>

[<span data-ttu-id="b32a7-136">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="b32a7-136">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
