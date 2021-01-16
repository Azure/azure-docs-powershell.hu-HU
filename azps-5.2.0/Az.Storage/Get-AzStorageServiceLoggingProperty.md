---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 6e4eced11a9de228f836e80e9f25350e3f09a8c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324949"
---
# <span data-ttu-id="ae11f-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ae11f-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="ae11f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae11f-102">SYNOPSIS</span></span>
<span data-ttu-id="ae11f-103">Naplózási tulajdonságokat kap az Azure Storage-szolgáltatásokhoz.</span><span class="sxs-lookup"><span data-stu-id="ae11f-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="ae11f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ae11f-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae11f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ae11f-105">DESCRIPTION</span></span>
<span data-ttu-id="ae11f-106">A **Get-AzStorageServiceLoggingProperty parancsmag** az Azure Storage-szolgáltatások naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ae11f-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="ae11f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ae11f-107">EXAMPLES</span></span>

### <span data-ttu-id="ae11f-108">1. példa: A Blob szolgáltatás naplózási tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="ae11f-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="ae11f-109">Ez a parancs a blobtároló naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ae11f-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="ae11f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae11f-110">PARAMETERS</span></span>

### <span data-ttu-id="ae11f-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ae11f-111">-Context</span></span>
<span data-ttu-id="ae11f-112">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae11f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ae11f-113">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ae11f-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ae11f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae11f-114">-DefaultProfile</span></span>
<span data-ttu-id="ae11f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae11f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae11f-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ae11f-116">-ServiceType</span></span>
<span data-ttu-id="ae11f-117">A társzolgáltatás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ae11f-117">Specifies the storage service type.</span></span>
<span data-ttu-id="ae11f-118">Ez a parancsmag a paraméter által megadott szolgáltatástípus naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ae11f-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="ae11f-119">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="ae11f-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ae11f-120">Blob</span><span class="sxs-lookup"><span data-stu-id="ae11f-120">Blob</span></span> 
- <span data-ttu-id="ae11f-121">Táblázat</span><span class="sxs-lookup"><span data-stu-id="ae11f-121">Table</span></span>
- <span data-ttu-id="ae11f-122">Várólistán</span><span class="sxs-lookup"><span data-stu-id="ae11f-122">Queue</span></span>
- <span data-ttu-id="ae11f-123">Fájl: A fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="ae11f-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="ae11f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae11f-124">CommonParameters</span></span>
<span data-ttu-id="ae11f-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae11f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae11f-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae11f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae11f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae11f-127">INPUTS</span></span>

### <span data-ttu-id="ae11f-128">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ae11f-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ae11f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae11f-129">OUTPUTS</span></span>

### <span data-ttu-id="ae11f-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="ae11f-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="ae11f-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ae11f-131">NOTES</span></span>

## <span data-ttu-id="ae11f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae11f-132">RELATED LINKS</span></span>

[<span data-ttu-id="ae11f-133">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="ae11f-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="ae11f-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ae11f-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


