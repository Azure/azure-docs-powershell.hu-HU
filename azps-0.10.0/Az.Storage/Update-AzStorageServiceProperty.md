---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: f07ef4aaf3837cbb432e1be546ab184a4b410e81
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842829"
---
# <span data-ttu-id="90e74-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="90e74-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="90e74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="90e74-102">SYNOPSIS</span></span>
<span data-ttu-id="90e74-103">Módosítja az Azure Storage szolgáltatás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="90e74-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="90e74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="90e74-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90e74-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="90e74-105">DESCRIPTION</span></span>
<span data-ttu-id="90e74-106">Az **Update-AzStorageServiceProperty** parancsmag módosította az Azure Storage szolgáltatás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="90e74-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="90e74-107">Példák</span><span class="sxs-lookup"><span data-stu-id="90e74-107">EXAMPLES</span></span>

### <span data-ttu-id="90e74-108">1. példa: a blob-szolgáltatás DefaultServiceVersion beállítása az 2017-04-17-be</span><span class="sxs-lookup"><span data-stu-id="90e74-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="90e74-109">Ez a parancs a blob-szolgáltatás DefaultServiceVersion a 2017-04-17-ra állítja be.</span><span class="sxs-lookup"><span data-stu-id="90e74-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="90e74-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="90e74-110">PARAMETERS</span></span>

### <span data-ttu-id="90e74-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="90e74-111">-Context</span></span>
<span data-ttu-id="90e74-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90e74-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="90e74-113">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="90e74-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="90e74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e74-114">-DefaultProfile</span></span>
<span data-ttu-id="90e74-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90e74-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90e74-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="90e74-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="90e74-117">A DefaultServiceVersion jelzi a blob-szolgáltatás kéréséhez használni kívánt alapértelmezett verziót, ha a beérkező kérések verziószáma nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="90e74-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="90e74-118">A lehetséges értékek közé tartozik a 2008-10-27-es verzió és az összes újabb verzió.</span><span class="sxs-lookup"><span data-stu-id="90e74-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="90e74-119">További információ https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span><span class="sxs-lookup"><span data-stu-id="90e74-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span></span>

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

### <span data-ttu-id="90e74-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90e74-120">-PassThru</span></span>
<span data-ttu-id="90e74-121">ServiceProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="90e74-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="90e74-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="90e74-122">-ServiceType</span></span>
<span data-ttu-id="90e74-123">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="90e74-123">Specifies the storage service type.</span></span>
<span data-ttu-id="90e74-124">Ez a parancsmag a paraméter által megadott szolgáltatási típus naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="90e74-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="90e74-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="90e74-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="90e74-126">BLOB</span><span class="sxs-lookup"><span data-stu-id="90e74-126">Blob</span></span> 
- <span data-ttu-id="90e74-127">Táblázat</span><span class="sxs-lookup"><span data-stu-id="90e74-127">Table</span></span>
- <span data-ttu-id="90e74-128">Várólista</span><span class="sxs-lookup"><span data-stu-id="90e74-128">Queue</span></span>
- <span data-ttu-id="90e74-129">Fájl</span><span class="sxs-lookup"><span data-stu-id="90e74-129">File</span></span>

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

### <span data-ttu-id="90e74-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="90e74-130">-Confirm</span></span>
<span data-ttu-id="90e74-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="90e74-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e74-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e74-132">-WhatIf</span></span>
<span data-ttu-id="90e74-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="90e74-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90e74-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="90e74-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e74-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e74-135">CommonParameters</span></span>
<span data-ttu-id="90e74-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="90e74-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e74-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90e74-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e74-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="90e74-138">INPUTS</span></span>

### <span data-ttu-id="90e74-139">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="90e74-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="90e74-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90e74-140">OUTPUTS</span></span>

### <span data-ttu-id="90e74-141">Microsoft. WindowsAzure. Command. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="90e74-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="90e74-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="90e74-142">NOTES</span></span>

## <span data-ttu-id="90e74-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90e74-143">RELATED LINKS</span></span>
