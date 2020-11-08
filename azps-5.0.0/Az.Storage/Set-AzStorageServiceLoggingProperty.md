---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 21c182dff12f8dd373000a295f964bd59484e337
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185762"
---
# <span data-ttu-id="e1fc4-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e1fc4-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="e1fc4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="e1fc4-103">Az Azure Storage Services naplózásának módosítása.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="e1fc4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1fc4-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1fc4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1fc4-105">DESCRIPTION</span></span>
<span data-ttu-id="e1fc4-106">A **set-AzStorageServiceLoggingProperty** parancsmag az Azure Storage Services naplózását módosítja.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="e1fc4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e1fc4-107">EXAMPLES</span></span>

### <span data-ttu-id="e1fc4-108">1. példa: a blob-szolgáltatás naplózási tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="e1fc4-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="e1fc4-109">Ez a parancs módosítja a 1,0-ös verzió naplózását a blob-tárolóhoz az olvasási és írási műveletek elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="e1fc4-110">Az Azure Storage Service naplózása 10 napra megőrzi a bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="e1fc4-111">Mivel a parancs a *PassThru* paramétert adja meg, a parancs a módosított naplózási tulajdonságokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="e1fc4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1fc4-112">PARAMETERS</span></span>

### <span data-ttu-id="e1fc4-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e1fc4-113">-Context</span></span>
<span data-ttu-id="e1fc4-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e1fc4-115">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e1fc4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1fc4-116">-DefaultProfile</span></span>
<span data-ttu-id="e1fc4-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1fc4-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="e1fc4-118">-LoggingOperations</span></span>
<span data-ttu-id="e1fc4-119">Az Azure Storage Service-műveletek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="e1fc4-120">Az Azure Storage Services naplózza azokat a műveleteket, amelyeket a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="e1fc4-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e1fc4-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e1fc4-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="e1fc4-122">None</span></span>
- <span data-ttu-id="e1fc4-123">Olvasása</span><span class="sxs-lookup"><span data-stu-id="e1fc4-123">Read</span></span>
- <span data-ttu-id="e1fc4-124">Írni</span><span class="sxs-lookup"><span data-stu-id="e1fc4-124">Write</span></span>
- <span data-ttu-id="e1fc4-125">Törlése</span><span class="sxs-lookup"><span data-stu-id="e1fc4-125">Delete</span></span>
- <span data-ttu-id="e1fc4-126">Minden</span><span class="sxs-lookup"><span data-stu-id="e1fc4-126">All</span></span>

```yaml
Type: Microsoft.Azure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1fc4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1fc4-127">-PassThru</span></span>
<span data-ttu-id="e1fc4-128">Azt jelzi, hogy ez a parancsmag a frissített naplózási tulajdonságokat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="e1fc4-129">Ha nem adja meg ezt a paramétert, ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e1fc4-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="e1fc4-130">-RetentionDays</span></span>
<span data-ttu-id="e1fc4-131">Annak a napoknak a száma, ameddig az Azure Storage szolgáltatás megőrzi a naplózási információkat.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="e1fc4-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="e1fc4-132">-ServiceType</span></span>
<span data-ttu-id="e1fc4-133">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-133">Specifies the storage service type.</span></span>
<span data-ttu-id="e1fc4-134">Ez a parancsmag módosítja a szolgáltatás típusának naplózási tulajdonságait, amelyeket a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="e1fc4-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e1fc4-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e1fc4-136">BLOB</span><span class="sxs-lookup"><span data-stu-id="e1fc4-136">Blob</span></span> 
- <span data-ttu-id="e1fc4-137">Táblázat</span><span class="sxs-lookup"><span data-stu-id="e1fc4-137">Table</span></span>
- <span data-ttu-id="e1fc4-138">Várólista</span><span class="sxs-lookup"><span data-stu-id="e1fc4-138">Queue</span></span>
- <span data-ttu-id="e1fc4-139">Fájl: a fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="e1fc4-140">-Verzió</span><span class="sxs-lookup"><span data-stu-id="e1fc4-140">-Version</span></span>
<span data-ttu-id="e1fc4-141">Az Azure Storage Service naplózásának verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="e1fc4-142">Az alapértelmezett érték a 1,0.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="e1fc4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1fc4-143">CommonParameters</span></span>
<span data-ttu-id="e1fc4-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1fc4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1fc4-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1fc4-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1fc4-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1fc4-146">INPUTS</span></span>

### <span data-ttu-id="e1fc4-147">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e1fc4-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e1fc4-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1fc4-148">OUTPUTS</span></span>

### <span data-ttu-id="e1fc4-149">Microsoft. Azure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="e1fc4-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="e1fc4-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1fc4-150">NOTES</span></span>

## <span data-ttu-id="e1fc4-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1fc4-151">RELATED LINKS</span></span>

[<span data-ttu-id="e1fc4-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e1fc4-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="e1fc4-153">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e1fc4-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


