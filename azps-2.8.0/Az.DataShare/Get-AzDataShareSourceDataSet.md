---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: e6f4562daf77204a96991ddeef9164f2f6aff17a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666732"
---
# <span data-ttu-id="38bda-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="38bda-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="38bda-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38bda-102">SYNOPSIS</span></span>
<span data-ttu-id="38bda-103">A megosztási előfizetésben lévő forrásadatok-halmazokra vonatkozó információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="38bda-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="38bda-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38bda-104">SYNTAX</span></span>

### <span data-ttu-id="38bda-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38bda-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38bda-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38bda-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38bda-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="38bda-107">DESCRIPTION</span></span>
<span data-ttu-id="38bda-108">A **Get-AzDataShareSourceDataSet** parancsmag információkat nyújt a megosztási előfizetéshez tartozó forrásadatok-készletekről.</span><span class="sxs-lookup"><span data-stu-id="38bda-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="38bda-109">Példák</span><span class="sxs-lookup"><span data-stu-id="38bda-109">EXAMPLES</span></span>

### <span data-ttu-id="38bda-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="38bda-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="38bda-111">A forrás megosztásban elérhető adatkészletek beolvasása</span><span class="sxs-lookup"><span data-stu-id="38bda-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="38bda-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38bda-112">PARAMETERS</span></span>

### <span data-ttu-id="38bda-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="38bda-113">-AccountName</span></span>
<span data-ttu-id="38bda-114">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="38bda-114">Azure data share account name</span></span>

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

### <span data-ttu-id="38bda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38bda-115">-DefaultProfile</span></span>
<span data-ttu-id="38bda-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38bda-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38bda-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38bda-117">-ResourceGroupName</span></span>
<span data-ttu-id="38bda-118">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="38bda-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="38bda-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="38bda-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="38bda-120">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="38bda-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="38bda-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="38bda-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="38bda-122">Azure Data Share-előfizetés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="38bda-122">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="38bda-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38bda-123">CommonParameters</span></span>
<span data-ttu-id="38bda-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38bda-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38bda-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38bda-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38bda-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38bda-126">INPUTS</span></span>

### <span data-ttu-id="38bda-127">System. String</span><span class="sxs-lookup"><span data-stu-id="38bda-127">System.String</span></span>

## <span data-ttu-id="38bda-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38bda-128">OUTPUTS</span></span>

### <span data-ttu-id="38bda-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="38bda-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="38bda-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38bda-130">NOTES</span></span>

## <span data-ttu-id="38bda-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38bda-131">RELATED LINKS</span></span>
