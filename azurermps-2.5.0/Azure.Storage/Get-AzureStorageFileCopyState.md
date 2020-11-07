---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecopystate
schema: 2.0.0
ms.openlocfilehash: 61e633bc0890a8971b0be9d1b5950d990d32e8f4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849446"
---
# <span data-ttu-id="d36d2-101">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="d36d2-101">Get-AzureStorageFileCopyState</span></span>

## <span data-ttu-id="d36d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d36d2-102">SYNOPSIS</span></span>
<span data-ttu-id="d36d2-103">A másolási művelet állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d36d2-103">Gets the state of a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d36d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d36d2-104">SYNTAX</span></span>

### <span data-ttu-id="d36d2-105">Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="d36d2-105">ShareName</span></span>
```
Get-AzureStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d36d2-106">Fájl</span><span class="sxs-lookup"><span data-stu-id="d36d2-106">File</span></span>
```
Get-AzureStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="d36d2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d36d2-107">DESCRIPTION</span></span>
<span data-ttu-id="d36d2-108">A **Get-AzureStorageFileCopyState** parancsmag az Azure-tárterület fájlmásolási műveletének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d36d2-108">The **Get-AzureStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="d36d2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d36d2-109">EXAMPLES</span></span>

### <span data-ttu-id="d36d2-110">Példa 1: a másolati állapot beolvasása fájlnév szerint</span><span class="sxs-lookup"><span data-stu-id="d36d2-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzureStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="d36d2-111">Ez a parancs a megadott nevű fájl másolási műveletének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d36d2-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="d36d2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d36d2-112">PARAMETERS</span></span>

### <span data-ttu-id="d36d2-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d36d2-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d36d2-114">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="d36d2-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d36d2-115">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="d36d2-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d36d2-116">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="d36d2-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d36d2-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d36d2-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d36d2-118">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="d36d2-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d36d2-119">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="d36d2-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d36d2-120">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="d36d2-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d36d2-121">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="d36d2-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d36d2-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="d36d2-122">The default value is 10.</span></span>

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

### <span data-ttu-id="d36d2-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d36d2-123">-Context</span></span>
<span data-ttu-id="d36d2-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d36d2-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="d36d2-125">Környezet beolvasásához használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d36d2-125">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="d36d2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d36d2-126">-DefaultProfile</span></span>
<span data-ttu-id="d36d2-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d36d2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d36d2-128">-Fájl</span><span class="sxs-lookup"><span data-stu-id="d36d2-128">-File</span></span>
<span data-ttu-id="d36d2-129">Egy **CloudFile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d36d2-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="d36d2-130">Létrehozhat egy felhőalapú fájlt, vagy megadhat egyet az Get-AzureStorageFile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="d36d2-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="d36d2-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d36d2-131">-FilePath</span></span>
<span data-ttu-id="d36d2-132">A fájl elérési útját adja meg egy Azure-tárterülethez viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="d36d2-132">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="d36d2-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d36d2-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d36d2-134">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d36d2-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d36d2-135">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="d36d2-135">-ShareName</span></span>
<span data-ttu-id="d36d2-136">A megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d36d2-136">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="d36d2-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="d36d2-137">-WaitForComplete</span></span>
<span data-ttu-id="d36d2-138">Jelzi, hogy ez a parancsmag várja a másolat befejezését.</span><span class="sxs-lookup"><span data-stu-id="d36d2-138">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="d36d2-139">Ha nem adja meg ezt a paramétert, ez a parancsmag azonnal visszaadott eredményt ad.</span><span class="sxs-lookup"><span data-stu-id="d36d2-139">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="d36d2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d36d2-140">CommonParameters</span></span>
<span data-ttu-id="d36d2-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d36d2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d36d2-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d36d2-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d36d2-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d36d2-143">INPUTS</span></span>

### <span data-ttu-id="d36d2-144">Microsoft. WindowsAzure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="d36d2-144">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="d36d2-145">Paraméterek: fájl (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d36d2-145">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="d36d2-146">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d36d2-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d36d2-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d36d2-147">OUTPUTS</span></span>

### <span data-ttu-id="d36d2-148">Microsoft. WindowsAzure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="d36d2-148">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="d36d2-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d36d2-149">NOTES</span></span>

## <span data-ttu-id="d36d2-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d36d2-150">RELATED LINKS</span></span>

[<span data-ttu-id="d36d2-151">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="d36d2-151">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="d36d2-152">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d36d2-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="d36d2-153">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d36d2-153">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)

[<span data-ttu-id="d36d2-154">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d36d2-154">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
