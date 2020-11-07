---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: 6b7944f96eb3ccc67322593d9056b39e83ee9010
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843054"
---
# <span data-ttu-id="9bbc9-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="9bbc9-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="9bbc9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9bbc9-102">SYNOPSIS</span></span>
<span data-ttu-id="9bbc9-103">Az Azure Storage Services tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="9bbc9-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="9bbc9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9bbc9-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bbc9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9bbc9-105">DESCRIPTION</span></span>
<span data-ttu-id="9bbc9-106">A **Get-AzStorageServiceProperty** parancsmag az Azure Storage Services tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9bbc9-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="9bbc9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9bbc9-107">EXAMPLES</span></span>

### <span data-ttu-id="9bbc9-108">Példa 1: az Azure Storage Services tulajdonság beszerzése a blob-szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="9bbc9-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
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

<span data-ttu-id="9bbc9-109">Ez a parancs a Paca szolgáltatás DefaultServiceVersion tulajdonságát kapja.</span><span class="sxs-lookup"><span data-stu-id="9bbc9-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="9bbc9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9bbc9-110">PARAMETERS</span></span>

### <span data-ttu-id="9bbc9-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9bbc9-111">-Context</span></span>
<span data-ttu-id="9bbc9-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9bbc9-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9bbc9-113">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9bbc9-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9bbc9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bbc9-114">-DefaultProfile</span></span>
<span data-ttu-id="9bbc9-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9bbc9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bbc9-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="9bbc9-116">-ServiceType</span></span>
<span data-ttu-id="9bbc9-117">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9bbc9-117">Specifies the storage service type.</span></span>
<span data-ttu-id="9bbc9-118">Ez a parancsmag a paraméter által megadott szolgáltatási típus naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9bbc9-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="9bbc9-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9bbc9-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9bbc9-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="9bbc9-120">Blob</span></span> 
- <span data-ttu-id="9bbc9-121">Táblázat</span><span class="sxs-lookup"><span data-stu-id="9bbc9-121">Table</span></span>
- <span data-ttu-id="9bbc9-122">Várólista</span><span class="sxs-lookup"><span data-stu-id="9bbc9-122">Queue</span></span>
- <span data-ttu-id="9bbc9-123">Fájl</span><span class="sxs-lookup"><span data-stu-id="9bbc9-123">File</span></span>

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

### <span data-ttu-id="9bbc9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bbc9-124">CommonParameters</span></span>
<span data-ttu-id="9bbc9-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9bbc9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bbc9-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bbc9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bbc9-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bbc9-127">INPUTS</span></span>

### <span data-ttu-id="9bbc9-128">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9bbc9-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9bbc9-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bbc9-129">OUTPUTS</span></span>

### <span data-ttu-id="9bbc9-130">Microsoft. WindowsAzure. Command. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="9bbc9-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="9bbc9-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9bbc9-131">NOTES</span></span>

## <span data-ttu-id="9bbc9-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9bbc9-132">RELATED LINKS</span></span>
