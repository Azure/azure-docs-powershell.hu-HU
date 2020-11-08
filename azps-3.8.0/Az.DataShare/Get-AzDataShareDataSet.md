---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 73272c2afd0b3d8ef62a522f2e67f04854c2232e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010965"
---
# <span data-ttu-id="9da90-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="9da90-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="9da90-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9da90-102">SYNOPSIS</span></span>
<span data-ttu-id="9da90-103">Információt kap az Azure-adatmegosztásban lévő adatkészletekről.</span><span class="sxs-lookup"><span data-stu-id="9da90-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="9da90-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9da90-104">SYNTAX</span></span>

### <span data-ttu-id="9da90-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9da90-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9da90-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9da90-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9da90-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9da90-107">DESCRIPTION</span></span>
<span data-ttu-id="9da90-108">A **Get-AzDataShareDataSet** parancsmag információkat kaphat az Azure adatmegosztási fiókban tárolt adatkészletekről.</span><span class="sxs-lookup"><span data-stu-id="9da90-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="9da90-109">Ha megadja az adatkészlet nevét, ez a parancsmag információkat kap az adathalmazról.</span><span class="sxs-lookup"><span data-stu-id="9da90-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="9da90-110">Ha nem ad meg nevet, ez a parancsmag információkat kap a megosztásban lévő összes adathalmazról. Lehet</span><span class="sxs-lookup"><span data-stu-id="9da90-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="9da90-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9da90-111">EXAMPLES</span></span>

### <span data-ttu-id="9da90-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9da90-112">Example 1</span></span>
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

<span data-ttu-id="9da90-113">Ez a parancs megjeleníti az Azure-adatmegosztási fiók WikiAdsAccount és AdsShare-HIRDETÉSEIben az AdsDataSet-on tárolt adathalmazok adatait.</span><span class="sxs-lookup"><span data-stu-id="9da90-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="9da90-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9da90-114">PARAMETERS</span></span>

### <span data-ttu-id="9da90-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9da90-115">-AccountName</span></span>
<span data-ttu-id="9da90-116">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="9da90-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="9da90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da90-117">-DefaultProfile</span></span>
<span data-ttu-id="9da90-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9da90-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9da90-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9da90-119">-Name</span></span>
<span data-ttu-id="9da90-120">Azure-adathalmaz neve</span><span class="sxs-lookup"><span data-stu-id="9da90-120">Azure data set name.</span></span>

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

### <span data-ttu-id="9da90-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9da90-121">-ResourceGroupName</span></span>
<span data-ttu-id="9da90-122">Az Azure Data Share-fiók erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="9da90-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="9da90-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9da90-123">-ResourceId</span></span>
<span data-ttu-id="9da90-124">Az Azure-adathalmaz erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9da90-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="9da90-125">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="9da90-125">-ShareName</span></span>
<span data-ttu-id="9da90-126">Azure-adatmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="9da90-126">Azure data share name.</span></span>

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

### <span data-ttu-id="9da90-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da90-127">CommonParameters</span></span>
<span data-ttu-id="9da90-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9da90-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da90-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9da90-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da90-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9da90-130">INPUTS</span></span>

### <span data-ttu-id="9da90-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9da90-131">System.String</span></span>

## <span data-ttu-id="9da90-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9da90-132">OUTPUTS</span></span>

### <span data-ttu-id="9da90-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="9da90-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="9da90-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9da90-134">NOTES</span></span>

## <span data-ttu-id="9da90-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9da90-135">RELATED LINKS</span></span>
