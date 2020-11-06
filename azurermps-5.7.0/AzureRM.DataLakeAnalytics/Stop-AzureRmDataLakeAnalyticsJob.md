---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/stop-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 956e263f402a3b6cb78631f8337d46fc1effdd98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495388"
---
# <span data-ttu-id="d318a-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d318a-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="d318a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d318a-102">SYNOPSIS</span></span>
<span data-ttu-id="d318a-103">Feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="d318a-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d318a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d318a-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d318a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d318a-105">DESCRIPTION</span></span>
<span data-ttu-id="d318a-106">A **stop-AzureRmDataLakeAnalyticsJob** parancsmag visszamondja az Azure Data-tó Analytics-munkáját.</span><span class="sxs-lookup"><span data-stu-id="d318a-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="d318a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d318a-107">EXAMPLES</span></span>

### <span data-ttu-id="d318a-108">Példa 1: feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="d318a-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="d318a-109">Ez a parancs lemondja a feladatot a megadott AZONOSÍTÓval.</span><span class="sxs-lookup"><span data-stu-id="d318a-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="d318a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d318a-110">PARAMETERS</span></span>

### <span data-ttu-id="d318a-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="d318a-111">-Account</span></span>
<span data-ttu-id="d318a-112">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d318a-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d318a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d318a-113">-DefaultProfile</span></span>
<span data-ttu-id="d318a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d318a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d318a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d318a-115">-Force</span></span>
<span data-ttu-id="d318a-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d318a-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d318a-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="d318a-117">-JobId</span></span>
<span data-ttu-id="d318a-118">A lemondani kívánt feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d318a-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d318a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d318a-119">-PassThru</span></span>
<span data-ttu-id="d318a-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d318a-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d318a-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="d318a-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d318a-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d318a-122">-Confirm</span></span>
<span data-ttu-id="d318a-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d318a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d318a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d318a-124">-WhatIf</span></span>
<span data-ttu-id="d318a-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d318a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d318a-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d318a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d318a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d318a-127">CommonParameters</span></span>
<span data-ttu-id="d318a-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d318a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d318a-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d318a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d318a-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d318a-130">INPUTS</span></span>

### <span data-ttu-id="d318a-131">GUID</span><span class="sxs-lookup"><span data-stu-id="d318a-131">Guid</span></span>
<span data-ttu-id="d318a-132">A ' JobId ' paraméter a pipeline "GUID" típusú értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d318a-132">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="d318a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d318a-133">OUTPUTS</span></span>

### <span data-ttu-id="d318a-134">bool</span><span class="sxs-lookup"><span data-stu-id="d318a-134">bool</span></span>
<span data-ttu-id="d318a-135">Ha a PassThru meg van adva, a művelet befejezésekor a True értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d318a-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="d318a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d318a-136">NOTES</span></span>

## <span data-ttu-id="d318a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d318a-137">RELATED LINKS</span></span>

[<span data-ttu-id="d318a-138">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d318a-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="d318a-139">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d318a-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="d318a-140">Várjon-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d318a-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


