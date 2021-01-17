---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: 3ac8cb302c65fd42fdd699588b71bc1b081cc9d2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466912"
---
# <span data-ttu-id="1d709-101">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="1d709-101">Remove-AzStorageDirectory</span></span>

## <span data-ttu-id="1d709-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d709-102">SYNOPSIS</span></span>
<span data-ttu-id="1d709-103">Címtár törlése.</span><span class="sxs-lookup"><span data-stu-id="1d709-103">Deletes a directory.</span></span>

## <span data-ttu-id="1d709-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d709-104">SYNTAX</span></span>

### <span data-ttu-id="1d709-105">ShareName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1d709-105">ShareName (Default)</span></span>
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d709-106">Megosztás</span><span class="sxs-lookup"><span data-stu-id="1d709-106">Share</span></span>
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d709-107">Címtár</span><span class="sxs-lookup"><span data-stu-id="1d709-107">Directory</span></span>
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d709-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d709-108">DESCRIPTION</span></span>
<span data-ttu-id="1d709-109">A **Remove-AzStorageDirectory** parancsmag töröl egy címtárat.</span><span class="sxs-lookup"><span data-stu-id="1d709-109">The **Remove-AzStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="1d709-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d709-110">EXAMPLES</span></span>

### <span data-ttu-id="1d709-111">1. példa: Mappa törlése</span><span class="sxs-lookup"><span data-stu-id="1d709-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="1d709-112">Ez a parancs törli a ContosoWorkingFolder nevű mappát a ContosoShare06 nevű fájlmegosztásból.</span><span class="sxs-lookup"><span data-stu-id="1d709-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="1d709-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d709-113">PARAMETERS</span></span>

### <span data-ttu-id="1d709-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1d709-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1d709-115">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="1d709-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1d709-116">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="1d709-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1d709-117">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="1d709-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1d709-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1d709-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1d709-119">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="1d709-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1d709-120">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="1d709-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1d709-121">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="1d709-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1d709-122">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="1d709-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1d709-123">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="1d709-123">The default value is 10.</span></span>

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

### <span data-ttu-id="1d709-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1d709-124">-Context</span></span>
<span data-ttu-id="1d709-125">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d709-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1d709-126">Tárterületkörnyezetet a [New-AzStorageContext](./New-AzStorageContext.md) parancsmag használatával szerezhet be.</span><span class="sxs-lookup"><span data-stu-id="1d709-126">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="1d709-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d709-127">-DefaultProfile</span></span>
<span data-ttu-id="1d709-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d709-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d709-129">-Directory</span><span class="sxs-lookup"><span data-stu-id="1d709-129">-Directory</span></span>
<span data-ttu-id="1d709-130">Mappát ad meg **CloudFileDirectory objektumként.**</span><span class="sxs-lookup"><span data-stu-id="1d709-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="1d709-131">Ez a parancsmag eltávolítja a paraméter által megadott mappát.</span><span class="sxs-lookup"><span data-stu-id="1d709-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="1d709-132">Címtár beszerzéséhez használja a New-AzStorageDirectory parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1d709-132">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="1d709-133">Könyvtár beszerzéséhez használhatja a **Get-AzStorageFile** parancsmagot is.</span><span class="sxs-lookup"><span data-stu-id="1d709-133">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="1d709-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d709-134">-PassThru</span></span>
<span data-ttu-id="1d709-135">Azt jelzi, hogy ha a parancsmag sikerrel jár, a visszaadott érték $True.</span><span class="sxs-lookup"><span data-stu-id="1d709-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="1d709-136">Ha ezt a paramétert adja meg, és a parancsmag nem jár sikerrel, mert nem megfelelő az _Elérési_ út paraméter értéke, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="1d709-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="1d709-137">Ha nem adja meg ezt a paramétert, ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="1d709-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1d709-138">-Path</span><span class="sxs-lookup"><span data-stu-id="1d709-138">-Path</span></span>
<span data-ttu-id="1d709-139">A mappa elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d709-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="1d709-140">Ha a paraméterrel megadott mappa üres, ez a parancsmag törli a mappát.</span><span class="sxs-lookup"><span data-stu-id="1d709-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="1d709-141">Ha a mappa nem üres, ez a parancsmag nem módosítja, és hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="1d709-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d709-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1d709-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1d709-143">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d709-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="1d709-144">-Megosztás</span><span class="sxs-lookup"><span data-stu-id="1d709-144">-Share</span></span>
<span data-ttu-id="1d709-145">Egy **CloudFileShare-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="1d709-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="1d709-146">Ez a parancsmag eltávolít egy mappát a paraméter által megadott fájlmegosztás alatt.</span><span class="sxs-lookup"><span data-stu-id="1d709-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="1d709-147">**CloudFileShare-objektum** beszerzéséhez használja a Get-AzStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1d709-147">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="1d709-148">Ez az objektum tartalmazza a tárterület környezetét.</span><span class="sxs-lookup"><span data-stu-id="1d709-148">This object contains the storage context.</span></span>
<span data-ttu-id="1d709-149">Ha ezt a paramétert adja meg, ne adja meg a környezet *paramétert.*</span><span class="sxs-lookup"><span data-stu-id="1d709-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="1d709-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1d709-150">-ShareName</span></span>
<span data-ttu-id="1d709-151">A fájlmegosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d709-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="1d709-152">Ez a parancsmag eltávolít egy mappát a paraméter által megadott fájlmegosztás alatt.</span><span class="sxs-lookup"><span data-stu-id="1d709-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d709-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d709-153">-Confirm</span></span>
<span data-ttu-id="1d709-154">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1d709-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d709-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d709-155">-WhatIf</span></span>
<span data-ttu-id="1d709-156">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1d709-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d709-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d709-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d709-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d709-158">CommonParameters</span></span>
<span data-ttu-id="1d709-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d709-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d709-160">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d709-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d709-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d709-161">INPUTS</span></span>

### <span data-ttu-id="1d709-162">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="1d709-162">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="1d709-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="1d709-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="1d709-164">System.String</span><span class="sxs-lookup"><span data-stu-id="1d709-164">System.String</span></span>

### <span data-ttu-id="1d709-165">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1d709-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1d709-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d709-166">OUTPUTS</span></span>

### <span data-ttu-id="1d709-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="1d709-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="1d709-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d709-168">NOTES</span></span>

## <span data-ttu-id="1d709-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d709-169">RELATED LINKS</span></span>

[<span data-ttu-id="1d709-170">Get-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="1d709-170">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="1d709-171">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="1d709-171">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="1d709-172">New-AzstorageDirectory</span><span class="sxs-lookup"><span data-stu-id="1d709-172">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)
