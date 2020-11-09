---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: dfdd338fd5b49813d17e089755b419605761af3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298034"
---
# <span data-ttu-id="dc98c-101">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="dc98c-101">Remove-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="dc98c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc98c-102">SYNOPSIS</span></span>
<span data-ttu-id="dc98c-103">Az adatforrások eltávolítása egy adattó-fiókból.</span><span class="sxs-lookup"><span data-stu-id="dc98c-103">Removes a data source from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="dc98c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc98c-104">SYNTAX</span></span>

### <span data-ttu-id="dc98c-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc98c-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc98c-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc98c-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc98c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc98c-107">DESCRIPTION</span></span>
<span data-ttu-id="dc98c-108">A **Remove-AzDataLakeAnalyticsDataSource** parancsmag az Azure Data Lake-alapú fiókokból származó adatforrásokat távolítja el.</span><span class="sxs-lookup"><span data-stu-id="dc98c-108">The **Remove-AzDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="dc98c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dc98c-109">EXAMPLES</span></span>

### <span data-ttu-id="dc98c-110">1. példa: adatforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dc98c-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="dc98c-111">Ez a parancs eltávolítja a AzureStorage01 nevű adatforrást a ContosoAdlAccount nevű fiókból.</span><span class="sxs-lookup"><span data-stu-id="dc98c-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="dc98c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc98c-112">PARAMETERS</span></span>

### <span data-ttu-id="dc98c-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="dc98c-113">-Account</span></span>
<span data-ttu-id="dc98c-114">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc98c-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="dc98c-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="dc98c-115">-Blob</span></span>
<span data-ttu-id="dc98c-116">Az eltávolítandó AzureBlob-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc98c-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

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

### <span data-ttu-id="dc98c-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc98c-117">-DataLakeStore</span></span>
<span data-ttu-id="dc98c-118">Itt adhatja meg az eltávolítandó AzureData-tároló fiók nevét.</span><span class="sxs-lookup"><span data-stu-id="dc98c-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

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

### <span data-ttu-id="dc98c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc98c-119">-DefaultProfile</span></span>
<span data-ttu-id="dc98c-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dc98c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc98c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="dc98c-121">-Force</span></span>
<span data-ttu-id="dc98c-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="dc98c-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dc98c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc98c-123">-PassThru</span></span>
<span data-ttu-id="dc98c-124">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="dc98c-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dc98c-125">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="dc98c-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dc98c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc98c-126">-ResourceGroupName</span></span>
<span data-ttu-id="dc98c-127">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc98c-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="dc98c-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dc98c-128">-Confirm</span></span>
<span data-ttu-id="dc98c-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dc98c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc98c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc98c-130">-WhatIf</span></span>
<span data-ttu-id="dc98c-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dc98c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc98c-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dc98c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc98c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc98c-133">CommonParameters</span></span>
<span data-ttu-id="dc98c-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc98c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc98c-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc98c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc98c-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc98c-136">INPUTS</span></span>

### <span data-ttu-id="dc98c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="dc98c-137">System.String</span></span>

## <span data-ttu-id="dc98c-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc98c-138">OUTPUTS</span></span>

### <span data-ttu-id="dc98c-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc98c-139">System.Boolean</span></span>

## <span data-ttu-id="dc98c-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc98c-140">NOTES</span></span>

## <span data-ttu-id="dc98c-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc98c-141">RELATED LINKS</span></span>

[<span data-ttu-id="dc98c-142">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="dc98c-142">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="dc98c-143">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="dc98c-143">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


