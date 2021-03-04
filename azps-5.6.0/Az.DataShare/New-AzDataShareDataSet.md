---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 12c0c4832d13e3e8637ab1cdb36a1f3fe3abb7d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927233"
---
# <span data-ttu-id="8761a-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="8761a-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="8761a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8761a-102">SYNOPSIS</span></span>
<span data-ttu-id="8761a-103">Adatkészleteket ad hozzá az Azure-adatok megosztásához.</span><span class="sxs-lookup"><span data-stu-id="8761a-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="8761a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8761a-104">SYNTAX</span></span>

### <span data-ttu-id="8761a-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8761a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8761a-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="8761a-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8761a-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="8761a-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8761a-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="8761a-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8761a-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8761a-109">DESCRIPTION</span></span>
<span data-ttu-id="8761a-110">A **New-AzDataShareDataSet** parancsmag adatkészleteket ad hozzá az adatmegosztási fiók Azure-adatmegosztásához.</span><span class="sxs-lookup"><span data-stu-id="8761a-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="8761a-111">Hozzáadhat blob, ADLS Gen2 és ADLS Gen1 típusú adatkészleteket.</span><span class="sxs-lookup"><span data-stu-id="8761a-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="8761a-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8761a-112">EXAMPLES</span></span>

### <span data-ttu-id="8761a-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="8761a-113">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="8761a-114">Ez a parancs hozzáad egy AdsDataSet nevű, típus blobtárolót tartalmazó adatkészletet az Azure-beli adatokat tároló AdsShare szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="8761a-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="8761a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8761a-115">PARAMETERS</span></span>

### <span data-ttu-id="8761a-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8761a-116">-AccountName</span></span>
<span data-ttu-id="8761a-117">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="8761a-117">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8761a-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="8761a-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="8761a-119">Azure storage ADLS gen1 mappa elérési útja</span><span class="sxs-lookup"><span data-stu-id="8761a-119">Azure storage ADLS gen1 folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8761a-120">-Container</span><span class="sxs-lookup"><span data-stu-id="8761a-120">-Container</span></span>
<span data-ttu-id="8761a-121">Azure-tárfiók tárolóneve</span><span class="sxs-lookup"><span data-stu-id="8761a-121">Azure storage account container name</span></span>

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

### <span data-ttu-id="8761a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8761a-122">-DefaultProfile</span></span>
<span data-ttu-id="8761a-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8761a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8761a-124">-FileName</span><span class="sxs-lookup"><span data-stu-id="8761a-124">-FileName</span></span>
<span data-ttu-id="8761a-125">Azure storage ADLS gen1 fájlnév</span><span class="sxs-lookup"><span data-stu-id="8761a-125">Azure storage ADLS gen1 file name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8761a-126">-FilePath</span><span class="sxs-lookup"><span data-stu-id="8761a-126">-FilePath</span></span>
<span data-ttu-id="8761a-127">Azure-tárterület elérési útja</span><span class="sxs-lookup"><span data-stu-id="8761a-127">Azure storage file path</span></span>

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

### <span data-ttu-id="8761a-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="8761a-128">-FileSystem</span></span>
<span data-ttu-id="8761a-129">Azure ADLS gen2 fájlrendszer neve</span><span class="sxs-lookup"><span data-stu-id="8761a-129">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="8761a-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="8761a-130">-FolderPath</span></span>
<span data-ttu-id="8761a-131">Azure-tármappa elérési útja</span><span class="sxs-lookup"><span data-stu-id="8761a-131">Azure storage folder path</span></span>

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

### <span data-ttu-id="8761a-132">-Name</span><span class="sxs-lookup"><span data-stu-id="8761a-132">-Name</span></span>
<span data-ttu-id="8761a-133">Azure-adatkészlet neve</span><span class="sxs-lookup"><span data-stu-id="8761a-133">Azure data set name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8761a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8761a-134">-ResourceGroupName</span></span>
<span data-ttu-id="8761a-135">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="8761a-135">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8761a-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8761a-136">-ShareName</span></span>
<span data-ttu-id="8761a-137">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="8761a-137">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8761a-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8761a-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="8761a-139">Azure-tárfiók erőforrásazonosítója</span><span class="sxs-lookup"><span data-stu-id="8761a-139">Azure storage account resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8761a-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8761a-140">-Confirm</span></span>
<span data-ttu-id="8761a-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8761a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8761a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8761a-142">-WhatIf</span></span>
<span data-ttu-id="8761a-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8761a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8761a-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8761a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8761a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8761a-145">CommonParameters</span></span>
<span data-ttu-id="8761a-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8761a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8761a-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8761a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8761a-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8761a-148">INPUTS</span></span>

### <span data-ttu-id="8761a-149">System.String</span><span class="sxs-lookup"><span data-stu-id="8761a-149">System.String</span></span>

## <span data-ttu-id="8761a-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8761a-150">OUTPUTS</span></span>

### <span data-ttu-id="8761a-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="8761a-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="8761a-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8761a-152">NOTES</span></span>

## <span data-ttu-id="8761a-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8761a-153">RELATED LINKS</span></span>
