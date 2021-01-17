---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 5792aeb937f82d3d80c0a6a7aea11e1ad0497970
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324389"
---
# <span data-ttu-id="51b53-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="51b53-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="51b53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51b53-102">SYNOPSIS</span></span>
<span data-ttu-id="51b53-103">Adatkészlet-megfeleltetést hoz létre a megosztási előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="51b53-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="51b53-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="51b53-104">SYNTAX</span></span>

### <span data-ttu-id="51b53-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51b53-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51b53-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="51b53-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51b53-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="51b53-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51b53-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="51b53-108">DESCRIPTION</span></span>
<span data-ttu-id="51b53-109">A **New-AzDataShareDataSetMapping** parancsmag adatkészlet-megfeleltetést hoz létre a forrásadatkészletek és a tárfiók között a megosztási előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="51b53-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="51b53-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="51b53-110">EXAMPLES</span></span>

### <span data-ttu-id="51b53-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="51b53-111">Example 1</span></span>
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

<span data-ttu-id="51b53-112">Ez a parancs létrehoz egy adatkészletet, amely megfeleltetést hoz létre az AdsDataSetMapping értéknek a Share Subscription AdsStorage tárhelyfiókjára vonatkozó AdsShareSubscription értékhez a WikiAdsAccount adatmegosztási fiókban.</span><span class="sxs-lookup"><span data-stu-id="51b53-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="51b53-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51b53-113">PARAMETERS</span></span>

### <span data-ttu-id="51b53-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="51b53-114">-AccountName</span></span>
<span data-ttu-id="51b53-115">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="51b53-115">Azure data share account name</span></span>

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

### <span data-ttu-id="51b53-116">-Container</span><span class="sxs-lookup"><span data-stu-id="51b53-116">-Container</span></span>
<span data-ttu-id="51b53-117">Azure-tárfiók tárolóneve</span><span class="sxs-lookup"><span data-stu-id="51b53-117">Azure storage account container name</span></span>

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

### <span data-ttu-id="51b53-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="51b53-118">-DataSetId</span></span>
<span data-ttu-id="51b53-119">Fogyasztói adatkészlet azonosítója</span><span class="sxs-lookup"><span data-stu-id="51b53-119">Consumer data set id</span></span>

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

### <span data-ttu-id="51b53-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b53-120">-DefaultProfile</span></span>
<span data-ttu-id="51b53-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51b53-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51b53-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="51b53-122">-FilePath</span></span>
<span data-ttu-id="51b53-123">Azure-tárterület elérési útja</span><span class="sxs-lookup"><span data-stu-id="51b53-123">Azure storage file path</span></span>

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

### <span data-ttu-id="51b53-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="51b53-124">-FileSystem</span></span>
<span data-ttu-id="51b53-125">Azure ADLS gen2 fájlrendszer neve</span><span class="sxs-lookup"><span data-stu-id="51b53-125">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="51b53-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="51b53-126">-FolderPath</span></span>
<span data-ttu-id="51b53-127">Azure-tármappa elérési útja</span><span class="sxs-lookup"><span data-stu-id="51b53-127">Azure storage folder path</span></span>

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

### <span data-ttu-id="51b53-128">-Name</span><span class="sxs-lookup"><span data-stu-id="51b53-128">-Name</span></span>
<span data-ttu-id="51b53-129">Azure-adatkészlet megfeleltetésének neve</span><span class="sxs-lookup"><span data-stu-id="51b53-129">Azure data set mapping name</span></span>

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

### <span data-ttu-id="51b53-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b53-130">-ResourceGroupName</span></span>
<span data-ttu-id="51b53-131">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="51b53-131">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="51b53-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="51b53-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="51b53-133">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="51b53-133">Azure data share subscription name</span></span>

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

### <span data-ttu-id="51b53-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="51b53-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="51b53-135">Azure Storage Account ResourceId</span><span class="sxs-lookup"><span data-stu-id="51b53-135">Azure Storage Account ResourceId</span></span>

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

### <span data-ttu-id="51b53-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51b53-136">-Confirm</span></span>
<span data-ttu-id="51b53-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="51b53-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51b53-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51b53-138">-WhatIf</span></span>
<span data-ttu-id="51b53-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="51b53-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51b53-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51b53-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51b53-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b53-141">CommonParameters</span></span>
<span data-ttu-id="51b53-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51b53-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b53-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51b53-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b53-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51b53-144">INPUTS</span></span>

### <span data-ttu-id="51b53-145">System.String</span><span class="sxs-lookup"><span data-stu-id="51b53-145">System.String</span></span>

## <span data-ttu-id="51b53-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51b53-146">OUTPUTS</span></span>

### <span data-ttu-id="51b53-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="51b53-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="51b53-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="51b53-148">NOTES</span></span>

## <span data-ttu-id="51b53-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51b53-149">RELATED LINKS</span></span>
