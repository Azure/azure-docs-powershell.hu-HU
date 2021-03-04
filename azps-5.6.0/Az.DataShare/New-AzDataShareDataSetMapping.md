---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 56c573f6806acf2d9c45f583bbbb880aa6fc5638
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941866"
---
# <span data-ttu-id="612c5-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="612c5-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="612c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="612c5-102">SYNOPSIS</span></span>
<span data-ttu-id="612c5-103">Adatkészlet-megfeleltetést hoz létre a megosztási előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="612c5-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="612c5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="612c5-104">SYNTAX</span></span>

### <span data-ttu-id="612c5-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="612c5-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="612c5-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="612c5-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="612c5-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="612c5-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="612c5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="612c5-108">DESCRIPTION</span></span>
<span data-ttu-id="612c5-109">A **New-AzDataShareDataSetMapping** parancsmag létrehoz egy adatkészlet-megfeleltetést a forrásadatkészletek és a tárfiók között a megosztási előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="612c5-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="612c5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="612c5-110">EXAMPLES</span></span>

### <span data-ttu-id="612c5-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="612c5-111">Example 1</span></span>
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

<span data-ttu-id="612c5-112">Ez a parancs létrehoz egy adatkészletet, amely megfeleltetést hoz létre a AdsDataSetMapping és a storage account AdsStorage számára a share subscription AdsShareSubscription esetén a WikiAdsAccount adatmegosztási fiókban.</span><span class="sxs-lookup"><span data-stu-id="612c5-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="612c5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="612c5-113">PARAMETERS</span></span>

### <span data-ttu-id="612c5-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="612c5-114">-AccountName</span></span>
<span data-ttu-id="612c5-115">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="612c5-115">Azure data share account name</span></span>

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

### <span data-ttu-id="612c5-116">-Container</span><span class="sxs-lookup"><span data-stu-id="612c5-116">-Container</span></span>
<span data-ttu-id="612c5-117">Azure-tárfiók tárolóneve</span><span class="sxs-lookup"><span data-stu-id="612c5-117">Azure storage account container name</span></span>

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

### <span data-ttu-id="612c5-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="612c5-118">-DataSetId</span></span>
<span data-ttu-id="612c5-119">Fogyasztói adatkészlet azonosítója</span><span class="sxs-lookup"><span data-stu-id="612c5-119">Consumer data set id</span></span>

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

### <span data-ttu-id="612c5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="612c5-120">-DefaultProfile</span></span>
<span data-ttu-id="612c5-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="612c5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="612c5-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="612c5-122">-FilePath</span></span>
<span data-ttu-id="612c5-123">Azure-tárterület elérési útja</span><span class="sxs-lookup"><span data-stu-id="612c5-123">Azure storage file path</span></span>

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

### <span data-ttu-id="612c5-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="612c5-124">-FileSystem</span></span>
<span data-ttu-id="612c5-125">Azure ADLS gen2 fájlrendszer neve</span><span class="sxs-lookup"><span data-stu-id="612c5-125">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="612c5-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="612c5-126">-FolderPath</span></span>
<span data-ttu-id="612c5-127">Azure-tármappa elérési útja</span><span class="sxs-lookup"><span data-stu-id="612c5-127">Azure storage folder path</span></span>

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

### <span data-ttu-id="612c5-128">-Name</span><span class="sxs-lookup"><span data-stu-id="612c5-128">-Name</span></span>
<span data-ttu-id="612c5-129">Azure data set mapping name</span><span class="sxs-lookup"><span data-stu-id="612c5-129">Azure data set mapping name</span></span>

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

### <span data-ttu-id="612c5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="612c5-130">-ResourceGroupName</span></span>
<span data-ttu-id="612c5-131">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="612c5-131">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="612c5-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="612c5-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="612c5-133">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="612c5-133">Azure data share subscription name</span></span>

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

### <span data-ttu-id="612c5-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="612c5-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="612c5-135">Azure Storage Account ResourceId</span><span class="sxs-lookup"><span data-stu-id="612c5-135">Azure Storage Account ResourceId</span></span>

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

### <span data-ttu-id="612c5-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="612c5-136">-Confirm</span></span>
<span data-ttu-id="612c5-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="612c5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="612c5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="612c5-138">-WhatIf</span></span>
<span data-ttu-id="612c5-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="612c5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="612c5-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="612c5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="612c5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="612c5-141">CommonParameters</span></span>
<span data-ttu-id="612c5-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="612c5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="612c5-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="612c5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="612c5-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="612c5-144">INPUTS</span></span>

### <span data-ttu-id="612c5-145">System.String</span><span class="sxs-lookup"><span data-stu-id="612c5-145">System.String</span></span>

## <span data-ttu-id="612c5-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="612c5-146">OUTPUTS</span></span>

### <span data-ttu-id="612c5-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="612c5-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="612c5-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="612c5-148">NOTES</span></span>

## <span data-ttu-id="612c5-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="612c5-149">RELATED LINKS</span></span>
