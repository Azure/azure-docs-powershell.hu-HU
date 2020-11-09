---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 5dbf797ffabdf42b1d30d9d709ba6bb3153d8696
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297461"
---
# <span data-ttu-id="1f391-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="1f391-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="1f391-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f391-102">SYNOPSIS</span></span>
<span data-ttu-id="1f391-103">Adatkészleteket ad hozzá az Azure Data Share szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="1f391-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="1f391-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f391-104">SYNTAX</span></span>

### <span data-ttu-id="1f391-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1f391-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f391-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="1f391-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f391-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f391-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f391-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f391-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f391-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f391-109">DESCRIPTION</span></span>
<span data-ttu-id="1f391-110">A **New-AzDataShareDataSet** parancsmag adathalmazokat adhat meg az Azure adatmegosztási fiókjában.</span><span class="sxs-lookup"><span data-stu-id="1f391-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="1f391-111">A Paca, a ADLS Gen2 és a ADLS Gen1 adatkészleteket vehet fel.</span><span class="sxs-lookup"><span data-stu-id="1f391-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="1f391-112">Példák</span><span class="sxs-lookup"><span data-stu-id="1f391-112">EXAMPLES</span></span>

### <span data-ttu-id="1f391-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1f391-113">Example 1</span></span>
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

<span data-ttu-id="1f391-114">Ez a parancs a blob-tároló AdsDataSet az Azure Data Share AdsShare nevű adatkészletet szúrja be.</span><span class="sxs-lookup"><span data-stu-id="1f391-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="1f391-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f391-115">PARAMETERS</span></span>

### <span data-ttu-id="1f391-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1f391-116">-AccountName</span></span>
<span data-ttu-id="1f391-117">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="1f391-117">Azure data share account name</span></span>

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

### <span data-ttu-id="1f391-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="1f391-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="1f391-119">Azure Storage ADLS gen1 mappa elérési útja</span><span class="sxs-lookup"><span data-stu-id="1f391-119">Azure storage ADLS gen1 folder path</span></span>

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

### <span data-ttu-id="1f391-120">-Container</span><span class="sxs-lookup"><span data-stu-id="1f391-120">-Container</span></span>
<span data-ttu-id="1f391-121">Azure Storage fiók tárolójának neve</span><span class="sxs-lookup"><span data-stu-id="1f391-121">Azure storage account container name</span></span>

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

### <span data-ttu-id="1f391-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f391-122">-DefaultProfile</span></span>
<span data-ttu-id="1f391-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f391-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f391-124">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="1f391-124">-FileName</span></span>
<span data-ttu-id="1f391-125">Azure Storage ADLS gen1 fájlnév</span><span class="sxs-lookup"><span data-stu-id="1f391-125">Azure storage ADLS gen1 file name</span></span>

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

### <span data-ttu-id="1f391-126">-FilePath</span><span class="sxs-lookup"><span data-stu-id="1f391-126">-FilePath</span></span>
<span data-ttu-id="1f391-127">Azure Storage file path</span><span class="sxs-lookup"><span data-stu-id="1f391-127">Azure storage file path</span></span>

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

### <span data-ttu-id="1f391-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="1f391-128">-FileSystem</span></span>
<span data-ttu-id="1f391-129">Azure ADLS Gen2-fájl neve</span><span class="sxs-lookup"><span data-stu-id="1f391-129">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="1f391-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="1f391-130">-FolderPath</span></span>
<span data-ttu-id="1f391-131">Azure Storage mappa elérési útja</span><span class="sxs-lookup"><span data-stu-id="1f391-131">Azure storage folder path</span></span>

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

### <span data-ttu-id="1f391-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f391-132">-Name</span></span>
<span data-ttu-id="1f391-133">Azure-adathalmaz neve</span><span class="sxs-lookup"><span data-stu-id="1f391-133">Azure data set name</span></span>

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

### <span data-ttu-id="1f391-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f391-134">-ResourceGroupName</span></span>
<span data-ttu-id="1f391-135">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="1f391-135">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="1f391-136">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="1f391-136">-ShareName</span></span>
<span data-ttu-id="1f391-137">Azure-adatmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="1f391-137">Azure data share name</span></span>

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

### <span data-ttu-id="1f391-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="1f391-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="1f391-139">Azure Storage Account resourceId</span><span class="sxs-lookup"><span data-stu-id="1f391-139">Azure storage account resourceId</span></span>

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

### <span data-ttu-id="1f391-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1f391-140">-Confirm</span></span>
<span data-ttu-id="1f391-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1f391-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f391-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f391-142">-WhatIf</span></span>
<span data-ttu-id="1f391-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1f391-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f391-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f391-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f391-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f391-145">CommonParameters</span></span>
<span data-ttu-id="1f391-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f391-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f391-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1f391-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f391-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f391-148">INPUTS</span></span>

### <span data-ttu-id="1f391-149">System. String</span><span class="sxs-lookup"><span data-stu-id="1f391-149">System.String</span></span>

## <span data-ttu-id="1f391-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f391-150">OUTPUTS</span></span>

### <span data-ttu-id="1f391-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="1f391-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="1f391-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f391-152">NOTES</span></span>

## <span data-ttu-id="1f391-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f391-153">RELATED LINKS</span></span>
