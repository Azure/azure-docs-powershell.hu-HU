---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: 49917b7d9719e682060c8a3cf24c30bbb9141874
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297494"
---
# <span data-ttu-id="a3fab-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="a3fab-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="a3fab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3fab-102">SYNOPSIS</span></span>
<span data-ttu-id="a3fab-103">Információkat kaphat a megosztási előfizetés synchonization részleteiről.</span><span class="sxs-lookup"><span data-stu-id="a3fab-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="a3fab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3fab-104">SYNTAX</span></span>

### <span data-ttu-id="a3fab-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a3fab-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3fab-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3fab-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3fab-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3fab-107">DESCRIPTION</span></span>
<span data-ttu-id="a3fab-108">A **Get-AzDataShareSubscriptionSynchronizationDetail** parancsmag a megosztási előfizetéshez kezdeményezett szinkronizálás részleteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a3fab-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="a3fab-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a3fab-109">EXAMPLES</span></span>

### <span data-ttu-id="a3fab-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a3fab-110">Example 1</span></span>
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

<span data-ttu-id="a3fab-111">Ez a parancs információkat nyújt az adatmegosztási fiók WikiAds az előfizetés megosztásához kezdeményezett szinkronizálási AdsShareSubscription.</span><span class="sxs-lookup"><span data-stu-id="a3fab-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="a3fab-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3fab-112">PARAMETERS</span></span>

### <span data-ttu-id="a3fab-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a3fab-113">-AccountName</span></span>
<span data-ttu-id="a3fab-114">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="a3fab-114">Azure data share account name</span></span>

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

### <span data-ttu-id="a3fab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3fab-115">-DefaultProfile</span></span>
<span data-ttu-id="a3fab-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3fab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3fab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3fab-117">-ResourceGroupName</span></span>
<span data-ttu-id="a3fab-118">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="a3fab-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a3fab-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3fab-119">-ResourceId</span></span>
<span data-ttu-id="a3fab-120">Azure Data Share-előfizetés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="a3fab-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="a3fab-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a3fab-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="a3fab-122">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="a3fab-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="a3fab-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="a3fab-123">-SynchronizationId</span></span>
<span data-ttu-id="a3fab-124">Az előfizetés megosztásának szinkronizálási azonosítója</span><span class="sxs-lookup"><span data-stu-id="a3fab-124">Synchronization id of share subscription synchronization</span></span>

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

### <span data-ttu-id="a3fab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3fab-125">CommonParameters</span></span>
<span data-ttu-id="a3fab-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3fab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3fab-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a3fab-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3fab-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3fab-128">INPUTS</span></span>

### <span data-ttu-id="a3fab-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a3fab-129">System.String</span></span>

## <span data-ttu-id="a3fab-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3fab-130">OUTPUTS</span></span>

### <span data-ttu-id="a3fab-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="a3fab-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="a3fab-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3fab-132">NOTES</span></span>

## <span data-ttu-id="a3fab-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3fab-133">RELATED LINKS</span></span>
