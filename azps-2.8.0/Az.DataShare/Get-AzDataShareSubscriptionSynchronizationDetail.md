---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: dfe0710be411f3739a888cd58d3c0a6ec5353cab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666724"
---
# <span data-ttu-id="02d5d-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="02d5d-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="02d5d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02d5d-102">SYNOPSIS</span></span>
<span data-ttu-id="02d5d-103">Információkat kaphat a megosztási előfizetés synchonization részleteiről.</span><span class="sxs-lookup"><span data-stu-id="02d5d-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="02d5d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02d5d-104">SYNTAX</span></span>

### <span data-ttu-id="02d5d-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02d5d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="02d5d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02d5d-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02d5d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="02d5d-107">DESCRIPTION</span></span>
<span data-ttu-id="02d5d-108">A **Get-AzDataShareSubscriptionSynchronizationDetail** parancsmag a megosztási előfizetéshez kezdeményezett szinkronizálás részleteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="02d5d-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="02d5d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="02d5d-109">EXAMPLES</span></span>

### <span data-ttu-id="02d5d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="02d5d-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId "a6ee5c8d-0ce0-485e-b2f2-966b187dc6c7"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="02d5d-111">Ez a parancs információkat nyújt az adatmegosztási fiók WikiAds az előfizetés megosztásához kezdeményezett szinkronizálási AdsShareSubscription.</span><span class="sxs-lookup"><span data-stu-id="02d5d-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="02d5d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02d5d-112">PARAMETERS</span></span>

### <span data-ttu-id="02d5d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="02d5d-113">-AccountName</span></span>
<span data-ttu-id="02d5d-114">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="02d5d-114">Azure data share account name</span></span>

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

### <span data-ttu-id="02d5d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d5d-115">-DefaultProfile</span></span>
<span data-ttu-id="02d5d-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02d5d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02d5d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02d5d-117">-ResourceGroupName</span></span>
<span data-ttu-id="02d5d-118">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="02d5d-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="02d5d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02d5d-119">-ResourceId</span></span>
<span data-ttu-id="02d5d-120">Azure Data Share-előfizetés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="02d5d-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="02d5d-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="02d5d-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="02d5d-122">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="02d5d-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="02d5d-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="02d5d-123">-SynchronizationId</span></span>
<span data-ttu-id="02d5d-124">Az előfizetés megosztásának szinkronizálási azonosítója</span><span class="sxs-lookup"><span data-stu-id="02d5d-124">Synchronization id of share subscription synchronization</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02d5d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d5d-125">CommonParameters</span></span>
<span data-ttu-id="02d5d-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02d5d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d5d-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02d5d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d5d-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02d5d-128">INPUTS</span></span>

### <span data-ttu-id="02d5d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="02d5d-129">System.String</span></span>

## <span data-ttu-id="02d5d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02d5d-130">OUTPUTS</span></span>

### <span data-ttu-id="02d5d-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="02d5d-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="02d5d-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02d5d-132">NOTES</span></span>

## <span data-ttu-id="02d5d-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02d5d-133">RELATED LINKS</span></span>
