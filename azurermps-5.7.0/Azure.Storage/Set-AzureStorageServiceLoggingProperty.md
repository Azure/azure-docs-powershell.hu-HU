---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
ms.openlocfilehash: fbd7c691e2cfbef58bc59429f68740af00288906
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680452"
---
# <span data-ttu-id="384e0-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="384e0-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="384e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="384e0-102">SYNOPSIS</span></span>
<span data-ttu-id="384e0-103">Az Azure Storage Services naplózásának módosítása.</span><span class="sxs-lookup"><span data-stu-id="384e0-103">Modifies logging for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="384e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="384e0-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="384e0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="384e0-105">DESCRIPTION</span></span>
<span data-ttu-id="384e0-106">A **set-AzureStorageServiceLoggingProperty** parancsmag az Azure Storage Services naplózását módosítja.</span><span class="sxs-lookup"><span data-stu-id="384e0-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="384e0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="384e0-107">EXAMPLES</span></span>

### <span data-ttu-id="384e0-108">1. példa: a blob-szolgáltatás naplózási tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="384e0-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="384e0-109">Ez a parancs módosítja a 1,0-ös verzió naplózását a blob-tárolóhoz az olvasási és írási műveletek elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="384e0-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="384e0-110">Az Azure Storage Service naplózása 10 napra megőrzi a bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="384e0-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="384e0-111">Mivel a parancs a *PassThru* paramétert adja meg, a parancs a módosított naplózási tulajdonságokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="384e0-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="384e0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="384e0-112">PARAMETERS</span></span>

### <span data-ttu-id="384e0-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="384e0-113">-Context</span></span>
<span data-ttu-id="384e0-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="384e0-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="384e0-115">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="384e0-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="384e0-116">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="384e0-116">-LoggingOperations</span></span>
<span data-ttu-id="384e0-117">Az Azure Storage Service-műveletek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="384e0-117">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="384e0-118">Az Azure Storage Services naplózza azokat a műveleteket, amelyeket a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="384e0-118">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="384e0-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="384e0-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="384e0-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="384e0-120">None</span></span>
- <span data-ttu-id="384e0-121">Olvasása</span><span class="sxs-lookup"><span data-stu-id="384e0-121">Read</span></span>
- <span data-ttu-id="384e0-122">Írni</span><span class="sxs-lookup"><span data-stu-id="384e0-122">Write</span></span>
- <span data-ttu-id="384e0-123">Törlése</span><span class="sxs-lookup"><span data-stu-id="384e0-123">Delete</span></span>
- <span data-ttu-id="384e0-124">Minden</span><span class="sxs-lookup"><span data-stu-id="384e0-124">All</span></span>

```yaml
Type: LoggingOperations[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="384e0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="384e0-125">-PassThru</span></span>
<span data-ttu-id="384e0-126">Azt jelzi, hogy ez a parancsmag a frissített naplózási tulajdonságokat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="384e0-126">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="384e0-127">Ha nem adja meg ezt a paramétert, ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="384e0-127">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="384e0-128">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="384e0-128">-RetentionDays</span></span>
<span data-ttu-id="384e0-129">Annak a napoknak a száma, ameddig az Azure Storage szolgáltatás megőrzi a naplózási információkat.</span><span class="sxs-lookup"><span data-stu-id="384e0-129">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="384e0-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="384e0-130">-ServiceType</span></span>
<span data-ttu-id="384e0-131">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="384e0-131">Specifies the storage service type.</span></span>
<span data-ttu-id="384e0-132">Ez a parancsmag módosítja a szolgáltatás típusának naplózási tulajdonságait, amelyeket a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="384e0-132">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="384e0-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="384e0-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="384e0-134">BLOB</span><span class="sxs-lookup"><span data-stu-id="384e0-134">Blob</span></span> 
- <span data-ttu-id="384e0-135">Táblázat</span><span class="sxs-lookup"><span data-stu-id="384e0-135">Table</span></span>
- <span data-ttu-id="384e0-136">Várólista</span><span class="sxs-lookup"><span data-stu-id="384e0-136">Queue</span></span>
- <span data-ttu-id="384e0-137">Fájl</span><span class="sxs-lookup"><span data-stu-id="384e0-137">File</span></span>

<span data-ttu-id="384e0-138">A fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="384e0-138">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="384e0-139">-Verzió</span><span class="sxs-lookup"><span data-stu-id="384e0-139">-Version</span></span>
<span data-ttu-id="384e0-140">Az Azure Storage Service naplózásának verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="384e0-140">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="384e0-141">Az alapértelmezett érték a 1,0.</span><span class="sxs-lookup"><span data-stu-id="384e0-141">The default value is 1.0.</span></span>

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

### <span data-ttu-id="384e0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="384e0-142">CommonParameters</span></span>
<span data-ttu-id="384e0-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="384e0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="384e0-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="384e0-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="384e0-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="384e0-145">INPUTS</span></span>

### <span data-ttu-id="384e0-146">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="384e0-146">IStorageContext</span></span>

<span data-ttu-id="384e0-147">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="384e0-147">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="384e0-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="384e0-148">OUTPUTS</span></span>

### <span data-ttu-id="384e0-149">Microsoft. WindowsAzure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="384e0-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="384e0-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="384e0-150">NOTES</span></span>

## <span data-ttu-id="384e0-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="384e0-151">RELATED LINKS</span></span>

[<span data-ttu-id="384e0-152">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="384e0-152">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="384e0-153">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="384e0-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


