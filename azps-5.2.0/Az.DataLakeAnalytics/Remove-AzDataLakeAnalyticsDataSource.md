---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: dfdd338fd5b49813d17e089755b419605761af3a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362037"
---
# <span data-ttu-id="4662d-101">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="4662d-101">Remove-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="4662d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4662d-102">SYNOPSIS</span></span>
<span data-ttu-id="4662d-103">Eltávolít egy adatforrást egy Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="4662d-103">Removes a data source from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="4662d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4662d-104">SYNTAX</span></span>

### <span data-ttu-id="4662d-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4662d-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4662d-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4662d-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4662d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4662d-107">DESCRIPTION</span></span>
<span data-ttu-id="4662d-108">A **Remove-AzDataLakeAnalyticsDataSource** parancsmag eltávolít egy adatforrást egy Azure Data Lake Analytics-fiókból.</span><span class="sxs-lookup"><span data-stu-id="4662d-108">The **Remove-AzDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="4662d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4662d-109">EXAMPLES</span></span>

### <span data-ttu-id="4662d-110">1. példa: Adatforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4662d-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="4662d-111">Ez a parancs eltávolítja az AzureStorage01 nevű adatforrást a ContosoAdlAccount nevű fiókból.</span><span class="sxs-lookup"><span data-stu-id="4662d-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="4662d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4662d-112">PARAMETERS</span></span>

### <span data-ttu-id="4662d-113">-Account</span><span class="sxs-lookup"><span data-stu-id="4662d-113">-Account</span></span>
<span data-ttu-id="4662d-114">A Data Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4662d-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="4662d-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="4662d-115">-Blob</span></span>
<span data-ttu-id="4662d-116">Az eltávolítható AzureBlob-tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4662d-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4662d-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4662d-117">-DataLakeStore</span></span>
<span data-ttu-id="4662d-118">Az eltávolítható AzureData Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4662d-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4662d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4662d-119">-DefaultProfile</span></span>
<span data-ttu-id="4662d-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4662d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4662d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4662d-121">-Force</span></span>
<span data-ttu-id="4662d-122">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="4662d-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4662d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4662d-123">-PassThru</span></span>
<span data-ttu-id="4662d-124">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="4662d-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4662d-125">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4662d-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4662d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4662d-126">-ResourceGroupName</span></span>
<span data-ttu-id="4662d-127">A Data Lake Analytics-fiók erőforráscsoportnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4662d-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="4662d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4662d-128">-Confirm</span></span>
<span data-ttu-id="4662d-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4662d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4662d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4662d-130">-WhatIf</span></span>
<span data-ttu-id="4662d-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4662d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4662d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4662d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4662d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4662d-133">CommonParameters</span></span>
<span data-ttu-id="4662d-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4662d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4662d-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4662d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4662d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4662d-136">INPUTS</span></span>

### <span data-ttu-id="4662d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="4662d-137">System.String</span></span>

## <span data-ttu-id="4662d-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4662d-138">OUTPUTS</span></span>

### <span data-ttu-id="4662d-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4662d-139">System.Boolean</span></span>

## <span data-ttu-id="4662d-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4662d-140">NOTES</span></span>

## <span data-ttu-id="4662d-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4662d-141">RELATED LINKS</span></span>

[<span data-ttu-id="4662d-142">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="4662d-142">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="4662d-143">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="4662d-143">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


