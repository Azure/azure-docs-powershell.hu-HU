---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51921a7d67cd8a297f5cd61716362f13cef6cdc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491780"
---
# <span data-ttu-id="f454b-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f454b-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="f454b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f454b-102">SYNOPSIS</span></span>
<span data-ttu-id="f454b-103">Módosítja az Azure Storage szolgáltatás metrikák tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="f454b-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="f454b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f454b-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="f454b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f454b-105">DESCRIPTION</span></span>
<span data-ttu-id="f454b-106">A **set-AzureStorageServiceMetricsProperty** parancsmag módosítja az Azure Storage szolgáltatás metrikák tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="f454b-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="f454b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f454b-107">EXAMPLES</span></span>

### <span data-ttu-id="f454b-108">1. példa: a blob-szolgáltatás metrikák tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="f454b-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="f454b-109">Ez a parancs a 1,0-os metrikákat a blob-tárolók számára a szolgáltatás szintjére módosítja.</span><span class="sxs-lookup"><span data-stu-id="f454b-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="f454b-110">Az Azure Storage Service metrikája 10 napra megőrzi a bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="f454b-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="f454b-111">Mivel a parancs a *PassThru* paramétert adja meg, a parancs a módosított metrikák tulajdonságot jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="f454b-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="f454b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f454b-112">PARAMETERS</span></span>

### <span data-ttu-id="f454b-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f454b-113">-Context</span></span>
<span data-ttu-id="f454b-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f454b-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f454b-115">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f454b-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f454b-116">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="f454b-116">-MetricsLevel</span></span>
<span data-ttu-id="f454b-117">Az Azure-tárterület által a szolgáltatáshoz használt metrikák szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f454b-117">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="f454b-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f454b-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f454b-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="f454b-119">None</span></span>
- <span data-ttu-id="f454b-120">Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="f454b-120">Service</span></span>
- <span data-ttu-id="f454b-121">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="f454b-121">ServiceAndApi</span></span>

```yaml
Type: MetricsLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f454b-122">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="f454b-122">-MetricsType</span></span>
<span data-ttu-id="f454b-123">A mérőszám típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f454b-123">Specifies a metrics type.</span></span>
<span data-ttu-id="f454b-124">Ez a cmldet az Azure Storage Service metrikák típusát a paraméter által megadott értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="f454b-124">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="f454b-125">A paraméter elfogadható értékei a következők: óra és perc.</span><span class="sxs-lookup"><span data-stu-id="f454b-125">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f454b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f454b-126">-PassThru</span></span>
<span data-ttu-id="f454b-127">Azt jelzi, hogy ez a parancsmag a frissített metrikák tulajdonságot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f454b-127">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="f454b-128">Ha nem adja meg ezt a paramétert, ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="f454b-128">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f454b-129">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="f454b-129">-RetentionDays</span></span>
<span data-ttu-id="f454b-130">Annak a napoknak a száma, ameddig az Azure Storage Service megőrzi a metrikák adatait.</span><span class="sxs-lookup"><span data-stu-id="f454b-130">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f454b-131">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="f454b-131">-ServiceType</span></span>
<span data-ttu-id="f454b-132">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f454b-132">Specifies the storage service type.</span></span>
<span data-ttu-id="f454b-133">Ez a parancsmag módosítja a paraméter által megadott szolgáltatási típus metrikájának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="f454b-133">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="f454b-134">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f454b-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f454b-135">BLOB</span><span class="sxs-lookup"><span data-stu-id="f454b-135">Blob</span></span> 
- <span data-ttu-id="f454b-136">Táblázat</span><span class="sxs-lookup"><span data-stu-id="f454b-136">Table</span></span>
- <span data-ttu-id="f454b-137">Várólista</span><span class="sxs-lookup"><span data-stu-id="f454b-137">Queue</span></span>
- <span data-ttu-id="f454b-138">Fájl</span><span class="sxs-lookup"><span data-stu-id="f454b-138">File</span></span>

<span data-ttu-id="f454b-139">A fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="f454b-139">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="f454b-140">-Verzió</span><span class="sxs-lookup"><span data-stu-id="f454b-140">-Version</span></span>
<span data-ttu-id="f454b-141">Az Azure-tárterület metrikájának verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f454b-141">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="f454b-142">Az alapértelmezett érték a 1,0.</span><span class="sxs-lookup"><span data-stu-id="f454b-142">The default value is 1.0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f454b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f454b-143">CommonParameters</span></span>
<span data-ttu-id="f454b-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f454b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f454b-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f454b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f454b-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f454b-146">INPUTS</span></span>

## <span data-ttu-id="f454b-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f454b-147">OUTPUTS</span></span>

## <span data-ttu-id="f454b-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f454b-148">NOTES</span></span>

## <span data-ttu-id="f454b-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f454b-149">RELATED LINKS</span></span>

[<span data-ttu-id="f454b-150">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f454b-150">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="f454b-151">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f454b-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


