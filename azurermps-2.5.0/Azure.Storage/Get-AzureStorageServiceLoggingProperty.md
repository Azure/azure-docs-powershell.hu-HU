---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
ms.openlocfilehash: f43386ff1eca223e8ff0e1e8ea7a07d1d8e25d0d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848573"
---
# <span data-ttu-id="aa05f-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="aa05f-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="aa05f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa05f-102">SYNOPSIS</span></span>
<span data-ttu-id="aa05f-103">Az Azure Storage Services naplózási tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="aa05f-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa05f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa05f-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa05f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa05f-105">DESCRIPTION</span></span>
<span data-ttu-id="aa05f-106">A **Get-AzureStorageServiceLoggingProperty** parancsmag az Azure Storage Services naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aa05f-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="aa05f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aa05f-107">EXAMPLES</span></span>

### <span data-ttu-id="aa05f-108">Példa 1: a blob-szolgáltatás naplózási tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="aa05f-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="aa05f-109">Ez a parancs a blob-tároló naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aa05f-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="aa05f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa05f-110">PARAMETERS</span></span>

### <span data-ttu-id="aa05f-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="aa05f-111">-Context</span></span>
<span data-ttu-id="aa05f-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa05f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="aa05f-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="aa05f-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="aa05f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa05f-114">-DefaultProfile</span></span>
<span data-ttu-id="aa05f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa05f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa05f-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="aa05f-116">-ServiceType</span></span>
<span data-ttu-id="aa05f-117">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa05f-117">Specifies the storage service type.</span></span>
<span data-ttu-id="aa05f-118">Ez a parancsmag a paraméter által megadott szolgáltatási típus naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aa05f-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="aa05f-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="aa05f-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aa05f-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="aa05f-120">Blob</span></span> 
- <span data-ttu-id="aa05f-121">Táblázat</span><span class="sxs-lookup"><span data-stu-id="aa05f-121">Table</span></span>
- <span data-ttu-id="aa05f-122">Várólista</span><span class="sxs-lookup"><span data-stu-id="aa05f-122">Queue</span></span>
- <span data-ttu-id="aa05f-123">Fájl: a fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="aa05f-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="aa05f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa05f-124">CommonParameters</span></span>
<span data-ttu-id="aa05f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa05f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa05f-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa05f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa05f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa05f-127">INPUTS</span></span>

### <span data-ttu-id="aa05f-128">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="aa05f-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="aa05f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa05f-129">OUTPUTS</span></span>

### <span data-ttu-id="aa05f-130">Microsoft. WindowsAzure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="aa05f-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="aa05f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa05f-131">NOTES</span></span>

## <span data-ttu-id="aa05f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa05f-132">RELATED LINKS</span></span>

[<span data-ttu-id="aa05f-133">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="aa05f-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="aa05f-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="aa05f-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


