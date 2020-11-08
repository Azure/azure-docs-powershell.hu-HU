---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 6e4eced11a9de228f836e80e9f25350e3f09a8c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186343"
---
# <span data-ttu-id="8c1a6-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8c1a6-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="8c1a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c1a6-102">SYNOPSIS</span></span>
<span data-ttu-id="8c1a6-103">Az Azure Storage Services naplózási tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="8c1a6-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="8c1a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c1a6-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c1a6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c1a6-105">DESCRIPTION</span></span>
<span data-ttu-id="8c1a6-106">A **Get-AzStorageServiceLoggingProperty** parancsmag az Azure Storage Services naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8c1a6-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="8c1a6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8c1a6-107">EXAMPLES</span></span>

### <span data-ttu-id="8c1a6-108">Példa 1: a blob-szolgáltatás naplózási tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="8c1a6-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="8c1a6-109">Ez a parancs a blob-tároló naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8c1a6-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="8c1a6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c1a6-110">PARAMETERS</span></span>

### <span data-ttu-id="8c1a6-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8c1a6-111">-Context</span></span>
<span data-ttu-id="8c1a6-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c1a6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8c1a6-113">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8c1a6-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8c1a6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c1a6-114">-DefaultProfile</span></span>
<span data-ttu-id="8c1a6-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c1a6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c1a6-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="8c1a6-116">-ServiceType</span></span>
<span data-ttu-id="8c1a6-117">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c1a6-117">Specifies the storage service type.</span></span>
<span data-ttu-id="8c1a6-118">Ez a parancsmag a paraméter által megadott szolgáltatási típus naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8c1a6-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="8c1a6-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8c1a6-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8c1a6-120">BLOB</span><span class="sxs-lookup"><span data-stu-id="8c1a6-120">Blob</span></span> 
- <span data-ttu-id="8c1a6-121">Táblázat</span><span class="sxs-lookup"><span data-stu-id="8c1a6-121">Table</span></span>
- <span data-ttu-id="8c1a6-122">Várólista</span><span class="sxs-lookup"><span data-stu-id="8c1a6-122">Queue</span></span>
- <span data-ttu-id="8c1a6-123">Fájl: a fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="8c1a6-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="8c1a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c1a6-124">CommonParameters</span></span>
<span data-ttu-id="8c1a6-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c1a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c1a6-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c1a6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c1a6-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c1a6-127">INPUTS</span></span>

### <span data-ttu-id="8c1a6-128">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8c1a6-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8c1a6-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c1a6-129">OUTPUTS</span></span>

### <span data-ttu-id="8c1a6-130">Microsoft. Azure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="8c1a6-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="8c1a6-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c1a6-131">NOTES</span></span>

## <span data-ttu-id="8c1a6-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c1a6-132">RELATED LINKS</span></span>

[<span data-ttu-id="8c1a6-133">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8c1a6-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="8c1a6-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8c1a6-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)

