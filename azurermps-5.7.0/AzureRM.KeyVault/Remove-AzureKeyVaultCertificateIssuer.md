---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 05a59e3fd098fb32122cc85a4d39e89cf1fc66aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672524"
---
# <span data-ttu-id="2b86e-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2b86e-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="2b86e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b86e-102">SYNOPSIS</span></span>
<span data-ttu-id="2b86e-103">A tanúsítvány kijavítása egy kulcs boltozatról</span><span class="sxs-lookup"><span data-stu-id="2b86e-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b86e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b86e-104">SYNTAX</span></span>

### <span data-ttu-id="2b86e-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2b86e-105">Default (Default)</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b86e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2b86e-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b86e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b86e-107">DESCRIPTION</span></span>
<span data-ttu-id="2b86e-108">A **Remove-AzureKeyVaultCertificateIssuer** parancsmag a tanúsítvány kifizetését egy kulcs boltozatról törli.</span><span class="sxs-lookup"><span data-stu-id="2b86e-108">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="2b86e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2b86e-109">EXAMPLES</span></span>

### <span data-ttu-id="2b86e-110">1. példa: a tanúsítvány kibocsátásának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2b86e-110">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="2b86e-111">Ez a parancs eltávolítja a TestIssuer01 nevű tanúsítvány-kibocsátási kulcsot a ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="2b86e-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="2b86e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b86e-112">PARAMETERS</span></span>

### <span data-ttu-id="2b86e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b86e-113">-DefaultProfile</span></span>
<span data-ttu-id="2b86e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2b86e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b86e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2b86e-115">-Force</span></span>
<span data-ttu-id="2b86e-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2b86e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2b86e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b86e-117">-InputObject</span></span>
<span data-ttu-id="2b86e-118">A tanúsítvány-kibocsátási objektum</span><span class="sxs-lookup"><span data-stu-id="2b86e-118">Certificate Issuer Object</span></span>

```yaml
Type: PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b86e-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2b86e-119">-Name</span></span>
<span data-ttu-id="2b86e-120">Itt adhatja meg az eltávolítandó tanúsítvány nevét.</span><span class="sxs-lookup"><span data-stu-id="2b86e-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b86e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b86e-121">-PassThru</span></span>
<span data-ttu-id="2b86e-122">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2b86e-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2b86e-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2b86e-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2b86e-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2b86e-124">-VaultName</span></span>
<span data-ttu-id="2b86e-125">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b86e-125">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b86e-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2b86e-126">-Confirm</span></span>
<span data-ttu-id="2b86e-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2b86e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b86e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b86e-128">-WhatIf</span></span>
<span data-ttu-id="2b86e-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2b86e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b86e-130">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2b86e-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b86e-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2b86e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b86e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b86e-132">CommonParameters</span></span>
<span data-ttu-id="2b86e-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b86e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b86e-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b86e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b86e-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b86e-135">INPUTS</span></span>

### <span data-ttu-id="2b86e-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="2b86e-136">None</span></span>
<span data-ttu-id="2b86e-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2b86e-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b86e-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b86e-138">OUTPUTS</span></span>

### <span data-ttu-id="2b86e-139">Microsoft. Azure. Command. PSKeyVaultCertificateIssuer. models.</span><span class="sxs-lookup"><span data-stu-id="2b86e-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="2b86e-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b86e-140">NOTES</span></span>

## <span data-ttu-id="2b86e-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b86e-141">RELATED LINKS</span></span>

[<span data-ttu-id="2b86e-142">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2b86e-142">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="2b86e-143">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2b86e-143">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


