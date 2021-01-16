---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 4d58b8e323476adda73f4a4827dc263c20bd4cc4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479449"
---
# <span data-ttu-id="fd9dc-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="fd9dc-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="fd9dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="fd9dc-103">Az Azure Storage szolgáltatás metrikatulajdonságokat kap.</span><span class="sxs-lookup"><span data-stu-id="fd9dc-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="fd9dc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd9dc-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd9dc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd9dc-105">DESCRIPTION</span></span>
<span data-ttu-id="fd9dc-106">A **Get-AzStorageServiceMetricsProperty** parancsmag metrikák tulajdonságait kapja meg az Azure Storage szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="fd9dc-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="fd9dc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd9dc-107">EXAMPLES</span></span>

### <span data-ttu-id="fd9dc-108">1. példa: A Blob szolgáltatás metrikák tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="fd9dc-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="fd9dc-109">Ez a parancs az Óra típusú metrikák blobtárára vonatkozó metrikák tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="fd9dc-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="fd9dc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd9dc-110">PARAMETERS</span></span>

### <span data-ttu-id="fd9dc-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fd9dc-111">-Context</span></span>
<span data-ttu-id="fd9dc-112">Egy Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fd9dc-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fd9dc-113">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fd9dc-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fd9dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd9dc-114">-DefaultProfile</span></span>
<span data-ttu-id="fd9dc-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd9dc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd9dc-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="fd9dc-116">-MetricsType</span></span>
<span data-ttu-id="fd9dc-117">A metrikák típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd9dc-117">Specifies a metrics type.</span></span>
<span data-ttu-id="fd9dc-118">Ez a parancsmag lekérte az Azure Storage szolgáltatás metrikák tulajdonságait a paraméter által megadott metrikák típusára.</span><span class="sxs-lookup"><span data-stu-id="fd9dc-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="fd9dc-119">A paraméter elfogadható értékei: Óra és perc.</span><span class="sxs-lookup"><span data-stu-id="fd9dc-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9dc-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="fd9dc-120">-ServiceType</span></span>
<span data-ttu-id="fd9dc-121">A társzolgáltatás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fd9dc-121">Specifies the storage service type.</span></span>
<span data-ttu-id="fd9dc-122">Ez a parancsmag a paraméter által megadott típus metrikák tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fd9dc-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="fd9dc-123">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="fd9dc-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fd9dc-124">Blob</span><span class="sxs-lookup"><span data-stu-id="fd9dc-124">Blob</span></span> 
- <span data-ttu-id="fd9dc-125">Táblázat</span><span class="sxs-lookup"><span data-stu-id="fd9dc-125">Table</span></span>
- <span data-ttu-id="fd9dc-126">Várólistán</span><span class="sxs-lookup"><span data-stu-id="fd9dc-126">Queue</span></span>
- <span data-ttu-id="fd9dc-127">Fájl: A fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="fd9dc-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="fd9dc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd9dc-128">CommonParameters</span></span>
<span data-ttu-id="fd9dc-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd9dc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd9dc-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd9dc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd9dc-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd9dc-131">INPUTS</span></span>

### <span data-ttu-id="fd9dc-132">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fd9dc-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fd9dc-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd9dc-133">OUTPUTS</span></span>

### <span data-ttu-id="fd9dc-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="fd9dc-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="fd9dc-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd9dc-135">NOTES</span></span>

## <span data-ttu-id="fd9dc-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd9dc-136">RELATED LINKS</span></span>

[<span data-ttu-id="fd9dc-137">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="fd9dc-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="fd9dc-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="fd9dc-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


