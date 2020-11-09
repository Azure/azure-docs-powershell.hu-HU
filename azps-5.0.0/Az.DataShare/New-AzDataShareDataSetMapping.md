---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 5792aeb937f82d3d80c0a6a7aea11e1ad0497970
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297446"
---
# <span data-ttu-id="b6eb8-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="b6eb8-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="b6eb8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="b6eb8-103">Adatkészlet-megfeleltetést hoz létre a megosztási előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="b6eb8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6eb8-104">SYNTAX</span></span>

### <span data-ttu-id="b6eb8-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b6eb8-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6eb8-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="b6eb8-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6eb8-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6eb8-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6eb8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6eb8-108">DESCRIPTION</span></span>
<span data-ttu-id="b6eb8-109">A **New-AzDataShareDataSetMapping** parancsmag adathalmaz-megfeleltetést hoz létre a forrásadatok és a mosogató tárolási fiók között a megosztási előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="b6eb8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b6eb8-110">EXAMPLES</span></span>

### <span data-ttu-id="b6eb8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b6eb8-111">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccoutName "WikiAdsAccount" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsDataSetMapping" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName        : AdsContainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : AdsStorage
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/AdsShareSubscription/dataSetMappings/AdsDataSetMapping
Name                 : AdsDataSetMapping
Type                 : Microsoft.DataShare/DataSetMappings
```

<span data-ttu-id="b6eb8-112">Ez a parancs létrehoz egy adathalmaz-megfeleltetési AdsDataSetMapping az adatmegosztási fiók AdsStorage-AdsShareSubscription az adatmegosztási fiók WikiAdsAccount.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="b6eb8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6eb8-113">PARAMETERS</span></span>

### <span data-ttu-id="b6eb8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b6eb8-114">-AccountName</span></span>
<span data-ttu-id="b6eb8-115">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="b6eb8-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6eb8-116">-Container</span><span class="sxs-lookup"><span data-stu-id="b6eb8-116">-Container</span></span>
<span data-ttu-id="b6eb8-117">Azure Storage fiók tárolójának neve</span><span class="sxs-lookup"><span data-stu-id="b6eb8-117">Azure storage account container name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6eb8-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="b6eb8-118">-DataSetId</span></span>
<span data-ttu-id="b6eb8-119">Consumer Data Set azonosító</span><span class="sxs-lookup"><span data-stu-id="b6eb8-119">Consumer data set id</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6eb8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6eb8-120">-DefaultProfile</span></span>
<span data-ttu-id="b6eb8-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6eb8-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="b6eb8-122">-FilePath</span></span>
<span data-ttu-id="b6eb8-123">Azure Storage file path</span><span class="sxs-lookup"><span data-stu-id="b6eb8-123">Azure storage file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6eb8-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="b6eb8-124">-FileSystem</span></span>
<span data-ttu-id="b6eb8-125">Azure ADLS Gen2-fájl neve</span><span class="sxs-lookup"><span data-stu-id="b6eb8-125">Azure ADLS gen2 file system name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6eb8-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="b6eb8-126">-FolderPath</span></span>
<span data-ttu-id="b6eb8-127">Azure Storage mappa elérési útja</span><span class="sxs-lookup"><span data-stu-id="b6eb8-127">Azure storage folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6eb8-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b6eb8-128">-Name</span></span>
<span data-ttu-id="b6eb8-129">Azure Data Set megfeleltetés neve</span><span class="sxs-lookup"><span data-stu-id="b6eb8-129">Azure data set mapping name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6eb8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6eb8-130">-ResourceGroupName</span></span>
<span data-ttu-id="b6eb8-131">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="b6eb8-131">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6eb8-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b6eb8-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="b6eb8-133">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="b6eb8-133">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6eb8-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="b6eb8-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="b6eb8-135">Azure Storage Account ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6eb8-135">Azure Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6eb8-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6eb8-136">-Confirm</span></span>
<span data-ttu-id="b6eb8-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6eb8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6eb8-138">-WhatIf</span></span>
<span data-ttu-id="b6eb8-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6eb8-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6eb8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6eb8-141">CommonParameters</span></span>
<span data-ttu-id="b6eb8-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6eb8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6eb8-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b6eb8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6eb8-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6eb8-144">INPUTS</span></span>

### <span data-ttu-id="b6eb8-145">System. String</span><span class="sxs-lookup"><span data-stu-id="b6eb8-145">System.String</span></span>

## <span data-ttu-id="b6eb8-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6eb8-146">OUTPUTS</span></span>

### <span data-ttu-id="b6eb8-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="b6eb8-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="b6eb8-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6eb8-148">NOTES</span></span>

## <span data-ttu-id="b6eb8-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6eb8-149">RELATED LINKS</span></span>
