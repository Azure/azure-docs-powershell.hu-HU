---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 84eae2221564d1c1a569ea5469c44cb1cd628b04
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929682"
---
# <span data-ttu-id="1caa5-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1caa5-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="1caa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1caa5-102">SYNOPSIS</span></span>
<span data-ttu-id="1caa5-103">Módosítja az Azure Storage-szolgáltatások naplózását.</span><span class="sxs-lookup"><span data-stu-id="1caa5-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="1caa5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1caa5-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1caa5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1caa5-105">DESCRIPTION</span></span>
<span data-ttu-id="1caa5-106">A **Set-AzStorageServiceLoggingProperty** parancsmag módosítja az Azure Storage-szolgáltatások naplózását.</span><span class="sxs-lookup"><span data-stu-id="1caa5-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="1caa5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1caa5-107">EXAMPLES</span></span>

### <span data-ttu-id="1caa5-108">1. példa: A Blob szolgáltatás naplózási tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="1caa5-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="1caa5-109">Ez a parancs módosítja az 1.0-s verzió naplózását a blobtárolóhoz olvasási és írási műveletekre.</span><span class="sxs-lookup"><span data-stu-id="1caa5-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="1caa5-110">Az Azure Storage szolgáltatás naplózása 10 napig őrzi meg a bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="1caa5-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="1caa5-111">Mivel ez a parancs megadja *a PassThru* paramétert, a parancs megjeleníti a módosított naplózási tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="1caa5-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="1caa5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1caa5-112">PARAMETERS</span></span>

### <span data-ttu-id="1caa5-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1caa5-113">-Context</span></span>
<span data-ttu-id="1caa5-114">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1caa5-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1caa5-115">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1caa5-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1caa5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1caa5-116">-DefaultProfile</span></span>
<span data-ttu-id="1caa5-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1caa5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1caa5-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="1caa5-118">-LoggingOperations</span></span>
<span data-ttu-id="1caa5-119">Az Azure Storage szolgáltatásműveletei tömbje.</span><span class="sxs-lookup"><span data-stu-id="1caa5-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="1caa5-120">Az Azure Storage Services naplózza a paraméter által megadott műveleteket.</span><span class="sxs-lookup"><span data-stu-id="1caa5-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="1caa5-121">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="1caa5-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1caa5-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="1caa5-122">None</span></span>
- <span data-ttu-id="1caa5-123">Olvasás</span><span class="sxs-lookup"><span data-stu-id="1caa5-123">Read</span></span>
- <span data-ttu-id="1caa5-124">Írás</span><span class="sxs-lookup"><span data-stu-id="1caa5-124">Write</span></span>
- <span data-ttu-id="1caa5-125">Törlés</span><span class="sxs-lookup"><span data-stu-id="1caa5-125">Delete</span></span>
- <span data-ttu-id="1caa5-126">Mind</span><span class="sxs-lookup"><span data-stu-id="1caa5-126">All</span></span>

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

### <span data-ttu-id="1caa5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1caa5-127">-PassThru</span></span>
<span data-ttu-id="1caa5-128">Azt jelzi, hogy ez a parancsmag a frissített naplózási tulajdonságokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="1caa5-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="1caa5-129">Ha nem adja meg ezt a paramétert, ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="1caa5-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1caa5-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="1caa5-130">-RetentionDays</span></span>
<span data-ttu-id="1caa5-131">Azt adja meg, hogy az Azure Storage szolgáltatás hány napig őrzi meg a naplózott adatokat.</span><span class="sxs-lookup"><span data-stu-id="1caa5-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="1caa5-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="1caa5-132">-ServiceType</span></span>
<span data-ttu-id="1caa5-133">A társzolgáltatás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="1caa5-133">Specifies the storage service type.</span></span>
<span data-ttu-id="1caa5-134">Ez a parancsmag módosítja a paraméter által megadott szolgáltatástípus naplózási tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="1caa5-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="1caa5-135">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="1caa5-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1caa5-136">Blob</span><span class="sxs-lookup"><span data-stu-id="1caa5-136">Blob</span></span> 
- <span data-ttu-id="1caa5-137">Táblázat</span><span class="sxs-lookup"><span data-stu-id="1caa5-137">Table</span></span>
- <span data-ttu-id="1caa5-138">Várólistán</span><span class="sxs-lookup"><span data-stu-id="1caa5-138">Queue</span></span>
- <span data-ttu-id="1caa5-139">Fájl: A fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="1caa5-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="1caa5-140">-Version</span><span class="sxs-lookup"><span data-stu-id="1caa5-140">-Version</span></span>
<span data-ttu-id="1caa5-141">Az Azure Storage szolgáltatás naplózási verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="1caa5-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="1caa5-142">Az alapértelmezett érték 1,0.</span><span class="sxs-lookup"><span data-stu-id="1caa5-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="1caa5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1caa5-143">CommonParameters</span></span>
<span data-ttu-id="1caa5-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1caa5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1caa5-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1caa5-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1caa5-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1caa5-146">INPUTS</span></span>

### <span data-ttu-id="1caa5-147">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1caa5-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1caa5-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1caa5-148">OUTPUTS</span></span>

### <span data-ttu-id="1caa5-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="1caa5-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="1caa5-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1caa5-150">NOTES</span></span>

## <span data-ttu-id="1caa5-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1caa5-151">RELATED LINKS</span></span>

[<span data-ttu-id="1caa5-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1caa5-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="1caa5-153">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="1caa5-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


