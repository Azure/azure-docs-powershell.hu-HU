---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: a25efdd89e99e52115ade8354d7e96f8ee7972ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938809"
---
# <span data-ttu-id="fd518-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="fd518-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="fd518-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd518-102">SYNOPSIS</span></span>
<span data-ttu-id="fd518-103">Információkat kap az adatkészlet-leképezésekről a megosztási előfizetésben</span><span class="sxs-lookup"><span data-stu-id="fd518-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="fd518-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd518-104">SYNTAX</span></span>

### <span data-ttu-id="fd518-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd518-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd518-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd518-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd518-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd518-107">DESCRIPTION</span></span>
<span data-ttu-id="fd518-108">A **Get-AzDataShareDataSetMapping** parancsmag információt kap egy adott adatkészlet megfeleltetésről, ha a név meg van adva.</span><span class="sxs-lookup"><span data-stu-id="fd518-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="fd518-109">Ellenkező esetben információkat kap egy megosztási előfizetésben található összes adatkészlet-megfeleltetésről.</span><span class="sxs-lookup"><span data-stu-id="fd518-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="fd518-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd518-110">EXAMPLES</span></span>

### <span data-ttu-id="fd518-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="fd518-111">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareSubscriptionName "WikiADS"

ContainerName        : testing
Prefix               : providercontainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : storageaccount
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/WikiADS/dataSetMappings/dsm
Name                 : dsm
Type                 : Microsoft.DataShare/DataSetMappings
```

 <span data-ttu-id="fd518-112">Ez a parancs információkat jelenít meg a megosztási előfizetésben található összes adatkészlet-megfeleltetésről.</span><span class="sxs-lookup"><span data-stu-id="fd518-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="fd518-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd518-113">PARAMETERS</span></span>

### <span data-ttu-id="fd518-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fd518-114">-AccountName</span></span>
<span data-ttu-id="fd518-115">Azure data share account name.</span><span class="sxs-lookup"><span data-stu-id="fd518-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="fd518-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd518-116">-DefaultProfile</span></span>
<span data-ttu-id="fd518-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd518-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd518-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fd518-118">-Name</span></span>
<span data-ttu-id="fd518-119">Azure-adatkészlet megfeleltetésének neve.</span><span class="sxs-lookup"><span data-stu-id="fd518-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="fd518-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd518-120">-ResourceGroupName</span></span>
<span data-ttu-id="fd518-121">Az Azure-adat-megosztási fiók erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="fd518-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="fd518-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd518-122">-ResourceId</span></span>
<span data-ttu-id="fd518-123">Az Azure-adatkészlet megfeleltetésének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fd518-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="fd518-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="fd518-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="fd518-125">Azure-adatok megosztására vonatkozó előfizetés neve.</span><span class="sxs-lookup"><span data-stu-id="fd518-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="fd518-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd518-126">CommonParameters</span></span>
<span data-ttu-id="fd518-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd518-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd518-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd518-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd518-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd518-129">INPUTS</span></span>

### <span data-ttu-id="fd518-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fd518-130">System.String</span></span>

## <span data-ttu-id="fd518-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd518-131">OUTPUTS</span></span>

### <span data-ttu-id="fd518-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="fd518-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="fd518-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd518-133">NOTES</span></span>

## <span data-ttu-id="fd518-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd518-134">RELATED LINKS</span></span>
