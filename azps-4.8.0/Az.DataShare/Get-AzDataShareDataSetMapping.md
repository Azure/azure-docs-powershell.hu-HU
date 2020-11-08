---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: 99f80aa920a402867b6385a3b4ef7ac118838f80
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183655"
---
# <span data-ttu-id="02b02-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="02b02-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="02b02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02b02-102">SYNOPSIS</span></span>
<span data-ttu-id="02b02-103">Információt kap az adatkészlet-megfeleltetésekről a megosztási előfizetésben</span><span class="sxs-lookup"><span data-stu-id="02b02-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="02b02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02b02-104">SYNTAX</span></span>

### <span data-ttu-id="02b02-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02b02-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02b02-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02b02-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02b02-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="02b02-107">DESCRIPTION</span></span>
<span data-ttu-id="02b02-108">A **Get-AzDataShareDataSetMapping** parancsmag információt kap egy adott adatkészlet-megfeleltetésről, ha a név meg van adva.</span><span class="sxs-lookup"><span data-stu-id="02b02-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="02b02-109">Ellenkező esetben az összes adatkészlet-megfeleltetésről információt kap egy megosztási előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="02b02-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="02b02-110">Példák</span><span class="sxs-lookup"><span data-stu-id="02b02-110">EXAMPLES</span></span>

### <span data-ttu-id="02b02-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="02b02-111">Example 1</span></span>
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

 <span data-ttu-id="02b02-112">Ez a parancs információt jelenít meg az összes adatkészlet-megfeleltetésről a megosztási előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="02b02-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="02b02-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02b02-113">PARAMETERS</span></span>

### <span data-ttu-id="02b02-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="02b02-114">-AccountName</span></span>
<span data-ttu-id="02b02-115">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="02b02-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="02b02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02b02-116">-DefaultProfile</span></span>
<span data-ttu-id="02b02-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02b02-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02b02-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="02b02-118">-Name</span></span>
<span data-ttu-id="02b02-119">Azure adathalmaz megfeleltetésének neve.</span><span class="sxs-lookup"><span data-stu-id="02b02-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="02b02-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02b02-120">-ResourceGroupName</span></span>
<span data-ttu-id="02b02-121">Az Azure Data Share-fiók erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="02b02-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="02b02-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02b02-122">-ResourceId</span></span>
<span data-ttu-id="02b02-123">Az Azure adathalmaz megfeleltetésének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="02b02-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="02b02-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="02b02-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="02b02-125">Azure Data Share (előfizetés neve)</span><span class="sxs-lookup"><span data-stu-id="02b02-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="02b02-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02b02-126">CommonParameters</span></span>
<span data-ttu-id="02b02-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02b02-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02b02-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="02b02-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02b02-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02b02-129">INPUTS</span></span>

### <span data-ttu-id="02b02-130">System. String</span><span class="sxs-lookup"><span data-stu-id="02b02-130">System.String</span></span>

## <span data-ttu-id="02b02-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02b02-131">OUTPUTS</span></span>

### <span data-ttu-id="02b02-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="02b02-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="02b02-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02b02-133">NOTES</span></span>

## <span data-ttu-id="02b02-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02b02-134">RELATED LINKS</span></span>
