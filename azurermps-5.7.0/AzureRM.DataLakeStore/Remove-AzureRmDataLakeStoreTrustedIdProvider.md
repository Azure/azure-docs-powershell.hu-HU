---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c769e3e084f0ac5fd6df22bae81a4d8df99dc700
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504579"
---
# <span data-ttu-id="2b091-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="2b091-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="2b091-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b091-102">SYNOPSIS</span></span>
<span data-ttu-id="2b091-103">A megadott megbízható identitás-szolgáltató eltávolítása a megadott Data Lake Store áruházból.</span><span class="sxs-lookup"><span data-stu-id="2b091-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b091-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b091-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b091-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b091-105">DESCRIPTION</span></span>
<span data-ttu-id="2b091-106">A **Remove-AzureRmDataLakeStoreTrustedIdProvider** parancsmag eltávolítja a megadott megbízható identitás-szolgáltatót a megadott Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="2b091-106">The **Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="2b091-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2b091-107">EXAMPLES</span></span>

### <span data-ttu-id="2b091-108">Példa 1: a megbízható identitás-szolgáltató eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="2b091-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="2b091-109">A "MyProvider" szolgáltató eltávolítása a "ContosoADL" fiókból</span><span class="sxs-lookup"><span data-stu-id="2b091-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="2b091-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b091-110">PARAMETERS</span></span>

### <span data-ttu-id="2b091-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="2b091-111">-Account</span></span>
<span data-ttu-id="2b091-112">Az Data Lake Store fiók a megbízható identitás-szolgáltató eltávolításához</span><span class="sxs-lookup"><span data-stu-id="2b091-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b091-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b091-113">-DefaultProfile</span></span>
<span data-ttu-id="2b091-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2b091-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b091-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2b091-115">-Name</span></span>
<span data-ttu-id="2b091-116">A megbízható identitás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="2b091-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="2b091-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b091-117">-PassThru</span></span>
<span data-ttu-id="2b091-118">A törlési művelet eredményét jelző logikai választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="2b091-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b091-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b091-119">-ResourceGroupName</span></span>
<span data-ttu-id="2b091-120">Annak a csoportnak a nevét adja meg, amely tartalmazza azt a fiókot, amelyből el szeretné távolítani a megbízható személyazonosság-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="2b091-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b091-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2b091-121">-Confirm</span></span>
<span data-ttu-id="2b091-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2b091-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b091-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b091-123">-WhatIf</span></span>
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

### <span data-ttu-id="2b091-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b091-124">CommonParameters</span></span>
<span data-ttu-id="2b091-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b091-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b091-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b091-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b091-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b091-127">INPUTS</span></span>

### <span data-ttu-id="2b091-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="2b091-128">None</span></span>
<span data-ttu-id="2b091-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2b091-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b091-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b091-130">OUTPUTS</span></span>

### <span data-ttu-id="2b091-131">bool</span><span class="sxs-lookup"><span data-stu-id="2b091-131">bool</span></span>
<span data-ttu-id="2b091-132">Ha a PassThru meg van adva, akkor a sikeres befejezéshez az igaz értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="2b091-132">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="2b091-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b091-133">NOTES</span></span>

## <span data-ttu-id="2b091-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b091-134">RELATED LINKS</span></span>

