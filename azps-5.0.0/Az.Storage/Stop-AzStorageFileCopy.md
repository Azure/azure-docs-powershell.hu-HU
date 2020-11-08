---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
ms.openlocfilehash: ac36914167bd5bda2e79576d9879d6f8c92ba7fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186005"
---
# <span data-ttu-id="83ed4-101">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="83ed4-101">Stop-AzStorageFileCopy</span></span>

## <span data-ttu-id="83ed4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="83ed4-103">Leállít egy másolási műveletet a megadott célfájlba.</span><span class="sxs-lookup"><span data-stu-id="83ed4-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="83ed4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83ed4-104">SYNTAX</span></span>

### <span data-ttu-id="83ed4-105">Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="83ed4-105">ShareName</span></span>
```
Stop-AzStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83ed4-106">Fájl</span><span class="sxs-lookup"><span data-stu-id="83ed4-106">File</span></span>
```
Stop-AzStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83ed4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="83ed4-107">DESCRIPTION</span></span>
<span data-ttu-id="83ed4-108">A **stop-AzStorageFileCopy** parancsmag leállítja a fájlok másolását a célfájlba.</span><span class="sxs-lookup"><span data-stu-id="83ed4-108">The **Stop-AzStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="83ed4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="83ed4-109">EXAMPLES</span></span>

### <span data-ttu-id="83ed4-110">Példa 1: a másolási művelet leállítása</span><span class="sxs-lookup"><span data-stu-id="83ed4-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="83ed4-111">Ez a parancs leállítja a megadott nevű fájl másolását.</span><span class="sxs-lookup"><span data-stu-id="83ed4-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="83ed4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83ed4-112">PARAMETERS</span></span>

### <span data-ttu-id="83ed4-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="83ed4-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="83ed4-114">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="83ed4-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="83ed4-115">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="83ed4-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="83ed4-116">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="83ed4-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="83ed4-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="83ed4-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="83ed4-118">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="83ed4-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="83ed4-119">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="83ed4-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="83ed4-120">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="83ed4-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="83ed4-121">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="83ed4-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="83ed4-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="83ed4-122">The default value is 10.</span></span>

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

### <span data-ttu-id="83ed4-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="83ed4-123">-Context</span></span>
<span data-ttu-id="83ed4-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="83ed4-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="83ed4-125">A tárolási környezet eléréséhez használja a [New-AzStorageContext](./New-AzStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="83ed4-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="83ed4-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="83ed4-126">-CopyId</span></span>
<span data-ttu-id="83ed4-127">A másolási művelet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="83ed4-127">Specifies the ID of the copy operation.</span></span>

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

### <span data-ttu-id="83ed4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83ed4-128">-DefaultProfile</span></span>
<span data-ttu-id="83ed4-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83ed4-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83ed4-130">-Fájl</span><span class="sxs-lookup"><span data-stu-id="83ed4-130">-File</span></span>
<span data-ttu-id="83ed4-131">Egy **CloudFile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="83ed4-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="83ed4-132">Létrehozhat egy felhőalapú fájlt, vagy megadhat egyet az Get-AzStorageFile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="83ed4-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="83ed4-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="83ed4-133">-FilePath</span></span>
<span data-ttu-id="83ed4-134">A fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="83ed4-134">Specifies the path of a file.</span></span>

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

### <span data-ttu-id="83ed4-135">-Force</span><span class="sxs-lookup"><span data-stu-id="83ed4-135">-Force</span></span>
<span data-ttu-id="83ed4-136">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="83ed4-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="83ed4-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="83ed4-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="83ed4-138">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="83ed4-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="83ed4-139">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="83ed4-139">-ShareName</span></span>
<span data-ttu-id="83ed4-140">A megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="83ed4-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="83ed4-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83ed4-141">-Confirm</span></span>
<span data-ttu-id="83ed4-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83ed4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83ed4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83ed4-143">-WhatIf</span></span>
<span data-ttu-id="83ed4-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83ed4-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83ed4-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83ed4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83ed4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ed4-146">CommonParameters</span></span>
<span data-ttu-id="83ed4-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83ed4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ed4-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83ed4-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ed4-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83ed4-149">INPUTS</span></span>

### <span data-ttu-id="83ed4-150">Microsoft. Azure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="83ed4-150">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="83ed4-151">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="83ed4-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="83ed4-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83ed4-152">OUTPUTS</span></span>

### <span data-ttu-id="83ed4-153">System. Void</span><span class="sxs-lookup"><span data-stu-id="83ed4-153">System.Void</span></span>

## <span data-ttu-id="83ed4-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83ed4-154">NOTES</span></span>

## <span data-ttu-id="83ed4-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83ed4-155">RELATED LINKS</span></span>

[<span data-ttu-id="83ed4-156">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="83ed4-156">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="83ed4-157">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="83ed4-157">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="83ed4-158">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="83ed4-158">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="83ed4-159">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="83ed4-159">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)
