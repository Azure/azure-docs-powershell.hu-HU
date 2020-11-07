---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 37cc2025b97e16a2af313a2f4dd2cf7dfe815b7b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842109"
---
# <span data-ttu-id="ecacb-101">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="ecacb-101">Remove-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="ecacb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ecacb-102">SYNOPSIS</span></span>
<span data-ttu-id="ecacb-103">Tanúsítványtároló törlése egy kulcsból.</span><span class="sxs-lookup"><span data-stu-id="ecacb-103">Deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="ecacb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ecacb-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecacb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ecacb-105">DESCRIPTION</span></span>
<span data-ttu-id="ecacb-106">A **Remove-AzKeyVaultCertificateOperation** parancsmag egy tanúsítvány-műveletet töröl egy kulcs boltozatról.</span><span class="sxs-lookup"><span data-stu-id="ecacb-106">The **Remove-AzKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="ecacb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ecacb-107">EXAMPLES</span></span>

### <span data-ttu-id="ecacb-108">1. példa: tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ecacb-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="ecacb-109">Ez a parancs eltávolítja a TestCert01 nevű tanúsítvány-műveletet a ContosoKV01, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ecacb-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="ecacb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ecacb-110">PARAMETERS</span></span>

### <span data-ttu-id="ecacb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecacb-111">-DefaultProfile</span></span>
<span data-ttu-id="ecacb-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ecacb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecacb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ecacb-113">-Force</span></span>
<span data-ttu-id="ecacb-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ecacb-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ecacb-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ecacb-115">-Name</span></span>
<span data-ttu-id="ecacb-116">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ecacb-116">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="ecacb-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecacb-117">-PassThru</span></span>
<span data-ttu-id="ecacb-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ecacb-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ecacb-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ecacb-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ecacb-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ecacb-120">-VaultName</span></span>
<span data-ttu-id="ecacb-121">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ecacb-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="ecacb-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ecacb-122">-Confirm</span></span>
<span data-ttu-id="ecacb-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ecacb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecacb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecacb-124">-WhatIf</span></span>
<span data-ttu-id="ecacb-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ecacb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecacb-126">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ecacb-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecacb-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ecacb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecacb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecacb-128">CommonParameters</span></span>
<span data-ttu-id="ecacb-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ecacb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecacb-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecacb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecacb-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecacb-131">INPUTS</span></span>

### <span data-ttu-id="ecacb-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="ecacb-132">None</span></span>
<span data-ttu-id="ecacb-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ecacb-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ecacb-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecacb-134">OUTPUTS</span></span>

### <span data-ttu-id="ecacb-135">Microsoft. Azure. Command. KeyVaultCertificateOperation. models.</span><span class="sxs-lookup"><span data-stu-id="ecacb-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="ecacb-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ecacb-136">NOTES</span></span>

## <span data-ttu-id="ecacb-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ecacb-137">RELATED LINKS</span></span>

[<span data-ttu-id="ecacb-138">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="ecacb-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="ecacb-139">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="ecacb-139">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

