---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: aff976a684f5a002e2b55f1282dd60756f21f2f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324935"
---
# <span data-ttu-id="48a9a-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="48a9a-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="48a9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="48a9a-103">Tulajdonságokat kap az Azure Storage-szolgáltatásokhoz.</span><span class="sxs-lookup"><span data-stu-id="48a9a-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="48a9a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="48a9a-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48a9a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="48a9a-105">DESCRIPTION</span></span>
<span data-ttu-id="48a9a-106">A **Get-AzStorageServiceProperty** parancsmag megkapja az Azure Storage-szolgáltatások tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="48a9a-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="48a9a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="48a9a-107">EXAMPLES</span></span>

### <span data-ttu-id="48a9a-108">1. példa: A Blob szolgáltatás Azure Storage Services tulajdonságának lekérte</span><span class="sxs-lookup"><span data-stu-id="48a9a-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
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

<span data-ttu-id="48a9a-109">Ez a parancs a Blob szolgáltatás DefaultServiceVersion tulajdonságát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="48a9a-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="48a9a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48a9a-110">PARAMETERS</span></span>

### <span data-ttu-id="48a9a-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="48a9a-111">-Context</span></span>
<span data-ttu-id="48a9a-112">Egy Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="48a9a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="48a9a-113">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="48a9a-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="48a9a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48a9a-114">-DefaultProfile</span></span>
<span data-ttu-id="48a9a-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48a9a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48a9a-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="48a9a-116">-ServiceType</span></span>
<span data-ttu-id="48a9a-117">A társzolgáltatás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="48a9a-117">Specifies the storage service type.</span></span>
<span data-ttu-id="48a9a-118">Ez a parancsmag a paraméter által megadott szolgáltatástípus naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="48a9a-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="48a9a-119">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="48a9a-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="48a9a-120">Blob</span><span class="sxs-lookup"><span data-stu-id="48a9a-120">Blob</span></span> 
- <span data-ttu-id="48a9a-121">Táblázat</span><span class="sxs-lookup"><span data-stu-id="48a9a-121">Table</span></span>
- <span data-ttu-id="48a9a-122">Várólistán</span><span class="sxs-lookup"><span data-stu-id="48a9a-122">Queue</span></span>
- <span data-ttu-id="48a9a-123">Fájl</span><span class="sxs-lookup"><span data-stu-id="48a9a-123">File</span></span>

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

### <span data-ttu-id="48a9a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48a9a-124">CommonParameters</span></span>
<span data-ttu-id="48a9a-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48a9a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48a9a-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48a9a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48a9a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48a9a-127">INPUTS</span></span>

### <span data-ttu-id="48a9a-128">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="48a9a-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="48a9a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48a9a-129">OUTPUTS</span></span>

### <span data-ttu-id="48a9a-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="48a9a-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="48a9a-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="48a9a-131">NOTES</span></span>

## <span data-ttu-id="48a9a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48a9a-132">RELATED LINKS</span></span>
