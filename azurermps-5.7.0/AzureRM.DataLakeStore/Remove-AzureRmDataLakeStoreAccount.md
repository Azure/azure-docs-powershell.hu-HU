---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 4e21d122c8a49209a7591457c36ba99fcc10496c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493136"
---
# <span data-ttu-id="af4cf-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="af4cf-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="af4cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af4cf-102">SYNOPSIS</span></span>
<span data-ttu-id="af4cf-103">Véglegesen törli az adattó-tároló fiókját.</span><span class="sxs-lookup"><span data-stu-id="af4cf-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af4cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af4cf-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af4cf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="af4cf-105">DESCRIPTION</span></span>
<span data-ttu-id="af4cf-106">A **Remove-AzureRmDataLakeStoreAccount** parancsmag véglegesen törli az adattó-tároló fiókját.</span><span class="sxs-lookup"><span data-stu-id="af4cf-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="af4cf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="af4cf-107">EXAMPLES</span></span>

### <span data-ttu-id="af4cf-108">1. példa: az adattó áruházbeli fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="af4cf-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="af4cf-109">Ez a parancs eltávolítja a ContosoADL nevű fiókot az adattó áruházból.</span><span class="sxs-lookup"><span data-stu-id="af4cf-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="af4cf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af4cf-110">PARAMETERS</span></span>

### <span data-ttu-id="af4cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af4cf-111">-DefaultProfile</span></span>
<span data-ttu-id="af4cf-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="af4cf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af4cf-113">-Force</span><span class="sxs-lookup"><span data-stu-id="af4cf-113">-Force</span></span>
<span data-ttu-id="af4cf-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="af4cf-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4cf-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af4cf-115">-Name</span></span>
<span data-ttu-id="af4cf-116">Az eltávolítandó fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af4cf-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="af4cf-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af4cf-117">-PassThru</span></span>
<span data-ttu-id="af4cf-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="af4cf-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="af4cf-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="af4cf-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4cf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af4cf-120">-ResourceGroupName</span></span>
<span data-ttu-id="af4cf-121">Azt az erőforráscsoportot adja meg, amely az eltávolítandó fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="af4cf-121">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="af4cf-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="af4cf-122">-Confirm</span></span>
<span data-ttu-id="af4cf-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="af4cf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af4cf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af4cf-124">-WhatIf</span></span>
<span data-ttu-id="af4cf-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="af4cf-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af4cf-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af4cf-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af4cf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af4cf-127">CommonParameters</span></span>
<span data-ttu-id="af4cf-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af4cf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af4cf-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af4cf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af4cf-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af4cf-130">INPUTS</span></span>

### <span data-ttu-id="af4cf-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="af4cf-131">None</span></span>
<span data-ttu-id="af4cf-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="af4cf-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af4cf-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af4cf-133">OUTPUTS</span></span>

### <span data-ttu-id="af4cf-134">bool</span><span class="sxs-lookup"><span data-stu-id="af4cf-134">bool</span></span>
<span data-ttu-id="af4cf-135">Ha a PassThru meg van adva, akkor a sikeres befejezéshez az igaz értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="af4cf-135">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="af4cf-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af4cf-136">NOTES</span></span>

## <span data-ttu-id="af4cf-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af4cf-137">RELATED LINKS</span></span>

[<span data-ttu-id="af4cf-138">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="af4cf-138">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="af4cf-139">Új – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="af4cf-139">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="af4cf-140">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="af4cf-140">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="af4cf-141">Teszt-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="af4cf-141">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


