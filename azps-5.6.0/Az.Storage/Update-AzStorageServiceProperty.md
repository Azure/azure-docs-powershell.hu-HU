---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: 952f66bfffef4d8f7636098a8280cd26b6fc7f5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929218"
---
# <span data-ttu-id="fd05f-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="fd05f-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="fd05f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd05f-102">SYNOPSIS</span></span>
<span data-ttu-id="fd05f-103">Módosítja az Azure Storage szolgáltatás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="fd05f-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="fd05f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd05f-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd05f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd05f-105">DESCRIPTION</span></span>
<span data-ttu-id="fd05f-106">Az **Update-AzStorageServiceProperty** parancsmag módosítja az Azure Storage szolgáltatás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="fd05f-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="fd05f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd05f-107">EXAMPLES</span></span>

### <span data-ttu-id="fd05f-108">1. példa: Blob-szolgáltatás DefaultServiceVersion beállítása 2017-04-17-re</span><span class="sxs-lookup"><span data-stu-id="fd05f-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="fd05f-109">Ez a parancs a Blobszolgáltatás DefaultServiceVersion-ének beállítása 2017-04-17-re</span><span class="sxs-lookup"><span data-stu-id="fd05f-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="fd05f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd05f-110">PARAMETERS</span></span>

### <span data-ttu-id="fd05f-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fd05f-111">-Context</span></span>
<span data-ttu-id="fd05f-112">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd05f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fd05f-113">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fd05f-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fd05f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd05f-114">-DefaultProfile</span></span>
<span data-ttu-id="fd05f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd05f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd05f-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="fd05f-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="fd05f-117">A DefaultServiceVersion azt az alapértelmezett verziót jelzi, amely a Blob szolgáltatáshoz érkező kérelmekhez használható, ha nincs megadva egy bejövő kérés verziója.</span><span class="sxs-lookup"><span data-stu-id="fd05f-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="fd05f-118">A lehetséges értékek közé tartozik a 2008-10-27-es verzió és az összes újabb verzió.</span><span class="sxs-lookup"><span data-stu-id="fd05f-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="fd05f-119">További részleteket itt talál: https://docs.microsoft.com/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="fd05f-119">See more details in https://docs.microsoft.com/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

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

### <span data-ttu-id="fd05f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd05f-120">-PassThru</span></span>
<span data-ttu-id="fd05f-121">Display ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="fd05f-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="fd05f-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="fd05f-122">-ServiceType</span></span>
<span data-ttu-id="fd05f-123">A társzolgáltatás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fd05f-123">Specifies the storage service type.</span></span>
<span data-ttu-id="fd05f-124">Ez a parancsmag a paraméter által megadott szolgáltatástípus naplózási tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fd05f-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="fd05f-125">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="fd05f-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fd05f-126">Blob</span><span class="sxs-lookup"><span data-stu-id="fd05f-126">Blob</span></span> 
- <span data-ttu-id="fd05f-127">Táblázat</span><span class="sxs-lookup"><span data-stu-id="fd05f-127">Table</span></span>
- <span data-ttu-id="fd05f-128">Várólistán</span><span class="sxs-lookup"><span data-stu-id="fd05f-128">Queue</span></span>
- <span data-ttu-id="fd05f-129">Fájl</span><span class="sxs-lookup"><span data-stu-id="fd05f-129">File</span></span>

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

### <span data-ttu-id="fd05f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd05f-130">-Confirm</span></span>
<span data-ttu-id="fd05f-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fd05f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd05f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd05f-132">-WhatIf</span></span>
<span data-ttu-id="fd05f-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fd05f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd05f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd05f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd05f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd05f-135">CommonParameters</span></span>
<span data-ttu-id="fd05f-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd05f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd05f-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd05f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd05f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd05f-138">INPUTS</span></span>

### <span data-ttu-id="fd05f-139">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fd05f-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fd05f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd05f-140">OUTPUTS</span></span>

### <span data-ttu-id="fd05f-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="fd05f-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="fd05f-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd05f-142">NOTES</span></span>

## <span data-ttu-id="fd05f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd05f-143">RELATED LINKS</span></span>
