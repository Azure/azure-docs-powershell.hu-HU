---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: f978925766fb664f5ddeaf3b6dffa94e55244f43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672375"
---
# <span data-ttu-id="6d112-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6d112-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="6d112-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d112-102">SYNOPSIS</span></span>
<span data-ttu-id="6d112-103">Az adattó-Analytics-fiók törlése</span><span class="sxs-lookup"><span data-stu-id="6d112-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d112-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d112-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d112-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d112-105">DESCRIPTION</span></span>
<span data-ttu-id="6d112-106">A **Remove-AzureRmDataLakeAnalyticsAccount** parancsmag véglegesen törli az Azure Data Lake Analytics-fiókját.</span><span class="sxs-lookup"><span data-stu-id="6d112-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="6d112-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6d112-107">EXAMPLES</span></span>

### <span data-ttu-id="6d112-108">1. példa: fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6d112-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="6d112-109">Ez a parancs eltávolítja a megadott Data Lake Analytics-fiókot.</span><span class="sxs-lookup"><span data-stu-id="6d112-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="6d112-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d112-110">PARAMETERS</span></span>

### <span data-ttu-id="6d112-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d112-111">-DefaultProfile</span></span>
<span data-ttu-id="6d112-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6d112-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d112-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6d112-113">-Force</span></span>
<span data-ttu-id="6d112-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6d112-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6d112-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6d112-115">-Name</span></span>
<span data-ttu-id="6d112-116">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6d112-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="6d112-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d112-117">-PassThru</span></span>
<span data-ttu-id="6d112-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6d112-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6d112-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="6d112-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6d112-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d112-120">-ResourceGroupName</span></span>
<span data-ttu-id="6d112-121">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6d112-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="6d112-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6d112-122">-Confirm</span></span>
<span data-ttu-id="6d112-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6d112-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d112-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d112-124">-WhatIf</span></span>
<span data-ttu-id="6d112-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6d112-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d112-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d112-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d112-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d112-127">CommonParameters</span></span>
<span data-ttu-id="6d112-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d112-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d112-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d112-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d112-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d112-130">INPUTS</span></span>

### <span data-ttu-id="6d112-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="6d112-131">None</span></span>
<span data-ttu-id="6d112-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="6d112-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6d112-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d112-133">OUTPUTS</span></span>

### <span data-ttu-id="6d112-134">bool</span><span class="sxs-lookup"><span data-stu-id="6d112-134">bool</span></span>
<span data-ttu-id="6d112-135">Ha a PassThru meg van adva, a művelet befejezésekor a True értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="6d112-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="6d112-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d112-136">NOTES</span></span>

## <span data-ttu-id="6d112-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d112-137">RELATED LINKS</span></span>

[<span data-ttu-id="6d112-138">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6d112-138">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6d112-139">Új – AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6d112-139">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6d112-140">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6d112-140">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6d112-141">Teszt-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6d112-141">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


