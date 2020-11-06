---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileCopyState.md
ms.openlocfilehash: 811e642bf92e12c0d385ff38d93297c3a7c060ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495208"
---
# <span data-ttu-id="e679f-101">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="e679f-101">Get-AzureStorageFileCopyState</span></span>

## <span data-ttu-id="e679f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e679f-102">SYNOPSIS</span></span>
<span data-ttu-id="e679f-103">A másolási művelet állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e679f-103">Gets the state of a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e679f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e679f-104">SYNTAX</span></span>

### <span data-ttu-id="e679f-105">Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="e679f-105">ShareName</span></span>
```
Get-AzureStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e679f-106">Fájl</span><span class="sxs-lookup"><span data-stu-id="e679f-106">File</span></span>
```
Get-AzureStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="e679f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e679f-107">DESCRIPTION</span></span>
<span data-ttu-id="e679f-108">A **Get-AzureStorageFileCopyState** parancsmag az Azure-tárterület fájlmásolási műveletének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e679f-108">The **Get-AzureStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="e679f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e679f-109">EXAMPLES</span></span>

### <span data-ttu-id="e679f-110">Példa 1: a másolati állapot beolvasása fájlnév szerint</span><span class="sxs-lookup"><span data-stu-id="e679f-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzureStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="e679f-111">Ez a parancs a megadott nevű fájl másolási műveletének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e679f-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="e679f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e679f-112">PARAMETERS</span></span>

### <span data-ttu-id="e679f-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e679f-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e679f-114">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="e679f-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e679f-115">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="e679f-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e679f-116">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="e679f-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e679f-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e679f-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e679f-118">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="e679f-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e679f-119">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="e679f-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e679f-120">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="e679f-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e679f-121">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="e679f-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e679f-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="e679f-122">The default value is 10.</span></span>

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

### <span data-ttu-id="e679f-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e679f-123">-Context</span></span>
<span data-ttu-id="e679f-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e679f-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e679f-125">Környezet beolvasásához használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e679f-125">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="e679f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e679f-126">-DefaultProfile</span></span>
<span data-ttu-id="e679f-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e679f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e679f-128">-Fájl</span><span class="sxs-lookup"><span data-stu-id="e679f-128">-File</span></span>
<span data-ttu-id="e679f-129">Egy **CloudFile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e679f-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="e679f-130">Létrehozhat egy felhőalapú fájlt, vagy megadhat egyet az Get-AzureStorageFile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="e679f-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="e679f-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e679f-131">-FilePath</span></span>
<span data-ttu-id="e679f-132">A fájl elérési útját adja meg egy Azure-tárterülethez viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="e679f-132">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="e679f-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e679f-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e679f-134">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e679f-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e679f-135">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="e679f-135">-ShareName</span></span>
<span data-ttu-id="e679f-136">A megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e679f-136">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="e679f-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="e679f-137">-WaitForComplete</span></span>
<span data-ttu-id="e679f-138">Jelzi, hogy ez a parancsmag várja a másolat befejezését.</span><span class="sxs-lookup"><span data-stu-id="e679f-138">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="e679f-139">Ha nem adja meg ezt a paramétert, ez a parancsmag azonnal visszaadott eredményt ad.</span><span class="sxs-lookup"><span data-stu-id="e679f-139">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="e679f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e679f-140">CommonParameters</span></span>
<span data-ttu-id="e679f-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e679f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e679f-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e679f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e679f-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e679f-143">INPUTS</span></span>

### <span data-ttu-id="e679f-144">Microsoft. WindowsAzure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="e679f-144">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="e679f-145">Paraméterek: fájl (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e679f-145">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="e679f-146">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e679f-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e679f-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e679f-147">OUTPUTS</span></span>

### <span data-ttu-id="e679f-148">Microsoft. WindowsAzure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="e679f-148">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="e679f-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e679f-149">NOTES</span></span>

## <span data-ttu-id="e679f-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e679f-150">RELATED LINKS</span></span>

[<span data-ttu-id="e679f-151">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="e679f-151">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="e679f-152">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e679f-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e679f-153">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e679f-153">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)

[<span data-ttu-id="e679f-154">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e679f-154">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
