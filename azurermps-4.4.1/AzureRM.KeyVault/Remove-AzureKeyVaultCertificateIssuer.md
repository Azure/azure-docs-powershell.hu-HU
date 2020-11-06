---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 3ef23bcbddc1f8a5c5c235c72dac32f535a71a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502719"
---
# <span data-ttu-id="fd61d-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="fd61d-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="fd61d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd61d-102">SYNOPSIS</span></span>
<span data-ttu-id="fd61d-103">A tanúsítvány kijavítása egy kulcs boltozatról</span><span class="sxs-lookup"><span data-stu-id="fd61d-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd61d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd61d-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd61d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd61d-105">DESCRIPTION</span></span>
<span data-ttu-id="fd61d-106">A **Remove-AzureKeyVaultCertificateIssuer** parancsmag a tanúsítvány kifizetését egy kulcs boltozatról törli.</span><span class="sxs-lookup"><span data-stu-id="fd61d-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="fd61d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fd61d-107">EXAMPLES</span></span>

### <span data-ttu-id="fd61d-108">1. példa: a tanúsítvány kibocsátásának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fd61d-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="fd61d-109">Ez a parancs eltávolítja a TestIssuer01 nevű tanúsítvány-kibocsátási kulcsot a ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="fd61d-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="fd61d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd61d-110">PARAMETERS</span></span>

### <span data-ttu-id="fd61d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="fd61d-111">-Force</span></span>
<span data-ttu-id="fd61d-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="fd61d-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fd61d-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd61d-113">-Name</span></span>
<span data-ttu-id="fd61d-114">Itt adhatja meg az eltávolítandó tanúsítvány nevét.</span><span class="sxs-lookup"><span data-stu-id="fd61d-114">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd61d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd61d-115">-PassThru</span></span>
<span data-ttu-id="fd61d-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="fd61d-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fd61d-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="fd61d-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fd61d-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fd61d-118">-VaultName</span></span>
<span data-ttu-id="fd61d-119">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd61d-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="fd61d-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fd61d-120">-Confirm</span></span>
<span data-ttu-id="fd61d-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd61d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd61d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd61d-122">-WhatIf</span></span>
<span data-ttu-id="fd61d-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fd61d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd61d-124">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fd61d-124">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd61d-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd61d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd61d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd61d-126">-DefaultProfile</span></span>
<span data-ttu-id="fd61d-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd61d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd61d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd61d-128">CommonParameters</span></span>
<span data-ttu-id="fd61d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd61d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd61d-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd61d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd61d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd61d-131">INPUTS</span></span>

## <span data-ttu-id="fd61d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd61d-132">OUTPUTS</span></span>

### <span data-ttu-id="fd61d-133">Microsoft. Azure. Command. KeyVaultCertificateIssuer. models.</span><span class="sxs-lookup"><span data-stu-id="fd61d-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="fd61d-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd61d-134">NOTES</span></span>

## <span data-ttu-id="fd61d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd61d-135">RELATED LINKS</span></span>

[<span data-ttu-id="fd61d-136">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="fd61d-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="fd61d-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="fd61d-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


