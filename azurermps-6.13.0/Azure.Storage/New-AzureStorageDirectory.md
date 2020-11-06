---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageDirectory.md
ms.openlocfilehash: b5d28a2c156572909f5d1e943473dbbf2c527d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498623"
---
# <span data-ttu-id="3679b-101">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="3679b-101">New-AzureStorageDirectory</span></span>

## <span data-ttu-id="3679b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3679b-102">SYNOPSIS</span></span>
<span data-ttu-id="3679b-103">Könyvtárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3679b-103">Creates a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3679b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3679b-104">SYNTAX</span></span>

### <span data-ttu-id="3679b-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3679b-105">ShareName (Default)</span></span>
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3679b-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="3679b-106">Share</span></span>
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="3679b-107">Directory</span><span class="sxs-lookup"><span data-stu-id="3679b-107">Directory</span></span>
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="3679b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3679b-108">DESCRIPTION</span></span>
<span data-ttu-id="3679b-109">A **New-AzureStorageDirectory** parancsmag létrehoz egy könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="3679b-109">The **New-AzureStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="3679b-110">Ez a parancsmag egy **CloudFileDirectory** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="3679b-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="3679b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3679b-111">EXAMPLES</span></span>

### <span data-ttu-id="3679b-112">1. példa: mappa létrehozása a fájlmegosztási verzióban</span><span class="sxs-lookup"><span data-stu-id="3679b-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="3679b-113">Ez a parancs létrehoz egy ContosoWorkingFolder nevű mappát a ContosoShare06 nevű fájlmegosztás-megosztásban.</span><span class="sxs-lookup"><span data-stu-id="3679b-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="3679b-114">2. példa: a fájlmegosztási objektumban megadott fájlmegosztás mappa létrehozása</span><span class="sxs-lookup"><span data-stu-id="3679b-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="3679b-115">Ez a parancs a **Get-AzureStorageShare** parancsmagot használja a ContosoShare06 nevű fájlmegosztás beolvasásához, majd átadja azt az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="3679b-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3679b-116">Az aktuális parancsmag a ContosoWorkingFolder nevű mappát hozza létre a ContosoShare06-ban.</span><span class="sxs-lookup"><span data-stu-id="3679b-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="3679b-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3679b-117">PARAMETERS</span></span>

### <span data-ttu-id="3679b-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3679b-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3679b-119">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="3679b-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3679b-120">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="3679b-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3679b-121">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="3679b-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3679b-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3679b-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3679b-123">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="3679b-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3679b-124">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="3679b-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3679b-125">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="3679b-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3679b-126">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="3679b-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3679b-127">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="3679b-127">The default value is 10.</span></span>

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

### <span data-ttu-id="3679b-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3679b-128">-Context</span></span>
<span data-ttu-id="3679b-129">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3679b-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3679b-130">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3679b-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3679b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3679b-131">-DefaultProfile</span></span>
<span data-ttu-id="3679b-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3679b-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3679b-133">-Címtár</span><span class="sxs-lookup"><span data-stu-id="3679b-133">-Directory</span></span>
<span data-ttu-id="3679b-134">**CloudFileDirectory** -objektumként adja meg a mappát.</span><span class="sxs-lookup"><span data-stu-id="3679b-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="3679b-135">Ez a parancsmag hozza létre a mappát abban a helyen, ahol a paraméter meg van határozva.</span><span class="sxs-lookup"><span data-stu-id="3679b-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="3679b-136">Címtár beolvasásához használja az New-AzureStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3679b-136">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="3679b-137">A címtár eléréséhez használhatja az Get-AzureStorageFile parancsmagot is.</span><span class="sxs-lookup"><span data-stu-id="3679b-137">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3679b-138">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="3679b-138">-Path</span></span>
<span data-ttu-id="3679b-139">A mappa elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3679b-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="3679b-140">Ez a parancsmag létrehoz egy mappát a parancsmag elérési útjának elérési útjához.</span><span class="sxs-lookup"><span data-stu-id="3679b-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3679b-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3679b-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3679b-142">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3679b-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3679b-143">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="3679b-143">-Share</span></span>
<span data-ttu-id="3679b-144">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="3679b-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="3679b-145">Ez a parancsmag létrehoz egy mappát a fájlmegosztási fájlban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="3679b-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="3679b-146">**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3679b-146">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="3679b-147">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3679b-147">This object contains the storage context.</span></span>
<span data-ttu-id="3679b-148">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="3679b-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3679b-149">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="3679b-149">-ShareName</span></span>
<span data-ttu-id="3679b-150">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="3679b-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="3679b-151">Ez a parancsmag létrehoz egy mappát a fájlmegosztási fájlban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="3679b-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3679b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3679b-152">CommonParameters</span></span>
<span data-ttu-id="3679b-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3679b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3679b-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3679b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3679b-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3679b-155">INPUTS</span></span>

### <span data-ttu-id="3679b-156">Microsoft. WindowsAzure. Storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="3679b-156">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="3679b-157">Paraméterek: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3679b-157">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="3679b-158">Microsoft. WindowsAzure. Storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="3679b-158">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="3679b-159">Paraméterek: címtár (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3679b-159">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="3679b-160">System. String</span><span class="sxs-lookup"><span data-stu-id="3679b-160">System.String</span></span>

### <span data-ttu-id="3679b-161">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3679b-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3679b-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3679b-162">OUTPUTS</span></span>

### <span data-ttu-id="3679b-163">Microsoft. WindowsAzure. Storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="3679b-163">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="3679b-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3679b-164">NOTES</span></span>

## <span data-ttu-id="3679b-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3679b-165">RELATED LINKS</span></span>

[<span data-ttu-id="3679b-166">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="3679b-166">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="3679b-167">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="3679b-167">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="3679b-168">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3679b-168">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3679b-169">Új – AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="3679b-169">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="3679b-170">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="3679b-170">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)
