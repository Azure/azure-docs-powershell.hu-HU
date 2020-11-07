---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageserviceloggingproperty
schema: 2.0.0
ms.openlocfilehash: 810dc3246e1b1d49db491c030446117dbabfb548
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850974"
---
# <span data-ttu-id="940ea-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="940ea-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="940ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="940ea-102">SYNOPSIS</span></span>
<span data-ttu-id="940ea-103">Az Azure Storage Services naplózásának módosítása.</span><span class="sxs-lookup"><span data-stu-id="940ea-103">Modifies logging for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="940ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="940ea-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="940ea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="940ea-105">DESCRIPTION</span></span>
<span data-ttu-id="940ea-106">A **set-AzureStorageServiceLoggingProperty** parancsmag az Azure Storage Services naplózását módosítja.</span><span class="sxs-lookup"><span data-stu-id="940ea-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="940ea-107">Példák</span><span class="sxs-lookup"><span data-stu-id="940ea-107">EXAMPLES</span></span>

### <span data-ttu-id="940ea-108">1. példa: a blob-szolgáltatás naplózási tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="940ea-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="940ea-109">Ez a parancs módosítja a 1,0-ös verzió naplózását a blob-tárolóhoz az olvasási és írási műveletek elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="940ea-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="940ea-110">Az Azure Storage Service naplózása 10 napra megőrzi a bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="940ea-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="940ea-111">Mivel a parancs a *PassThru* paramétert adja meg, a parancs a módosított naplózási tulajdonságokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="940ea-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="940ea-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="940ea-112">PARAMETERS</span></span>

### <span data-ttu-id="940ea-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="940ea-113">-Context</span></span>
<span data-ttu-id="940ea-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="940ea-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="940ea-115">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="940ea-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="940ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="940ea-116">-DefaultProfile</span></span>
<span data-ttu-id="940ea-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="940ea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="940ea-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="940ea-118">-LoggingOperations</span></span>
<span data-ttu-id="940ea-119">Az Azure Storage Service-műveletek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="940ea-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="940ea-120">Az Azure Storage Services naplózza azokat a műveleteket, amelyeket a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="940ea-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="940ea-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="940ea-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="940ea-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="940ea-122">None</span></span>
- <span data-ttu-id="940ea-123">Olvasása</span><span class="sxs-lookup"><span data-stu-id="940ea-123">Read</span></span>
- <span data-ttu-id="940ea-124">Írni</span><span class="sxs-lookup"><span data-stu-id="940ea-124">Write</span></span>
- <span data-ttu-id="940ea-125">Törlése</span><span class="sxs-lookup"><span data-stu-id="940ea-125">Delete</span></span>
- <span data-ttu-id="940ea-126">Minden</span><span class="sxs-lookup"><span data-stu-id="940ea-126">All</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940ea-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="940ea-127">-PassThru</span></span>
<span data-ttu-id="940ea-128">Azt jelzi, hogy ez a parancsmag a frissített naplózási tulajdonságokat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="940ea-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="940ea-129">Ha nem adja meg ezt a paramétert, ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="940ea-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="940ea-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="940ea-130">-RetentionDays</span></span>
<span data-ttu-id="940ea-131">Annak a napoknak a száma, ameddig az Azure Storage szolgáltatás megőrzi a naplózási információkat.</span><span class="sxs-lookup"><span data-stu-id="940ea-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="940ea-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="940ea-132">-ServiceType</span></span>
<span data-ttu-id="940ea-133">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="940ea-133">Specifies the storage service type.</span></span>
<span data-ttu-id="940ea-134">Ez a parancsmag módosítja a szolgáltatás típusának naplózási tulajdonságait, amelyeket a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="940ea-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="940ea-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="940ea-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="940ea-136">BLOB</span><span class="sxs-lookup"><span data-stu-id="940ea-136">Blob</span></span> 
- <span data-ttu-id="940ea-137">Táblázat</span><span class="sxs-lookup"><span data-stu-id="940ea-137">Table</span></span>
- <span data-ttu-id="940ea-138">Várólista</span><span class="sxs-lookup"><span data-stu-id="940ea-138">Queue</span></span>
- <span data-ttu-id="940ea-139">Fájl: a fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="940ea-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="940ea-140">-Verzió</span><span class="sxs-lookup"><span data-stu-id="940ea-140">-Version</span></span>
<span data-ttu-id="940ea-141">Az Azure Storage Service naplózásának verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="940ea-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="940ea-142">Az alapértelmezett érték a 1,0.</span><span class="sxs-lookup"><span data-stu-id="940ea-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="940ea-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="940ea-143">CommonParameters</span></span>
<span data-ttu-id="940ea-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="940ea-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="940ea-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="940ea-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="940ea-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="940ea-146">INPUTS</span></span>

### <span data-ttu-id="940ea-147">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="940ea-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="940ea-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="940ea-148">OUTPUTS</span></span>

### <span data-ttu-id="940ea-149">Microsoft. WindowsAzure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="940ea-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="940ea-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="940ea-150">NOTES</span></span>

## <span data-ttu-id="940ea-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="940ea-151">RELATED LINKS</span></span>

[<span data-ttu-id="940ea-152">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="940ea-152">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="940ea-153">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="940ea-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


