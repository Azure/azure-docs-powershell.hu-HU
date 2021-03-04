---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: eff94aac5ac9a1a71a12f31be81a1eb4c89bf73b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933306"
---
# <span data-ttu-id="d7b02-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d7b02-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="d7b02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7b02-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b02-103">Tulajdonságokat kap az Azure Storage-szolgáltatásokhoz.</span><span class="sxs-lookup"><span data-stu-id="d7b02-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="d7b02-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d7b02-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7b02-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d7b02-105">DESCRIPTION</span></span>
<span data-ttu-id="d7b02-106">A **Get-AzStorageServiceProperty** parancsmag megkapja az Azure Storage-szolgáltatások tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d7b02-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="d7b02-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d7b02-107">EXAMPLES</span></span>

### <span data-ttu-id="d7b02-108">1. példa: A Blob szolgáltatás Azure Storage Services tulajdonságának lekérte</span><span class="sxs-lookup"><span data-stu-id="d7b02-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceProperty -ServiceType Blob

Logging.Version                     : 1.0
Logging.LoggingOperations           : None
Logging.RetentionDays               : 
HourMetrics.Version                 : 1.0
HourMetrics.MetricsLevel            : ServiceAndApi
HourMetrics.RetentionDays           : 7
MinuteMetrics.Version               : 1.0
MinuteMetrics.MetricsLevel          : None
MinuteMetrics.RetentionDays         : 
DeleteRetentionPolicy.Enabled       : True
DeleteRetentionPolicy.RetentionDays : 70
Cors                                : 
DefaultServiceVersion               : 2017-07-29
```

<span data-ttu-id="d7b02-109">Ez a parancs a Blob szolgáltatás DefaultServiceVersion tulajdonságát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d7b02-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="d7b02-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7b02-110">PARAMETERS</span></span>

### <span data-ttu-id="d7b02-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d7b02-111">-Context</span></span>
<span data-ttu-id="d7b02-112">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7b02-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d7b02-113">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d7b02-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b02-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b02-114">-DefaultProfile</span></span>
<span data-ttu-id="d7b02-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7b02-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b02-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="d7b02-116">-ServiceType</span></span>
<span data-ttu-id="d7b02-117">A társzolgáltatás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d7b02-117">Specifies the storage service type.</span></span>
<span data-ttu-id="d7b02-118">Ez a parancsmag a paraméter által megadott szolgáltatástípus naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d7b02-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="d7b02-119">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="d7b02-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d7b02-120">Blob</span><span class="sxs-lookup"><span data-stu-id="d7b02-120">Blob</span></span> 
- <span data-ttu-id="d7b02-121">Táblázat</span><span class="sxs-lookup"><span data-stu-id="d7b02-121">Table</span></span>
- <span data-ttu-id="d7b02-122">Várólistán</span><span class="sxs-lookup"><span data-stu-id="d7b02-122">Queue</span></span>
- <span data-ttu-id="d7b02-123">Fájl</span><span class="sxs-lookup"><span data-stu-id="d7b02-123">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b02-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b02-124">CommonParameters</span></span>
<span data-ttu-id="d7b02-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7b02-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b02-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7b02-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b02-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7b02-127">INPUTS</span></span>

### <span data-ttu-id="d7b02-128">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d7b02-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d7b02-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7b02-129">OUTPUTS</span></span>

### <span data-ttu-id="d7b02-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="d7b02-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="d7b02-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d7b02-131">NOTES</span></span>

## <span data-ttu-id="d7b02-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7b02-132">RELATED LINKS</span></span>
