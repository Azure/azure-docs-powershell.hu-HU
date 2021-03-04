---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 4d956dfd49e541751003d28c31285722616ab640
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942049"
---
# <span data-ttu-id="5e42a-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="5e42a-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="5e42a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e42a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e42a-103">Naplózási tulajdonságokat kap az Azure Storage-szolgáltatásokhoz.</span><span class="sxs-lookup"><span data-stu-id="5e42a-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="5e42a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5e42a-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e42a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5e42a-105">DESCRIPTION</span></span>
<span data-ttu-id="5e42a-106">A **Get-AzStorageServiceLoggingProperty parancsmag** az Azure Storage-szolgáltatások naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5e42a-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="5e42a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5e42a-107">EXAMPLES</span></span>

### <span data-ttu-id="5e42a-108">1. példa: A Blob szolgáltatás naplózási tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="5e42a-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="5e42a-109">Ez a parancs naplózási tulajdonságokat ad a blobtárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="5e42a-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="5e42a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e42a-110">PARAMETERS</span></span>

### <span data-ttu-id="5e42a-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5e42a-111">-Context</span></span>
<span data-ttu-id="5e42a-112">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e42a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5e42a-113">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5e42a-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5e42a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e42a-114">-DefaultProfile</span></span>
<span data-ttu-id="5e42a-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e42a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e42a-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="5e42a-116">-ServiceType</span></span>
<span data-ttu-id="5e42a-117">A társzolgáltatás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5e42a-117">Specifies the storage service type.</span></span>
<span data-ttu-id="5e42a-118">Ez a parancsmag a paraméter által megadott szolgáltatástípus naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5e42a-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="5e42a-119">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="5e42a-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5e42a-120">Blob</span><span class="sxs-lookup"><span data-stu-id="5e42a-120">Blob</span></span> 
- <span data-ttu-id="5e42a-121">Táblázat</span><span class="sxs-lookup"><span data-stu-id="5e42a-121">Table</span></span>
- <span data-ttu-id="5e42a-122">Várólistán</span><span class="sxs-lookup"><span data-stu-id="5e42a-122">Queue</span></span>
- <span data-ttu-id="5e42a-123">Fájl: A fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="5e42a-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="5e42a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e42a-124">CommonParameters</span></span>
<span data-ttu-id="5e42a-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e42a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e42a-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e42a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e42a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e42a-127">INPUTS</span></span>

### <span data-ttu-id="5e42a-128">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5e42a-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5e42a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e42a-129">OUTPUTS</span></span>

### <span data-ttu-id="5e42a-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="5e42a-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="5e42a-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5e42a-131">NOTES</span></span>

## <span data-ttu-id="5e42a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e42a-132">RELATED LINKS</span></span>

[<span data-ttu-id="5e42a-133">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="5e42a-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="5e42a-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="5e42a-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


