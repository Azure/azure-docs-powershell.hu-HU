---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageservicemetricsproperty
schema: 2.0.0
ms.openlocfilehash: 45192b6b24719bb793e3f443cf2a8cb42abd78ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850973"
---
# <span data-ttu-id="af1f5-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="af1f5-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="af1f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af1f5-102">SYNOPSIS</span></span>
<span data-ttu-id="af1f5-103">Módosítja az Azure Storage szolgáltatás metrikák tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="af1f5-103">Modifies metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af1f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af1f5-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af1f5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="af1f5-105">DESCRIPTION</span></span>
<span data-ttu-id="af1f5-106">A **set-AzureStorageServiceMetricsProperty** parancsmag módosítja az Azure Storage szolgáltatás metrikák tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="af1f5-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="af1f5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="af1f5-107">EXAMPLES</span></span>

### <span data-ttu-id="af1f5-108">1. példa: a blob-szolgáltatás metrikák tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="af1f5-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="af1f5-109">Ez a parancs a 1,0-os metrikákat a blob-tárolók számára a szolgáltatás szintjére módosítja.</span><span class="sxs-lookup"><span data-stu-id="af1f5-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="af1f5-110">Az Azure Storage Service metrikája 10 napra megőrzi a bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="af1f5-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="af1f5-111">Mivel a parancs a *PassThru* paramétert adja meg, a parancs a módosított metrikák tulajdonságot jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="af1f5-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="af1f5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af1f5-112">PARAMETERS</span></span>

### <span data-ttu-id="af1f5-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="af1f5-113">-Context</span></span>
<span data-ttu-id="af1f5-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af1f5-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="af1f5-115">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="af1f5-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="af1f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af1f5-116">-DefaultProfile</span></span>
<span data-ttu-id="af1f5-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af1f5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af1f5-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="af1f5-118">-MetricsLevel</span></span>
<span data-ttu-id="af1f5-119">Az Azure-tárterület által a szolgáltatáshoz használt metrikák szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af1f5-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="af1f5-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="af1f5-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="af1f5-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="af1f5-121">None</span></span>
- <span data-ttu-id="af1f5-122">Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="af1f5-122">Service</span></span>
- <span data-ttu-id="af1f5-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="af1f5-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af1f5-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="af1f5-124">-MetricsType</span></span>
<span data-ttu-id="af1f5-125">A mérőszám típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="af1f5-125">Specifies a metrics type.</span></span>
<span data-ttu-id="af1f5-126">Ez a cmldet az Azure Storage Service metrikák típusát a paraméter által megadott értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="af1f5-126">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="af1f5-127">A paraméter elfogadható értékei a következők: óra és perc.</span><span class="sxs-lookup"><span data-stu-id="af1f5-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="af1f5-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af1f5-128">-PassThru</span></span>
<span data-ttu-id="af1f5-129">Azt jelzi, hogy ez a parancsmag a frissített metrikák tulajdonságot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="af1f5-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="af1f5-130">Ha nem adja meg ezt a paramétert, ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="af1f5-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="af1f5-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="af1f5-131">-RetentionDays</span></span>
<span data-ttu-id="af1f5-132">Annak a napoknak a száma, ameddig az Azure Storage Service megőrzi a metrikák adatait.</span><span class="sxs-lookup"><span data-stu-id="af1f5-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="af1f5-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="af1f5-133">-ServiceType</span></span>
<span data-ttu-id="af1f5-134">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="af1f5-134">Specifies the storage service type.</span></span>
<span data-ttu-id="af1f5-135">Ez a parancsmag módosítja a paraméter által megadott szolgáltatási típus metrikájának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="af1f5-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="af1f5-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="af1f5-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="af1f5-137">BLOB</span><span class="sxs-lookup"><span data-stu-id="af1f5-137">Blob</span></span> 
- <span data-ttu-id="af1f5-138">Táblázat</span><span class="sxs-lookup"><span data-stu-id="af1f5-138">Table</span></span>
- <span data-ttu-id="af1f5-139">Várólista</span><span class="sxs-lookup"><span data-stu-id="af1f5-139">Queue</span></span>
- <span data-ttu-id="af1f5-140">Fájl: a fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="af1f5-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="af1f5-141">-Verzió</span><span class="sxs-lookup"><span data-stu-id="af1f5-141">-Version</span></span>
<span data-ttu-id="af1f5-142">Az Azure-tárterület metrikájának verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="af1f5-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="af1f5-143">Az alapértelmezett érték a 1,0.</span><span class="sxs-lookup"><span data-stu-id="af1f5-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="af1f5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af1f5-144">CommonParameters</span></span>
<span data-ttu-id="af1f5-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af1f5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af1f5-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af1f5-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af1f5-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af1f5-147">INPUTS</span></span>

### <span data-ttu-id="af1f5-148">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="af1f5-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="af1f5-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af1f5-149">OUTPUTS</span></span>

### <span data-ttu-id="af1f5-150">Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="af1f5-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="af1f5-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af1f5-151">NOTES</span></span>

## <span data-ttu-id="af1f5-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af1f5-152">RELATED LINKS</span></span>

[<span data-ttu-id="af1f5-153">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="af1f5-153">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="af1f5-154">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="af1f5-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


