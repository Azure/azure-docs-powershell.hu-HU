---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d615c0a807c12640f20a72b97a2c11c2efcd5b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491725"
---
# <span data-ttu-id="91d0c-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="91d0c-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="91d0c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="91d0c-103">Az Azure Storage Services naplózási tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="91d0c-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="91d0c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91d0c-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="91d0c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="91d0c-105">DESCRIPTION</span></span>
<span data-ttu-id="91d0c-106">A **Get-AzureStorageServiceLoggingProperty** parancsmag az Azure Storage Services naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="91d0c-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="91d0c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="91d0c-107">EXAMPLES</span></span>

### <span data-ttu-id="91d0c-108">Példa 1: a blob-szolgáltatás naplózási tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="91d0c-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="91d0c-109">Ez a parancs a blob-tároló naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="91d0c-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="91d0c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91d0c-110">PARAMETERS</span></span>

### <span data-ttu-id="91d0c-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="91d0c-111">-Context</span></span>
<span data-ttu-id="91d0c-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91d0c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="91d0c-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="91d0c-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="91d0c-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="91d0c-114">-ServiceType</span></span>
<span data-ttu-id="91d0c-115">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="91d0c-115">Specifies the storage service type.</span></span>
<span data-ttu-id="91d0c-116">Ez a parancsmag a paraméter által megadott szolgáltatási típus naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="91d0c-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="91d0c-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="91d0c-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91d0c-118">BLOB</span><span class="sxs-lookup"><span data-stu-id="91d0c-118">Blob</span></span> 
- <span data-ttu-id="91d0c-119">Táblázat</span><span class="sxs-lookup"><span data-stu-id="91d0c-119">Table</span></span>
- <span data-ttu-id="91d0c-120">Várólista</span><span class="sxs-lookup"><span data-stu-id="91d0c-120">Queue</span></span>
- <span data-ttu-id="91d0c-121">Fájl</span><span class="sxs-lookup"><span data-stu-id="91d0c-121">File</span></span>

<span data-ttu-id="91d0c-122">A fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="91d0c-122">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="91d0c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d0c-123">CommonParameters</span></span>
<span data-ttu-id="91d0c-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91d0c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d0c-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91d0c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d0c-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91d0c-126">INPUTS</span></span>

## <span data-ttu-id="91d0c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91d0c-127">OUTPUTS</span></span>

## <span data-ttu-id="91d0c-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91d0c-128">NOTES</span></span>

## <span data-ttu-id="91d0c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91d0c-129">RELATED LINKS</span></span>

[<span data-ttu-id="91d0c-130">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="91d0c-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="91d0c-131">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="91d0c-131">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


