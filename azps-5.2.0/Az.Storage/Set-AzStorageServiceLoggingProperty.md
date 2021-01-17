---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 21c182dff12f8dd373000a295f964bd59484e337
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348210"
---
# <span data-ttu-id="4b6bb-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="4b6bb-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="4b6bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b6bb-102">SYNOPSIS</span></span>
<span data-ttu-id="4b6bb-103">Módosítja az Azure Storage-szolgáltatások naplózását.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="4b6bb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4b6bb-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b6bb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4b6bb-105">DESCRIPTION</span></span>
<span data-ttu-id="4b6bb-106">A **Set-AzStorageServiceLoggingProperty** parancsmag módosítja az Azure Storage-szolgáltatások naplózását.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="4b6bb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4b6bb-107">EXAMPLES</span></span>

### <span data-ttu-id="4b6bb-108">1. példa: A Blob szolgáltatás naplózási tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="4b6bb-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="4b6bb-109">Ez a parancs módosítja az 1.0-s verzió naplózását a blobtárolóhoz olvasási és írási műveletekre.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="4b6bb-110">Az Azure Storage szolgáltatás naplózása 10 napig őrzi meg a bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="4b6bb-111">Mivel ez a parancs megadja *a PassThru* paramétert, a parancs megjeleníti a módosított naplózási tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="4b6bb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b6bb-112">PARAMETERS</span></span>

### <span data-ttu-id="4b6bb-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4b6bb-113">-Context</span></span>
<span data-ttu-id="4b6bb-114">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4b6bb-115">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4b6bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b6bb-116">-DefaultProfile</span></span>
<span data-ttu-id="4b6bb-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b6bb-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="4b6bb-118">-LoggingOperations</span></span>
<span data-ttu-id="4b6bb-119">Az Azure Storage szolgáltatásműveletei tömbje.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="4b6bb-120">Az Azure Storage Services naplózza a paraméter által megadott műveleteket.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="4b6bb-121">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="4b6bb-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4b6bb-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="4b6bb-122">None</span></span>
- <span data-ttu-id="4b6bb-123">Olvasás</span><span class="sxs-lookup"><span data-stu-id="4b6bb-123">Read</span></span>
- <span data-ttu-id="4b6bb-124">Írás</span><span class="sxs-lookup"><span data-stu-id="4b6bb-124">Write</span></span>
- <span data-ttu-id="4b6bb-125">Törlés</span><span class="sxs-lookup"><span data-stu-id="4b6bb-125">Delete</span></span>
- <span data-ttu-id="4b6bb-126">Mind</span><span class="sxs-lookup"><span data-stu-id="4b6bb-126">All</span></span>

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

### <span data-ttu-id="4b6bb-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b6bb-127">-PassThru</span></span>
<span data-ttu-id="4b6bb-128">Azt jelzi, hogy ez a parancsmag a frissített naplózási tulajdonságokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="4b6bb-129">Ha nem adja meg ezt a paramétert, ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4b6bb-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="4b6bb-130">-RetentionDays</span></span>
<span data-ttu-id="4b6bb-131">Azt adja meg, hogy az Azure Storage szolgáltatás hány napig őrzi meg a naplózott adatokat.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="4b6bb-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="4b6bb-132">-ServiceType</span></span>
<span data-ttu-id="4b6bb-133">A társzolgáltatás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-133">Specifies the storage service type.</span></span>
<span data-ttu-id="4b6bb-134">Ez a parancsmag módosítja a paraméter által megadott szolgáltatástípus naplózási tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="4b6bb-135">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="4b6bb-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4b6bb-136">Blob</span><span class="sxs-lookup"><span data-stu-id="4b6bb-136">Blob</span></span> 
- <span data-ttu-id="4b6bb-137">Táblázat</span><span class="sxs-lookup"><span data-stu-id="4b6bb-137">Table</span></span>
- <span data-ttu-id="4b6bb-138">Várólistán</span><span class="sxs-lookup"><span data-stu-id="4b6bb-138">Queue</span></span>
- <span data-ttu-id="4b6bb-139">Fájl: A fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="4b6bb-140">-Version</span><span class="sxs-lookup"><span data-stu-id="4b6bb-140">-Version</span></span>
<span data-ttu-id="4b6bb-141">Az Azure Storage szolgáltatás naplózási verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="4b6bb-142">Az alapértelmezett érték 1,0.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="4b6bb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b6bb-143">CommonParameters</span></span>
<span data-ttu-id="4b6bb-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b6bb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b6bb-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b6bb-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b6bb-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b6bb-146">INPUTS</span></span>

### <span data-ttu-id="4b6bb-147">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4b6bb-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4b6bb-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b6bb-148">OUTPUTS</span></span>

### <span data-ttu-id="4b6bb-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="4b6bb-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="4b6bb-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4b6bb-150">NOTES</span></span>

## <span data-ttu-id="4b6bb-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b6bb-151">RELATED LINKS</span></span>

[<span data-ttu-id="4b6bb-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="4b6bb-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="4b6bb-153">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="4b6bb-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


