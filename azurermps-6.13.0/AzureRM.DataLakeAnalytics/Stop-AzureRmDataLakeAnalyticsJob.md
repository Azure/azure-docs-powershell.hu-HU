---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/stop-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 4fc5c20cf43fbafb89007328307c69d4820b2127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672962"
---
# <span data-ttu-id="4a3f3-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4a3f3-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="4a3f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="4a3f3-103">Feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="4a3f3-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a3f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a3f3-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a3f3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a3f3-105">DESCRIPTION</span></span>
<span data-ttu-id="4a3f3-106">A **stop-AzureRmDataLakeAnalyticsJob** parancsmag visszamondja az Azure Data-tó Analytics-munkáját.</span><span class="sxs-lookup"><span data-stu-id="4a3f3-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="4a3f3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4a3f3-107">EXAMPLES</span></span>

### <span data-ttu-id="4a3f3-108">Példa 1: feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="4a3f3-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="4a3f3-109">Ez a parancs lemondja a feladatot a megadott AZONOSÍTÓval.</span><span class="sxs-lookup"><span data-stu-id="4a3f3-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="4a3f3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a3f3-110">PARAMETERS</span></span>

### <span data-ttu-id="4a3f3-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="4a3f3-111">-Account</span></span>
<span data-ttu-id="4a3f3-112">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a3f3-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a3f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a3f3-113">-DefaultProfile</span></span>
<span data-ttu-id="4a3f3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4a3f3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a3f3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4a3f3-115">-Force</span></span>
<span data-ttu-id="4a3f3-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="4a3f3-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a3f3-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="4a3f3-117">-JobId</span></span>
<span data-ttu-id="4a3f3-118">A lemondani kívánt feladat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a3f3-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a3f3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a3f3-119">-PassThru</span></span>
<span data-ttu-id="4a3f3-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="4a3f3-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4a3f3-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4a3f3-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3f3-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4a3f3-122">-Confirm</span></span>
<span data-ttu-id="4a3f3-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4a3f3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a3f3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a3f3-124">-WhatIf</span></span>
<span data-ttu-id="4a3f3-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4a3f3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a3f3-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4a3f3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a3f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a3f3-127">CommonParameters</span></span>
<span data-ttu-id="4a3f3-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a3f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a3f3-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a3f3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a3f3-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a3f3-130">INPUTS</span></span>

### <span data-ttu-id="4a3f3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4a3f3-131">System.String</span></span>

### <span data-ttu-id="4a3f3-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="4a3f3-132">System.Guid</span></span>

### <span data-ttu-id="4a3f3-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4a3f3-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4a3f3-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a3f3-134">OUTPUTS</span></span>

### <span data-ttu-id="4a3f3-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a3f3-135">System.Boolean</span></span>

## <span data-ttu-id="4a3f3-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a3f3-136">NOTES</span></span>

## <span data-ttu-id="4a3f3-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a3f3-137">RELATED LINKS</span></span>

[<span data-ttu-id="4a3f3-138">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4a3f3-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="4a3f3-139">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4a3f3-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="4a3f3-140">Várjon-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4a3f3-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


