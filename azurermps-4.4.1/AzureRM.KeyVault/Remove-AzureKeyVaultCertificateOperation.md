---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: d40489471e94474e83243803b5c64cdad1d572d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502716"
---
# <span data-ttu-id="0fd36-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="0fd36-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="0fd36-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0fd36-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd36-103">Tanúsítványtároló törlése egy kulcsból.</span><span class="sxs-lookup"><span data-stu-id="0fd36-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fd36-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0fd36-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fd36-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0fd36-105">DESCRIPTION</span></span>
<span data-ttu-id="0fd36-106">A **Remove-AzureKeyVaultCertificateOperation** parancsmag egy tanúsítvány-műveletet töröl egy kulcs boltozatról.</span><span class="sxs-lookup"><span data-stu-id="0fd36-106">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="0fd36-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0fd36-107">EXAMPLES</span></span>

### <span data-ttu-id="0fd36-108">1. példa: tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0fd36-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="0fd36-109">Ez a parancs eltávolítja a TestCert01 nevű tanúsítvány-műveletet a ContosoKV01, és nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0fd36-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="0fd36-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0fd36-110">PARAMETERS</span></span>

### <span data-ttu-id="0fd36-111">-Force</span><span class="sxs-lookup"><span data-stu-id="0fd36-111">-Force</span></span>
<span data-ttu-id="0fd36-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0fd36-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0fd36-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0fd36-113">-Name</span></span>
<span data-ttu-id="0fd36-114">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0fd36-114">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd36-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fd36-115">-PassThru</span></span>
<span data-ttu-id="0fd36-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="0fd36-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0fd36-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="0fd36-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0fd36-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0fd36-118">-VaultName</span></span>
<span data-ttu-id="0fd36-119">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0fd36-119">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd36-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0fd36-120">-Confirm</span></span>
<span data-ttu-id="0fd36-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0fd36-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fd36-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fd36-122">-WhatIf</span></span>
<span data-ttu-id="0fd36-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0fd36-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fd36-124">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0fd36-124">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fd36-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0fd36-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fd36-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd36-126">-DefaultProfile</span></span>
<span data-ttu-id="0fd36-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fd36-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fd36-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd36-128">CommonParameters</span></span>
<span data-ttu-id="0fd36-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0fd36-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd36-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fd36-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd36-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fd36-131">INPUTS</span></span>

## <span data-ttu-id="0fd36-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fd36-132">OUTPUTS</span></span>

### <span data-ttu-id="0fd36-133">Microsoft. Azure. Command. KeyVaultCertificateOperation. models.</span><span class="sxs-lookup"><span data-stu-id="0fd36-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="0fd36-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0fd36-134">NOTES</span></span>

## <span data-ttu-id="0fd36-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fd36-135">RELATED LINKS</span></span>

[<span data-ttu-id="0fd36-136">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="0fd36-136">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="0fd36-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="0fd36-137">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

