---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: d0bf60bbfd13474270391afd6f01bc9ec8130b62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938810"
---
# <span data-ttu-id="1b608-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="1b608-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="1b608-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b608-102">SYNOPSIS</span></span>
<span data-ttu-id="1b608-103">Információkat kap az Azure-adat megosztásában található adatkészletekkel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="1b608-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="1b608-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1b608-104">SYNTAX</span></span>

### <span data-ttu-id="1b608-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1b608-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b608-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b608-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b608-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1b608-107">DESCRIPTION</span></span>
<span data-ttu-id="1b608-108">A **Get-AzDataShareDataSet** parancsmag információkat kap az Azure-adatmegosztási fiókban megosztott adatkészletekkel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="1b608-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="1b608-109">Ha megadja az adatkészlet nevét, ez a parancsmag információt kap az adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="1b608-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="1b608-110">Ha nem ad meg nevet, ez a parancsmag információt kap a megosztásban található összes adatkészletről. I</span><span class="sxs-lookup"><span data-stu-id="1b608-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="1b608-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1b608-111">EXAMPLES</span></span>

### <span data-ttu-id="1b608-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="1b608-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="1b608-113">Ez a parancs információkat jelenít meg az AdsDataSet adatkészletről a Share AdsShare szolgáltatásban az Azure-adatmegosztási fiók wikiAdsAccount és az ads erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="1b608-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="1b608-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b608-114">PARAMETERS</span></span>

### <span data-ttu-id="1b608-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1b608-115">-AccountName</span></span>
<span data-ttu-id="1b608-116">Azure data share account name.</span><span class="sxs-lookup"><span data-stu-id="1b608-116">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b608-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b608-117">-DefaultProfile</span></span>
<span data-ttu-id="1b608-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b608-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b608-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1b608-119">-Name</span></span>
<span data-ttu-id="1b608-120">Azure-adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="1b608-120">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b608-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b608-121">-ResourceGroupName</span></span>
<span data-ttu-id="1b608-122">Az Azure-adat-megosztási fiók erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="1b608-122">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b608-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b608-123">-ResourceId</span></span>
<span data-ttu-id="1b608-124">Az Azure-adatkészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1b608-124">The resource id of the azure data set.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b608-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1b608-125">-ShareName</span></span>
<span data-ttu-id="1b608-126">Azure-adatok megosztásának neve.</span><span class="sxs-lookup"><span data-stu-id="1b608-126">Azure data share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b608-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b608-127">CommonParameters</span></span>
<span data-ttu-id="1b608-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b608-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b608-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b608-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b608-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b608-130">INPUTS</span></span>

### <span data-ttu-id="1b608-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1b608-131">System.String</span></span>

## <span data-ttu-id="1b608-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b608-132">OUTPUTS</span></span>

### <span data-ttu-id="1b608-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="1b608-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="1b608-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1b608-134">NOTES</span></span>

## <span data-ttu-id="1b608-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b608-135">RELATED LINKS</span></span>
