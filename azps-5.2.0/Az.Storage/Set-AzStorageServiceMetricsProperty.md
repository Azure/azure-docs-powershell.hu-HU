---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: d3f32e44e5653d0d6a9c9b5a9a1eee27b66d43cf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348186"
---
# <span data-ttu-id="549c3-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="549c3-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="549c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="549c3-102">SYNOPSIS</span></span>
<span data-ttu-id="549c3-103">Módosítja az Azure Storage szolgáltatás metrikák tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="549c3-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="549c3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="549c3-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="549c3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="549c3-105">DESCRIPTION</span></span>
<span data-ttu-id="549c3-106">A **Set-AzStorageServiceMetricsProperty** parancsmag módosítja az Azure Storage szolgáltatás metrikák tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="549c3-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="549c3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="549c3-107">EXAMPLES</span></span>

### <span data-ttu-id="549c3-108">1. példa: A Blob szolgáltatás metrikák tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="549c3-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="549c3-109">Ez a parancs szolgáltatásszintre módosítja a blobtároló 1.0-s verzióját.</span><span class="sxs-lookup"><span data-stu-id="549c3-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="549c3-110">Az Azure Storage service metrikák 10 napig őrzik meg a bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="549c3-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="549c3-111">Mivel ez a parancs megadja *a PassThru* paramétert, a parancs megjeleníti a módosított metrikák tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="549c3-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="549c3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="549c3-112">PARAMETERS</span></span>

### <span data-ttu-id="549c3-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="549c3-113">-Context</span></span>
<span data-ttu-id="549c3-114">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="549c3-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="549c3-115">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="549c3-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="549c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="549c3-116">-DefaultProfile</span></span>
<span data-ttu-id="549c3-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="549c3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="549c3-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="549c3-118">-MetricsLevel</span></span>
<span data-ttu-id="549c3-119">Az Azure Storage által a szolgáltatáshoz használt metrikák szintjét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="549c3-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="549c3-120">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="549c3-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="549c3-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="549c3-121">None</span></span>
- <span data-ttu-id="549c3-122">Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="549c3-122">Service</span></span>
- <span data-ttu-id="549c3-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="549c3-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="549c3-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="549c3-124">-MetricsType</span></span>
<span data-ttu-id="549c3-125">A metrikák típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="549c3-125">Specifies a metrics type.</span></span>
<span data-ttu-id="549c3-126">Ez a parancsmag az Azure Storage szolgáltatás metrikák típusát a paraméter által megadott értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="549c3-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="549c3-127">A paraméter elfogadható értékei: Óra és perc.</span><span class="sxs-lookup"><span data-stu-id="549c3-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="549c3-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="549c3-128">-PassThru</span></span>
<span data-ttu-id="549c3-129">Azt jelzi, hogy ezek a parancsmagok a frissített metrikák tulajdonságait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="549c3-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="549c3-130">Ha nem adja meg ezt a paramétert, ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="549c3-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="549c3-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="549c3-131">-RetentionDays</span></span>
<span data-ttu-id="549c3-132">Azt adja meg, hogy az Azure Storage szolgáltatás hány napig őrizze meg a metrikákat.</span><span class="sxs-lookup"><span data-stu-id="549c3-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="549c3-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="549c3-133">-ServiceType</span></span>
<span data-ttu-id="549c3-134">A társzolgáltatás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="549c3-134">Specifies the storage service type.</span></span>
<span data-ttu-id="549c3-135">Ez a parancsmag módosítja a paraméter által megadott szolgáltatástípus metrikák tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="549c3-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="549c3-136">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="549c3-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="549c3-137">Blob</span><span class="sxs-lookup"><span data-stu-id="549c3-137">Blob</span></span> 
- <span data-ttu-id="549c3-138">Táblázat</span><span class="sxs-lookup"><span data-stu-id="549c3-138">Table</span></span>
- <span data-ttu-id="549c3-139">Várólistán</span><span class="sxs-lookup"><span data-stu-id="549c3-139">Queue</span></span>
- <span data-ttu-id="549c3-140">Fájl: A fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="549c3-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="549c3-141">-Version</span><span class="sxs-lookup"><span data-stu-id="549c3-141">-Version</span></span>
<span data-ttu-id="549c3-142">Az Azure Storage metrikák verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="549c3-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="549c3-143">Az alapértelmezett érték 1,0.</span><span class="sxs-lookup"><span data-stu-id="549c3-143">The default value is 1.0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="549c3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="549c3-144">CommonParameters</span></span>
<span data-ttu-id="549c3-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="549c3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="549c3-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="549c3-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="549c3-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="549c3-147">INPUTS</span></span>

### <span data-ttu-id="549c3-148">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="549c3-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="549c3-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="549c3-149">OUTPUTS</span></span>

### <span data-ttu-id="549c3-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="549c3-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="549c3-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="549c3-151">NOTES</span></span>

## <span data-ttu-id="549c3-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="549c3-152">RELATED LINKS</span></span>

[<span data-ttu-id="549c3-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="549c3-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="549c3-154">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="549c3-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


