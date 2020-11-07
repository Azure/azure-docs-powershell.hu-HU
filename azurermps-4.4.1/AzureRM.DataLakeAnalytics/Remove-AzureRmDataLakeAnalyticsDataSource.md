---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 9b0e4b5da6ecd2877bab5860179cbaed80f43911
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679482"
---
# <span data-ttu-id="9f46a-101">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="9f46a-101">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="9f46a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f46a-102">SYNOPSIS</span></span>
<span data-ttu-id="9f46a-103">Az adatforrások eltávolítása egy adattó-fiókból.</span><span class="sxs-lookup"><span data-stu-id="9f46a-103">Removes a data source from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f46a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f46a-104">SYNTAX</span></span>

### <span data-ttu-id="9f46a-105">Az adattó-tároló fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9f46a-105">Remove a Data Lake storage account</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f46a-106">BLOB-tároló fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9f46a-106">Remove a Blob storage account</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f46a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f46a-107">DESCRIPTION</span></span>
<span data-ttu-id="9f46a-108">A **Remove-AzureRmDataLakeAnalyticsDataSource** parancsmag az Azure Data Lake-alapú fiókokból származó adatforrásokat távolítja el.</span><span class="sxs-lookup"><span data-stu-id="9f46a-108">The **Remove-AzureRmDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="9f46a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9f46a-109">EXAMPLES</span></span>

### <span data-ttu-id="9f46a-110">1. példa: adatforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9f46a-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="9f46a-111">Ez a parancs eltávolítja a AzureStorage01 nevű adatforrást a ContosoAdlAccount nevű fiókból.</span><span class="sxs-lookup"><span data-stu-id="9f46a-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="9f46a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f46a-112">PARAMETERS</span></span>

### <span data-ttu-id="9f46a-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="9f46a-113">-Account</span></span>
<span data-ttu-id="9f46a-114">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f46a-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="9f46a-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="9f46a-115">-Blob</span></span>
<span data-ttu-id="9f46a-116">Az eltávolítandó AzureBlob-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f46a-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f46a-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9f46a-117">-DataLakeStore</span></span>
<span data-ttu-id="9f46a-118">Itt adhatja meg az eltávolítandó AzureData-tároló fiók nevét.</span><span class="sxs-lookup"><span data-stu-id="9f46a-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Data Lake storage account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f46a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9f46a-119">-Force</span></span>
<span data-ttu-id="9f46a-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="9f46a-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f46a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f46a-121">-PassThru</span></span>
<span data-ttu-id="9f46a-122">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9f46a-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9f46a-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9f46a-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9f46a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f46a-124">-ResourceGroupName</span></span>
<span data-ttu-id="9f46a-125">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f46a-125">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f46a-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9f46a-126">-Confirm</span></span>
<span data-ttu-id="9f46a-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9f46a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f46a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f46a-128">-WhatIf</span></span>
<span data-ttu-id="9f46a-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9f46a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f46a-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f46a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f46a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f46a-131">-DefaultProfile</span></span>
<span data-ttu-id="9f46a-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f46a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f46a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f46a-133">CommonParameters</span></span>
<span data-ttu-id="9f46a-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f46a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f46a-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f46a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f46a-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f46a-136">INPUTS</span></span>

## <span data-ttu-id="9f46a-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f46a-137">OUTPUTS</span></span>

### <span data-ttu-id="9f46a-138">bool</span><span class="sxs-lookup"><span data-stu-id="9f46a-138">bool</span></span>
<span data-ttu-id="9f46a-139">Ha a PassThru meg van adva, a művelet befejezésekor a True értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9f46a-139">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="9f46a-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f46a-140">NOTES</span></span>

## <span data-ttu-id="9f46a-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f46a-141">RELATED LINKS</span></span>

[<span data-ttu-id="9f46a-142">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="9f46a-142">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="9f46a-143">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="9f46a-143">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


