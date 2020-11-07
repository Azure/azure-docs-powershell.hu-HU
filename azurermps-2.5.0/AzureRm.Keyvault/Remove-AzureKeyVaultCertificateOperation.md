---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
ms.openlocfilehash: 7d5a575bfb5e26511f2051e8e45654af1e8c9f2e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848222"
---
# <span data-ttu-id="72060-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="72060-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="72060-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72060-102">SYNOPSIS</span></span>
<span data-ttu-id="72060-103">Tanúsítványtároló törlése egy kulcsból.</span><span class="sxs-lookup"><span data-stu-id="72060-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72060-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72060-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72060-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72060-105">DESCRIPTION</span></span>
<span data-ttu-id="72060-106">A **Remove-AzureKeyVaultCertificateOperation** parancsmag egy tanúsítvány-műveletet töröl egy kulcs boltozatról.</span><span class="sxs-lookup"><span data-stu-id="72060-106">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="72060-107">Példák</span><span class="sxs-lookup"><span data-stu-id="72060-107">EXAMPLES</span></span>

### <span data-ttu-id="72060-108">1. példa: tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="72060-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="72060-109">Ez a parancs eltávolítja a TestCert01 nevű tanúsítvány-műveletet a ContosoKV01, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="72060-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="72060-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72060-110">PARAMETERS</span></span>

### <span data-ttu-id="72060-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72060-111">-DefaultProfile</span></span>
<span data-ttu-id="72060-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="72060-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72060-113">-Force</span><span class="sxs-lookup"><span data-stu-id="72060-113">-Force</span></span>
<span data-ttu-id="72060-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="72060-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="72060-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="72060-115">-Name</span></span>
<span data-ttu-id="72060-116">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72060-116">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="72060-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72060-117">-PassThru</span></span>
<span data-ttu-id="72060-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="72060-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="72060-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="72060-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="72060-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="72060-120">-VaultName</span></span>
<span data-ttu-id="72060-121">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72060-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="72060-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="72060-122">-Confirm</span></span>
<span data-ttu-id="72060-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="72060-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72060-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72060-124">-WhatIf</span></span>
<span data-ttu-id="72060-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="72060-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72060-126">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="72060-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72060-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="72060-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72060-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72060-128">CommonParameters</span></span>
<span data-ttu-id="72060-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72060-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72060-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72060-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72060-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72060-131">INPUTS</span></span>

## <span data-ttu-id="72060-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72060-132">OUTPUTS</span></span>

### <span data-ttu-id="72060-133">Microsoft. Azure. Command. KeyVaultCertificateOperation. models.</span><span class="sxs-lookup"><span data-stu-id="72060-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="72060-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72060-134">NOTES</span></span>

## <span data-ttu-id="72060-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72060-135">RELATED LINKS</span></span>

[<span data-ttu-id="72060-136">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="72060-136">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="72060-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="72060-137">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

