---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
ms.openlocfilehash: a36b1f13f08cd94339f9791512d764a872019672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498648"
---
# <span data-ttu-id="529b0-101">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="529b0-101">Get-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="529b0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="529b0-102">SYNOPSIS</span></span>
<span data-ttu-id="529b0-103">Az Azure Storage Services tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="529b0-103">Gets properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="529b0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="529b0-104">SYNTAX</span></span>

```
Get-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="529b0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="529b0-105">DESCRIPTION</span></span>
<span data-ttu-id="529b0-106">A **Get-AzureStorageServiceProperty** parancsmag az Azure Storage Services tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="529b0-106">The **Get-AzureStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="529b0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="529b0-107">EXAMPLES</span></span>

### <span data-ttu-id="529b0-108">Példa 1: az Azure Storage Services tulajdonság beszerzése a blob-szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="529b0-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceProperty -ServiceType Blob

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

<span data-ttu-id="529b0-109">Ez a parancs a Paca szolgáltatás DefaultServiceVersion tulajdonságát kapja.</span><span class="sxs-lookup"><span data-stu-id="529b0-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="529b0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="529b0-110">PARAMETERS</span></span>

### <span data-ttu-id="529b0-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="529b0-111">-Context</span></span>
<span data-ttu-id="529b0-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="529b0-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="529b0-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="529b0-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="529b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="529b0-114">-DefaultProfile</span></span>
<span data-ttu-id="529b0-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="529b0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529b0-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="529b0-116">-ServiceType</span></span>
<span data-ttu-id="529b0-117">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="529b0-117">Specifies the storage service type.</span></span>
<span data-ttu-id="529b0-118">Ez a parancsmag a paraméter által megadott szolgáltatási típus naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="529b0-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="529b0-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="529b0-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="529b0-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="529b0-120">Blob</span></span> 
- <span data-ttu-id="529b0-121">Táblázat</span><span class="sxs-lookup"><span data-stu-id="529b0-121">Table</span></span>
- <span data-ttu-id="529b0-122">Várólista</span><span class="sxs-lookup"><span data-stu-id="529b0-122">Queue</span></span>
- <span data-ttu-id="529b0-123">Fájl</span><span class="sxs-lookup"><span data-stu-id="529b0-123">File</span></span>

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

### <span data-ttu-id="529b0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="529b0-124">CommonParameters</span></span>
<span data-ttu-id="529b0-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="529b0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="529b0-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="529b0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="529b0-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="529b0-127">INPUTS</span></span>

### <span data-ttu-id="529b0-128">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="529b0-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="529b0-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="529b0-129">OUTPUTS</span></span>

### <span data-ttu-id="529b0-130">Microsoft. WindowsAzure. Command. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="529b0-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="529b0-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="529b0-131">NOTES</span></span>

## <span data-ttu-id="529b0-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="529b0-132">RELATED LINKS</span></span>
