---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/update-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
ms.openlocfilehash: 7036f12b4ab47043b69fe4164ac567f4355a51ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501579"
---
# <span data-ttu-id="d96f9-101">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d96f9-101">Update-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="d96f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d96f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d96f9-103">Módosítja az Azure Storage szolgáltatás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d96f9-103">Modifies the properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d96f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d96f9-104">SYNTAX</span></span>

```
Update-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d96f9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d96f9-105">DESCRIPTION</span></span>
<span data-ttu-id="d96f9-106">Az **Update-AzureStorageServiceProperty** parancsmag módosította az Azure Storage szolgáltatás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d96f9-106">The **Update-AzureStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="d96f9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d96f9-107">EXAMPLES</span></span>

### <span data-ttu-id="d96f9-108">1. példa: a blob-szolgáltatás DefaultServiceVersion beállítása az 2017-04-17-be</span><span class="sxs-lookup"><span data-stu-id="d96f9-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzureStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="d96f9-109">Ez a parancs a blob-szolgáltatás DefaultServiceVersion a 2017-04-17-ra állítja be.</span><span class="sxs-lookup"><span data-stu-id="d96f9-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="d96f9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d96f9-110">PARAMETERS</span></span>

### <span data-ttu-id="d96f9-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d96f9-111">-Context</span></span>
<span data-ttu-id="d96f9-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d96f9-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d96f9-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d96f9-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d96f9-114">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="d96f9-114">-DefaultServiceVersion</span></span>
<span data-ttu-id="d96f9-115">A DefaultServiceVersion jelzi a blob-szolgáltatás kéréséhez használni kívánt alapértelmezett verziót, ha a beérkező kérések verziószáma nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="d96f9-115">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="d96f9-116">A lehetséges értékek közé tartozik a 2008-10-27-es verzió és az összes újabb verzió.</span><span class="sxs-lookup"><span data-stu-id="d96f9-116">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="d96f9-117">További információ https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span><span class="sxs-lookup"><span data-stu-id="d96f9-117">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d96f9-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d96f9-118">-PassThru</span></span>
<span data-ttu-id="d96f9-119">ServiceProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="d96f9-119">Display ServiceProperties</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d96f9-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="d96f9-120">-ServiceType</span></span>
<span data-ttu-id="d96f9-121">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d96f9-121">Specifies the storage service type.</span></span>
<span data-ttu-id="d96f9-122">Ez a parancsmag a paraméter által megadott szolgáltatási típus naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d96f9-122">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="d96f9-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d96f9-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d96f9-124">BLOB</span><span class="sxs-lookup"><span data-stu-id="d96f9-124">Blob</span></span> 
- <span data-ttu-id="d96f9-125">Táblázat</span><span class="sxs-lookup"><span data-stu-id="d96f9-125">Table</span></span>
- <span data-ttu-id="d96f9-126">Várólista</span><span class="sxs-lookup"><span data-stu-id="d96f9-126">Queue</span></span>
- <span data-ttu-id="d96f9-127">Fájl</span><span class="sxs-lookup"><span data-stu-id="d96f9-127">File</span></span>

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

### <span data-ttu-id="d96f9-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d96f9-128">-Confirm</span></span>
<span data-ttu-id="d96f9-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d96f9-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d96f9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d96f9-130">-WhatIf</span></span>
<span data-ttu-id="d96f9-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d96f9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d96f9-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d96f9-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d96f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d96f9-133">CommonParameters</span></span>
<span data-ttu-id="d96f9-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d96f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d96f9-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d96f9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d96f9-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d96f9-136">INPUTS</span></span>

### <span data-ttu-id="d96f9-137">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d96f9-137">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d96f9-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d96f9-138">OUTPUTS</span></span>

### <span data-ttu-id="d96f9-139">Microsoft. WindowsAzure. Command. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="d96f9-139">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="d96f9-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d96f9-140">NOTES</span></span>

## <span data-ttu-id="d96f9-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d96f9-141">RELATED LINKS</span></span>

