---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageFile.md
ms.openlocfilehash: 4752612120da1f89729299c41df1b7af78580f92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492934"
---
# <span data-ttu-id="0a6b9-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="0a6b9-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="0a6b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6b9-103">Töröl egy fájlt.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-103">Deletes a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a6b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a6b9-104">SYNTAX</span></span>

### <span data-ttu-id="0a6b9-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0a6b9-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a6b9-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="0a6b9-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a6b9-107">Directory</span><span class="sxs-lookup"><span data-stu-id="0a6b9-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a6b9-108">Fájl</span><span class="sxs-lookup"><span data-stu-id="0a6b9-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a6b9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a6b9-109">DESCRIPTION</span></span>
<span data-ttu-id="0a6b9-110">A **Remove-AzureStorageFile** parancsmag töröl egy fájlt.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="0a6b9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0a6b9-111">EXAMPLES</span></span>

### <span data-ttu-id="0a6b9-112">1. példa: fájl törlése a fájl-megosztásból</span><span class="sxs-lookup"><span data-stu-id="0a6b9-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="0a6b9-113">Ez a parancs törli a ContosoFile22 nevű fájlt a ContosoShare06 nevű fájlmegosztás-megosztásból.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="0a6b9-114">2. példa: fájlmegosztás-objektum használatával beolvashatja a fájlt a fájlból.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="0a6b9-115">Ez a parancs a **Get-AzureStorageShare** parancsmagot használja a ContosoShare06 nevű fájlmegosztás beszerzéséhez, majd a csővezeték-kezelő segítségével átadja az objektumot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0a6b9-116">A jelenlegi parancs törli a ContosoFile22 nevű fájlt a ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="0a6b9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a6b9-117">PARAMETERS</span></span>

### <span data-ttu-id="0a6b9-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0a6b9-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0a6b9-119">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0a6b9-120">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0a6b9-121">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0a6b9-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0a6b9-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0a6b9-123">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0a6b9-124">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0a6b9-125">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0a6b9-126">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="0a6b9-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0a6b9-127">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-127">The default value is 10.</span></span>

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

### <span data-ttu-id="0a6b9-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0a6b9-128">-Context</span></span>
<span data-ttu-id="0a6b9-129">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0a6b9-130">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="0a6b9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6b9-131">-DefaultProfile</span></span>
<span data-ttu-id="0a6b9-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a6b9-133">-Címtár</span><span class="sxs-lookup"><span data-stu-id="0a6b9-133">-Directory</span></span>
<span data-ttu-id="0a6b9-134">**CloudFileDirectory** -objektumként adja meg a mappát.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="0a6b9-135">Ez a parancsmag eltávolítja a fájl azon mappáját, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="0a6b9-136">-Fájl</span><span class="sxs-lookup"><span data-stu-id="0a6b9-136">-File</span></span>
<span data-ttu-id="0a6b9-137">A fájlt **CloudFile** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="0a6b9-138">Ez a parancsmag eltávolítja a paraméter által megadott fájlt.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="0a6b9-139">**CloudFile** objektum beolvasásához használja az Get-AzureStorageFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-139">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6b9-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a6b9-140">-PassThru</span></span>
<span data-ttu-id="0a6b9-141">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="0a6b9-142">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="0a6b9-143">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="0a6b9-143">-Path</span></span>
<span data-ttu-id="0a6b9-144">A fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-144">Specifies the path of a file.</span></span>
<span data-ttu-id="0a6b9-145">Ez a parancsmag törli a paraméter által megadott fájlt.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-145">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6b9-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0a6b9-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0a6b9-147">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="0a6b9-148">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="0a6b9-148">-Share</span></span>
<span data-ttu-id="0a6b9-149">Egy **CloudFileShare** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="0a6b9-150">Ez a parancsmag eltávolítja a fájlt a megosztás ebben a paraméterben beállításban.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="0a6b9-151">**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-151">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="0a6b9-152">Ez az objektum a tárolási környezetet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-152">This object contains the storage context.</span></span>
<span data-ttu-id="0a6b9-153">Ha ezt a paramétert adja meg, ne adja meg a *környezeti* paramétert.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="0a6b9-154">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="0a6b9-154">-ShareName</span></span>
<span data-ttu-id="0a6b9-155">Itt adhatja meg a fájl megosztásának a nevét.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="0a6b9-156">Ez a parancsmag eltávolítja a fájlt a megosztás ebben a paraméterben beállításban.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="0a6b9-157">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0a6b9-157">-Confirm</span></span>
<span data-ttu-id="0a6b9-158">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6b9-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a6b9-159">-WhatIf</span></span>
<span data-ttu-id="0a6b9-160">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a6b9-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a6b9-161">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6b9-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6b9-162">CommonParameters</span></span>
<span data-ttu-id="0a6b9-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a6b9-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6b9-164">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a6b9-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6b9-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a6b9-165">INPUTS</span></span>

### <span data-ttu-id="0a6b9-166">Microsoft. WindowsAzure. Storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="0a6b9-166">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="0a6b9-167">Paraméterek: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0a6b9-167">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="0a6b9-168">Microsoft. WindowsAzure. Storage. file. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="0a6b9-168">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="0a6b9-169">Paraméterek: címtár (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0a6b9-169">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="0a6b9-170">Microsoft. WindowsAzure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="0a6b9-170">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="0a6b9-171">Paraméterek: fájl (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0a6b9-171">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="0a6b9-172">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0a6b9-172">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0a6b9-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a6b9-173">OUTPUTS</span></span>

### <span data-ttu-id="0a6b9-174">Microsoft. WindowsAzure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="0a6b9-174">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="0a6b9-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a6b9-175">NOTES</span></span>

## <span data-ttu-id="0a6b9-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a6b9-176">RELATED LINKS</span></span>

[<span data-ttu-id="0a6b9-177">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="0a6b9-177">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="0a6b9-178">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="0a6b9-178">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="0a6b9-179">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="0a6b9-179">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
