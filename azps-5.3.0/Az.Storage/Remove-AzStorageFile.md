---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: 99809e5115cb256b8e546334efce0e6e399be04f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466907"
---
# <span data-ttu-id="a83f7-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="a83f7-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="a83f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a83f7-102">SYNOPSIS</span></span>
<span data-ttu-id="a83f7-103">Fájl törlése.</span><span class="sxs-lookup"><span data-stu-id="a83f7-103">Deletes a file.</span></span>

## <span data-ttu-id="a83f7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a83f7-104">SYNTAX</span></span>

### <span data-ttu-id="a83f7-105">ShareName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a83f7-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a83f7-106">Megosztás</span><span class="sxs-lookup"><span data-stu-id="a83f7-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a83f7-107">Címtár</span><span class="sxs-lookup"><span data-stu-id="a83f7-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a83f7-108">Fájl</span><span class="sxs-lookup"><span data-stu-id="a83f7-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a83f7-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a83f7-109">DESCRIPTION</span></span>
<span data-ttu-id="a83f7-110">A **Remove-AzStorageFile** parancsmag töröl egy fájlt.</span><span class="sxs-lookup"><span data-stu-id="a83f7-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="a83f7-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a83f7-111">EXAMPLES</span></span>

### <span data-ttu-id="a83f7-112">1. példa: Fájl törlése fájlmegosztásból</span><span class="sxs-lookup"><span data-stu-id="a83f7-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="a83f7-113">Ez a parancs törli a ContosoFile22 nevű fájlt a ContosoShare06 nevű fájlmegosztásból.</span><span class="sxs-lookup"><span data-stu-id="a83f7-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="a83f7-114">2. példa: Fájl behozása fájlmegosztásból fájlmegosztási objektum használatával</span><span class="sxs-lookup"><span data-stu-id="a83f7-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="a83f7-115">Ez a parancs **a Get-AzStorageShare** parancsmagot használva lekérte a ContosoShare06 nevű fájlmegosztást, majd a folyamat műveleti operátorával átadja az objektumot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="a83f7-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a83f7-116">Az aktuális parancs törli a ContosoFile22 nevű fájlt a ContosoShare06-ból.</span><span class="sxs-lookup"><span data-stu-id="a83f7-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="a83f7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a83f7-117">PARAMETERS</span></span>

### <span data-ttu-id="a83f7-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a83f7-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a83f7-119">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="a83f7-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a83f7-120">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="a83f7-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a83f7-121">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="a83f7-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a83f7-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a83f7-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a83f7-123">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="a83f7-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a83f7-124">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="a83f7-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a83f7-125">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="a83f7-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a83f7-126">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="a83f7-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a83f7-127">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="a83f7-127">The default value is 10.</span></span>

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

### <span data-ttu-id="a83f7-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a83f7-128">-Context</span></span>
<span data-ttu-id="a83f7-129">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a83f7-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a83f7-130">Tárterületkörnyezetet a [New-AzStorageContext](./New-AzStorageContext.md) parancsmag használatával szerezhet be.</span><span class="sxs-lookup"><span data-stu-id="a83f7-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="a83f7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a83f7-131">-DefaultProfile</span></span>
<span data-ttu-id="a83f7-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a83f7-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a83f7-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="a83f7-133">-Directory</span></span>
<span data-ttu-id="a83f7-134">Mappát ad meg **CloudFileDirectory objektumként.**</span><span class="sxs-lookup"><span data-stu-id="a83f7-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="a83f7-135">Ez a parancsmag eltávolít egy fájlt a paraméter által megadott mappából.</span><span class="sxs-lookup"><span data-stu-id="a83f7-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="a83f7-136">-File</span><span class="sxs-lookup"><span data-stu-id="a83f7-136">-File</span></span>
<span data-ttu-id="a83f7-137">Egy fájlt ad meg **CloudFile-objektumként.**</span><span class="sxs-lookup"><span data-stu-id="a83f7-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="a83f7-138">Ez a parancsmag eltávolítja a paraméter által megadott fájlt.</span><span class="sxs-lookup"><span data-stu-id="a83f7-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="a83f7-139">**CloudFile-objektum** beszerzéséhez használja a Get-AzStorageFile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a83f7-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a83f7-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a83f7-140">-PassThru</span></span>
<span data-ttu-id="a83f7-141">Azt jelzi, hogy ez a parancsmag egy **logikai** értéket ad vissza, amely tükrözi a művelet sikeres működését.</span><span class="sxs-lookup"><span data-stu-id="a83f7-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a83f7-142">Alapértelmezés szerint ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="a83f7-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a83f7-143">-Path</span><span class="sxs-lookup"><span data-stu-id="a83f7-143">-Path</span></span>
<span data-ttu-id="a83f7-144">A fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a83f7-144">Specifies the path of a file.</span></span>
<span data-ttu-id="a83f7-145">Ez a parancsmag törli a paraméter által megadott fájlt.</span><span class="sxs-lookup"><span data-stu-id="a83f7-145">This cmdlet deletes the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="a83f7-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a83f7-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a83f7-147">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a83f7-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a83f7-148">-Megosztás</span><span class="sxs-lookup"><span data-stu-id="a83f7-148">-Share</span></span>
<span data-ttu-id="a83f7-149">Egy **CloudFileShare-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="a83f7-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="a83f7-150">Ez a parancsmag eltávolítja a fájlt a paraméter által megadott megosztásból.</span><span class="sxs-lookup"><span data-stu-id="a83f7-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="a83f7-151">**CloudFileShare-objektum** beszerzéséhez használja a Get-AzStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a83f7-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="a83f7-152">Ez az objektum tartalmazza a tárterület környezetét.</span><span class="sxs-lookup"><span data-stu-id="a83f7-152">This object contains the storage context.</span></span>
<span data-ttu-id="a83f7-153">Ha ezt a paramétert adja meg, ne adja meg a környezet *paramétert.*</span><span class="sxs-lookup"><span data-stu-id="a83f7-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="a83f7-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a83f7-154">-ShareName</span></span>
<span data-ttu-id="a83f7-155">A fájlmegosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a83f7-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="a83f7-156">Ez a parancsmag eltávolítja a fájlt a paraméter által megadott megosztásból.</span><span class="sxs-lookup"><span data-stu-id="a83f7-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="a83f7-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a83f7-157">-Confirm</span></span>
<span data-ttu-id="a83f7-158">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a83f7-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a83f7-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a83f7-159">-WhatIf</span></span>
<span data-ttu-id="a83f7-160">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a83f7-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a83f7-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a83f7-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a83f7-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a83f7-162">CommonParameters</span></span>
<span data-ttu-id="a83f7-163">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a83f7-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a83f7-164">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a83f7-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a83f7-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a83f7-165">INPUTS</span></span>

### <span data-ttu-id="a83f7-166">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="a83f7-166">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="a83f7-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="a83f7-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="a83f7-168">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="a83f7-168">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="a83f7-169">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a83f7-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a83f7-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a83f7-170">OUTPUTS</span></span>

### <span data-ttu-id="a83f7-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="a83f7-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="a83f7-172">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a83f7-172">NOTES</span></span>

## <span data-ttu-id="a83f7-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a83f7-173">RELATED LINKS</span></span>

[<span data-ttu-id="a83f7-174">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="a83f7-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="a83f7-175">Get-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="a83f7-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="a83f7-176">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="a83f7-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
