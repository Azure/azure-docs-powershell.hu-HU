---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: e94bb90ffeda257dd024c1cf9b834764455cd6aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180758"
---
# <span data-ttu-id="d1f6f-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d1f6f-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="d1f6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f6f-103">Módosítja az Azure Storage szolgáltatás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d1f6f-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="d1f6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1f6f-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1f6f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1f6f-105">DESCRIPTION</span></span>
<span data-ttu-id="d1f6f-106">Az **Update-AzStorageServiceProperty** parancsmag módosította az Azure Storage szolgáltatás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d1f6f-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="d1f6f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d1f6f-107">EXAMPLES</span></span>

### <span data-ttu-id="d1f6f-108">1. példa: a blob-szolgáltatás DefaultServiceVersion beállítása az 2017-04-17-be</span><span class="sxs-lookup"><span data-stu-id="d1f6f-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="d1f6f-109">Ez a parancs a blob-szolgáltatás DefaultServiceVersion a 2017-04-17-ra állítja be.</span><span class="sxs-lookup"><span data-stu-id="d1f6f-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="d1f6f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1f6f-110">PARAMETERS</span></span>

### <span data-ttu-id="d1f6f-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d1f6f-111">-Context</span></span>
<span data-ttu-id="d1f6f-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1f6f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d1f6f-113">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d1f6f-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d1f6f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1f6f-114">-DefaultProfile</span></span>
<span data-ttu-id="d1f6f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1f6f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1f6f-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="d1f6f-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="d1f6f-117">A DefaultServiceVersion jelzi a blob-szolgáltatás kéréséhez használni kívánt alapértelmezett verziót, ha a beérkező kérések verziószáma nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="d1f6f-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="d1f6f-118">A lehetséges értékek közé tartozik a 2008-10-27-es verzió és az összes újabb verzió.</span><span class="sxs-lookup"><span data-stu-id="d1f6f-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="d1f6f-119">További információ https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="d1f6f-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f6f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1f6f-120">-PassThru</span></span>
<span data-ttu-id="d1f6f-121">ServiceProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="d1f6f-121">Display ServiceProperties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f6f-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="d1f6f-122">-ServiceType</span></span>
<span data-ttu-id="d1f6f-123">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1f6f-123">Specifies the storage service type.</span></span>
<span data-ttu-id="d1f6f-124">Ez a parancsmag a paraméter által megadott szolgáltatási típus naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d1f6f-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="d1f6f-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d1f6f-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d1f6f-126">BLOB</span><span class="sxs-lookup"><span data-stu-id="d1f6f-126">Blob</span></span> 
- <span data-ttu-id="d1f6f-127">Táblázat</span><span class="sxs-lookup"><span data-stu-id="d1f6f-127">Table</span></span>
- <span data-ttu-id="d1f6f-128">Várólista</span><span class="sxs-lookup"><span data-stu-id="d1f6f-128">Queue</span></span>
- <span data-ttu-id="d1f6f-129">Fájl</span><span class="sxs-lookup"><span data-stu-id="d1f6f-129">File</span></span>

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

### <span data-ttu-id="d1f6f-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d1f6f-130">-Confirm</span></span>
<span data-ttu-id="d1f6f-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d1f6f-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f6f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1f6f-132">-WhatIf</span></span>
<span data-ttu-id="d1f6f-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d1f6f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1f6f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1f6f-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f6f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f6f-135">CommonParameters</span></span>
<span data-ttu-id="d1f6f-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1f6f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f6f-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1f6f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f6f-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1f6f-138">INPUTS</span></span>

### <span data-ttu-id="d1f6f-139">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d1f6f-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d1f6f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1f6f-140">OUTPUTS</span></span>

### <span data-ttu-id="d1f6f-141">Microsoft. WindowsAzure. Command. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="d1f6f-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="d1f6f-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1f6f-142">NOTES</span></span>

## <span data-ttu-id="d1f6f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1f6f-143">RELATED LINKS</span></span>
