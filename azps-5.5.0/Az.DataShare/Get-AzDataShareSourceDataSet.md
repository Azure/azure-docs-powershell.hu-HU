---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: 5f10289a5890ffa0e2764c475d65a0d5103b705e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209767"
---
# <span data-ttu-id="63748-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="63748-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="63748-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63748-102">SYNOPSIS</span></span>
<span data-ttu-id="63748-103">Információkat kap a forrásadat-készletekről a megosztási előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="63748-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="63748-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="63748-104">SYNTAX</span></span>

### <span data-ttu-id="63748-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="63748-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63748-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63748-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63748-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="63748-107">DESCRIPTION</span></span>
<span data-ttu-id="63748-108">A **Get-AzDataShareSourceDataSet** parancsmag információt nyújt a megosztási előfizetésben szereplő forrásadatkészletekkel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="63748-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="63748-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="63748-109">EXAMPLES</span></span>

### <span data-ttu-id="63748-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="63748-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="63748-111">A forrás megosztásban elérhető adatkészletek lekérhetők</span><span class="sxs-lookup"><span data-stu-id="63748-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="63748-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63748-112">PARAMETERS</span></span>

### <span data-ttu-id="63748-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="63748-113">-AccountName</span></span>
<span data-ttu-id="63748-114">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="63748-114">Azure data share account name</span></span>

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

### <span data-ttu-id="63748-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63748-115">-DefaultProfile</span></span>
<span data-ttu-id="63748-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63748-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63748-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63748-117">-ResourceGroupName</span></span>
<span data-ttu-id="63748-118">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="63748-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="63748-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="63748-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="63748-120">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="63748-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="63748-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="63748-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="63748-122">Azure data share subscription resource id</span><span class="sxs-lookup"><span data-stu-id="63748-122">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="63748-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63748-123">CommonParameters</span></span>
<span data-ttu-id="63748-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63748-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63748-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63748-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63748-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63748-126">INPUTS</span></span>

### <span data-ttu-id="63748-127">System.String</span><span class="sxs-lookup"><span data-stu-id="63748-127">System.String</span></span>

## <span data-ttu-id="63748-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63748-128">OUTPUTS</span></span>

### <span data-ttu-id="63748-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="63748-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="63748-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="63748-130">NOTES</span></span>

## <span data-ttu-id="63748-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63748-131">RELATED LINKS</span></span>
