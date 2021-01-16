---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
ms.openlocfilehash: ac36914167bd5bda2e79576d9879d6f8c92ba7fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376009"
---
# <span data-ttu-id="07472-101">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="07472-101">Stop-AzStorageFileCopy</span></span>

## <span data-ttu-id="07472-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07472-102">SYNOPSIS</span></span>
<span data-ttu-id="07472-103">A másolási művelet leállítja a megadott célfájlba való másolást.</span><span class="sxs-lookup"><span data-stu-id="07472-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="07472-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="07472-104">SYNTAX</span></span>

### <span data-ttu-id="07472-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="07472-105">ShareName</span></span>
```
Stop-AzStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07472-106">Fájl</span><span class="sxs-lookup"><span data-stu-id="07472-106">File</span></span>
```
Stop-AzStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07472-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="07472-107">DESCRIPTION</span></span>
<span data-ttu-id="07472-108">A **Stop-AzStorageFileCopy** parancsmag leállítja a fájlok célfájlba való másolását.</span><span class="sxs-lookup"><span data-stu-id="07472-108">The **Stop-AzStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="07472-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="07472-109">EXAMPLES</span></span>

### <span data-ttu-id="07472-110">1. példa: Másolási művelet leállítása</span><span class="sxs-lookup"><span data-stu-id="07472-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="07472-111">Ez a parancs leállítja a megadott nevű fájl másolását.</span><span class="sxs-lookup"><span data-stu-id="07472-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="07472-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07472-112">PARAMETERS</span></span>

### <span data-ttu-id="07472-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="07472-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="07472-114">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="07472-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="07472-115">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="07472-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="07472-116">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="07472-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="07472-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="07472-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="07472-118">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="07472-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="07472-119">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="07472-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="07472-120">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="07472-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="07472-121">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="07472-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="07472-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="07472-122">The default value is 10.</span></span>

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

### <span data-ttu-id="07472-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="07472-123">-Context</span></span>
<span data-ttu-id="07472-124">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07472-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="07472-125">Tárterületkörnyezetet a [New-AzStorageContext](./New-AzStorageContext.md) parancsmag használatával szerezhet be.</span><span class="sxs-lookup"><span data-stu-id="07472-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="07472-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="07472-126">-CopyId</span></span>
<span data-ttu-id="07472-127">A másolási művelet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="07472-127">Specifies the ID of the copy operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07472-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07472-128">-DefaultProfile</span></span>
<span data-ttu-id="07472-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07472-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07472-130">-File</span><span class="sxs-lookup"><span data-stu-id="07472-130">-File</span></span>
<span data-ttu-id="07472-131">Egy **CloudFile-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="07472-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="07472-132">Létrehozhat felhőfájlt, vagy beszerezhet egyet a Get-AzStorageFile parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="07472-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="07472-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="07472-133">-FilePath</span></span>
<span data-ttu-id="07472-134">A fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="07472-134">Specifies the path of a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07472-135">-Force</span><span class="sxs-lookup"><span data-stu-id="07472-135">-Force</span></span>
<span data-ttu-id="07472-136">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="07472-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="07472-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="07472-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="07472-138">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="07472-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="07472-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="07472-139">-ShareName</span></span>
<span data-ttu-id="07472-140">Egy megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07472-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="07472-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07472-141">-Confirm</span></span>
<span data-ttu-id="07472-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="07472-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07472-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07472-143">-WhatIf</span></span>
<span data-ttu-id="07472-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="07472-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07472-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07472-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07472-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07472-146">CommonParameters</span></span>
<span data-ttu-id="07472-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07472-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07472-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07472-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07472-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07472-149">INPUTS</span></span>

### <span data-ttu-id="07472-150">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="07472-150">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="07472-151">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="07472-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="07472-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07472-152">OUTPUTS</span></span>

### <span data-ttu-id="07472-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="07472-153">System.Void</span></span>

## <span data-ttu-id="07472-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="07472-154">NOTES</span></span>

## <span data-ttu-id="07472-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07472-155">RELATED LINKS</span></span>

[<span data-ttu-id="07472-156">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="07472-156">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="07472-157">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="07472-157">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="07472-158">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="07472-158">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="07472-159">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="07472-159">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)
