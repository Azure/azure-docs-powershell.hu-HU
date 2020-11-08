---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 84f6ae7f80eb7af3c4fccad08b0d9d2a20b0caeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187162"
---
# <span data-ttu-id="de604-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="de604-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="de604-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de604-102">SYNOPSIS</span></span>
<span data-ttu-id="de604-103">Könyvtárat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="de604-103">Creates a directory.</span></span>

## <span data-ttu-id="de604-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de604-104">SYNTAX</span></span>

### <span data-ttu-id="de604-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="de604-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="de604-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="de604-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="de604-107">Directory</span><span class="sxs-lookup"><span data-stu-id="de604-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="de604-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="de604-108">DESCRIPTION</span></span>
<span data-ttu-id="de604-109">A **New-AzStorageDirectory** parancsmag létrehoz egy könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="de604-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="de604-110">Ez a parancsmag egy **CloudFileDirectory** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="de604-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="de604-111">Példák</span><span class="sxs-lookup"><span data-stu-id="de604-111">EXAMPLES</span></span>

### <span data-ttu-id="de604-112">1. példa: mappa létrehozása a fájlmegosztási verzióban</span><span class="sxs-lookup"><span data-stu-id="de604-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="de604-113">Ez a parancs létrehoz egy ContosoWorkingFolder nevű mappát a ContosoShare06 nevű fájlmegosztás-megosztásban.</span><span class="sxs-lookup"><span data-stu-id="de604-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="de604-114">2. példa: a fájlmegosztási objektumban megadott fájlmegosztás mappa létrehozása</span><span class="sxs-lookup"><span data-stu-id="de604-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="de604-115">Ez a parancs a **Get-AzStorageShare** parancsmagot használja a ContosoShare06 nevű fájlmegosztás beolvasásához, majd átadja azt az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="de604-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="de604-116">Az aktuális parancsmag a ContosoWorkingFolder nevű mappát hozza létre a ContosoShare06-ban.</span><span class="sxs-lookup"><span data-stu-id="de604-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="de604-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de604-117">PARAMETERS</span></span>

### <span data-ttu-id="de604-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="de604-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="de604-119">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="de604-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="de604-120">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="de604-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="de604-121">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="de604-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de604-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="de604-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="de604-123">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="de604-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="de604-124">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="de604-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="de604-125">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="de604-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="de604-126">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="de604-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="de604-127">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="de604-127">The default value is 10.</span></span>

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

### <span data-ttu-id="de604-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="de604-128">-Context</span></span>
<span data-ttu-id="de604-129">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="de604-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="de604-130">A tárolási környezet eléréséhez használja a [New-AzStorageContext](./New-AzStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="de604-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="de604-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de604-131">-DefaultProfile</span></span>
<span data-ttu-id="de604-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de604-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de604-133">-Címtár</span><span class="sxs-lookup"><span data-stu-id="de604-133">-Directory</span></span>
<span data-ttu-id="de604-134">**CloudFileDirectory** -objektumként adja meg a mappát.</span><span class="sxs-lookup"><span data-stu-id="de604-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="de604-135">Ez a parancsmag hozza létre a mappát abban a helyen, ahol a paraméter meg van határozva.</span><span class="sxs-lookup"><span data-stu-id="de604-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="de604-136">Címtár beolvasásához használja az New-AzStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="de604-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="de604-137">A címtár eléréséhez használhatja az Get-AzStorageFile parancsmagot is.</span><span class="sxs-lookup"><span data-stu-id="de604-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de604-138">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="de604-138">-Path</span></span>
<span data-ttu-id="de604-139">A mappa elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="de604-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="de604-140">Ez a parancsmag létrehoz egy mappát a parancsmag elérési útjának elérési útjához.</span><span class="sxs-lookup"><span data-stu-id="de604-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="de604-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="de604-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="de604-142">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="de604-142">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de604-143">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="de604-143">-Share</span></span>
<span data-ttu-id="de604-144">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="de604-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="de604-145">Ez a parancsmag létrehoz egy mappát a fájlmegosztási fájlban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="de604-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="de604-146">**CloudFileShare** objektum beolvasásához használja az Get-AzStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="de604-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="de604-147">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="de604-147">This object contains the storage context.</span></span>
<span data-ttu-id="de604-148">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="de604-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de604-149">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="de604-149">-ShareName</span></span>
<span data-ttu-id="de604-150">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="de604-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="de604-151">Ez a parancsmag létrehoz egy mappát a fájlmegosztási fájlban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="de604-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="de604-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de604-152">CommonParameters</span></span>
<span data-ttu-id="de604-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de604-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de604-154">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de604-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de604-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de604-155">INPUTS</span></span>

### <span data-ttu-id="de604-156">Microsoft. Azure. Storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="de604-156">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="de604-157">Microsoft. Azure. Storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="de604-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="de604-158">System. String</span><span class="sxs-lookup"><span data-stu-id="de604-158">System.String</span></span>

### <span data-ttu-id="de604-159">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="de604-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="de604-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de604-160">OUTPUTS</span></span>

### <span data-ttu-id="de604-161">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="de604-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="de604-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de604-162">NOTES</span></span>

## <span data-ttu-id="de604-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de604-163">RELATED LINKS</span></span>

[<span data-ttu-id="de604-164">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="de604-164">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="de604-165">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="de604-165">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="de604-166">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="de604-166">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="de604-167">Új – AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="de604-167">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="de604-168">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="de604-168">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)
