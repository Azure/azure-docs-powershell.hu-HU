---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 4d671e99ed8b5c26b98b8e224728785e034e450b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668530"
---
# <span data-ttu-id="f7694-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f7694-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="f7694-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7694-102">SYNOPSIS</span></span>
<span data-ttu-id="f7694-103">Az Azure Storage Services naplózásának módosítása.</span><span class="sxs-lookup"><span data-stu-id="f7694-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="f7694-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7694-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7694-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7694-105">DESCRIPTION</span></span>
<span data-ttu-id="f7694-106">A **set-AzStorageServiceLoggingProperty** parancsmag az Azure Storage Services naplózását módosítja.</span><span class="sxs-lookup"><span data-stu-id="f7694-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="f7694-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f7694-107">EXAMPLES</span></span>

### <span data-ttu-id="f7694-108">1. példa: a blob-szolgáltatás naplózási tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="f7694-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="f7694-109">Ez a parancs módosítja a 1,0-ös verzió naplózását a blob-tárolóhoz az olvasási és írási műveletek elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="f7694-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="f7694-110">Az Azure Storage Service naplózása 10 napra megőrzi a bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="f7694-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="f7694-111">Mivel a parancs a *PassThru* paramétert adja meg, a parancs a módosított naplózási tulajdonságokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="f7694-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="f7694-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7694-112">PARAMETERS</span></span>

### <span data-ttu-id="f7694-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f7694-113">-Context</span></span>
<span data-ttu-id="f7694-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7694-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f7694-115">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f7694-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f7694-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7694-116">-DefaultProfile</span></span>
<span data-ttu-id="f7694-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7694-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7694-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="f7694-118">-LoggingOperations</span></span>
<span data-ttu-id="f7694-119">Az Azure Storage Service-műveletek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7694-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="f7694-120">Az Azure Storage Services naplózza azokat a műveleteket, amelyeket a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="f7694-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="f7694-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f7694-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f7694-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="f7694-122">None</span></span>
- <span data-ttu-id="f7694-123">Olvasása</span><span class="sxs-lookup"><span data-stu-id="f7694-123">Read</span></span>
- <span data-ttu-id="f7694-124">Írni</span><span class="sxs-lookup"><span data-stu-id="f7694-124">Write</span></span>
- <span data-ttu-id="f7694-125">Törlése</span><span class="sxs-lookup"><span data-stu-id="f7694-125">Delete</span></span>
- <span data-ttu-id="f7694-126">Minden</span><span class="sxs-lookup"><span data-stu-id="f7694-126">All</span></span>

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

### <span data-ttu-id="f7694-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7694-127">-PassThru</span></span>
<span data-ttu-id="f7694-128">Azt jelzi, hogy ez a parancsmag a frissített naplózási tulajdonságokat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f7694-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="f7694-129">Ha nem adja meg ezt a paramétert, ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="f7694-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f7694-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="f7694-130">-RetentionDays</span></span>
<span data-ttu-id="f7694-131">Annak a napoknak a száma, ameddig az Azure Storage szolgáltatás megőrzi a naplózási információkat.</span><span class="sxs-lookup"><span data-stu-id="f7694-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="f7694-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="f7694-132">-ServiceType</span></span>
<span data-ttu-id="f7694-133">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7694-133">Specifies the storage service type.</span></span>
<span data-ttu-id="f7694-134">Ez a parancsmag módosítja a szolgáltatás típusának naplózási tulajdonságait, amelyeket a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="f7694-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="f7694-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f7694-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f7694-136">BLOB</span><span class="sxs-lookup"><span data-stu-id="f7694-136">Blob</span></span> 
- <span data-ttu-id="f7694-137">Táblázat</span><span class="sxs-lookup"><span data-stu-id="f7694-137">Table</span></span>
- <span data-ttu-id="f7694-138">Várólista</span><span class="sxs-lookup"><span data-stu-id="f7694-138">Queue</span></span>
- <span data-ttu-id="f7694-139">Fájl: a fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="f7694-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="f7694-140">-Verzió</span><span class="sxs-lookup"><span data-stu-id="f7694-140">-Version</span></span>
<span data-ttu-id="f7694-141">Az Azure Storage Service naplózásának verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7694-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="f7694-142">Az alapértelmezett érték a 1,0.</span><span class="sxs-lookup"><span data-stu-id="f7694-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="f7694-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7694-143">CommonParameters</span></span>
<span data-ttu-id="f7694-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7694-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7694-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7694-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7694-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7694-146">INPUTS</span></span>

### <span data-ttu-id="f7694-147">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f7694-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f7694-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7694-148">OUTPUTS</span></span>

### <span data-ttu-id="f7694-149">Microsoft. WindowsAzure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="f7694-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="f7694-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7694-150">NOTES</span></span>

## <span data-ttu-id="f7694-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7694-151">RELATED LINKS</span></span>

[<span data-ttu-id="f7694-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f7694-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="f7694-153">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f7694-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


