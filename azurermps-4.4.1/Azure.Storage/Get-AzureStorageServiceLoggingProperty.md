---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: a3981ba2b0759afec06bb4cf34bc1e086658765a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672084"
---
# <span data-ttu-id="e90eb-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e90eb-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="e90eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e90eb-102">SYNOPSIS</span></span>
<span data-ttu-id="e90eb-103">Az Azure Storage Services naplózási tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="e90eb-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e90eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e90eb-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="e90eb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e90eb-105">DESCRIPTION</span></span>
<span data-ttu-id="e90eb-106">A **Get-AzureStorageServiceLoggingProperty** parancsmag az Azure Storage Services naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e90eb-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="e90eb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e90eb-107">EXAMPLES</span></span>

### <span data-ttu-id="e90eb-108">Példa 1: a blob-szolgáltatás naplózási tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="e90eb-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="e90eb-109">Ez a parancs a blob-tároló naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e90eb-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="e90eb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e90eb-110">PARAMETERS</span></span>

### <span data-ttu-id="e90eb-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e90eb-111">-Context</span></span>
<span data-ttu-id="e90eb-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e90eb-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e90eb-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e90eb-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e90eb-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="e90eb-114">-ServiceType</span></span>
<span data-ttu-id="e90eb-115">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e90eb-115">Specifies the storage service type.</span></span>
<span data-ttu-id="e90eb-116">Ez a parancsmag a paraméter által megadott szolgáltatási típus naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e90eb-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="e90eb-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e90eb-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e90eb-118">BLOB</span><span class="sxs-lookup"><span data-stu-id="e90eb-118">Blob</span></span> 
- <span data-ttu-id="e90eb-119">Táblázat</span><span class="sxs-lookup"><span data-stu-id="e90eb-119">Table</span></span>
- <span data-ttu-id="e90eb-120">Várólista</span><span class="sxs-lookup"><span data-stu-id="e90eb-120">Queue</span></span>
- <span data-ttu-id="e90eb-121">Fájl</span><span class="sxs-lookup"><span data-stu-id="e90eb-121">File</span></span>

<span data-ttu-id="e90eb-122">A fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="e90eb-122">The value of File is not currently supported.</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e90eb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e90eb-123">CommonParameters</span></span>
<span data-ttu-id="e90eb-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e90eb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e90eb-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e90eb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e90eb-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e90eb-126">INPUTS</span></span>

### <span data-ttu-id="e90eb-127">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e90eb-127">IStorageContext</span></span>

<span data-ttu-id="e90eb-128">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e90eb-128">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="e90eb-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e90eb-129">OUTPUTS</span></span>

### <span data-ttu-id="e90eb-130">Microsoft. WindowsAzure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="e90eb-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="e90eb-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e90eb-131">NOTES</span></span>

## <span data-ttu-id="e90eb-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e90eb-132">RELATED LINKS</span></span>

[<span data-ttu-id="e90eb-133">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e90eb-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e90eb-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e90eb-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


