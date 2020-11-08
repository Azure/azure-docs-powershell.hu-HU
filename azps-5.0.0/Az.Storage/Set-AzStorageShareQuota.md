---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: d029a00a2ddba5974fb473e58b933820e2e14757
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185755"
---
# <span data-ttu-id="64b02-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="64b02-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="64b02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64b02-102">SYNOPSIS</span></span>
<span data-ttu-id="64b02-103">A megosztás tárterület-kapacitását adja meg.</span><span class="sxs-lookup"><span data-stu-id="64b02-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="64b02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64b02-104">SYNTAX</span></span>

### <span data-ttu-id="64b02-105">Megosztásnév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="64b02-105">ShareName (Default)</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="64b02-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="64b02-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="64b02-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="64b02-107">DESCRIPTION</span></span>
<span data-ttu-id="64b02-108">A **set-AzStorageShareQuota** parancsmag a megadott megosztás tárolási kapacitását adja meg.</span><span class="sxs-lookup"><span data-stu-id="64b02-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="64b02-109">Példák</span><span class="sxs-lookup"><span data-stu-id="64b02-109">EXAMPLES</span></span>

### <span data-ttu-id="64b02-110">1. példa: egy megosztás tárterület-kapacitásának beállítása</span><span class="sxs-lookup"><span data-stu-id="64b02-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="64b02-111">Ez a parancs beállítja a ContosoShare01 nevű megosztás 1024 GB-ra való tárolási kapacitását.</span><span class="sxs-lookup"><span data-stu-id="64b02-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="64b02-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64b02-112">PARAMETERS</span></span>

### <span data-ttu-id="64b02-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="64b02-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="64b02-114">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="64b02-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="64b02-115">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="64b02-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="64b02-116">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="64b02-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="64b02-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="64b02-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="64b02-118">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="64b02-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="64b02-119">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="64b02-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="64b02-120">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="64b02-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="64b02-121">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="64b02-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="64b02-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="64b02-122">The default value is 10.</span></span>

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

### <span data-ttu-id="64b02-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="64b02-123">-Context</span></span>
<span data-ttu-id="64b02-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64b02-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="64b02-125">A tárolási környezet eléréséhez használja a [New-AzStorageContext](./New-AzStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="64b02-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="64b02-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b02-126">-DefaultProfile</span></span>
<span data-ttu-id="64b02-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64b02-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64b02-128">-Kvóta</span><span class="sxs-lookup"><span data-stu-id="64b02-128">-Quota</span></span>
<span data-ttu-id="64b02-129">A kvóta értékét gigabájtban (GB) adja meg.</span><span class="sxs-lookup"><span data-stu-id="64b02-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="64b02-130">Tekintse meg a kvóta korlátozását https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="64b02-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: QuotaGiB

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b02-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="64b02-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="64b02-132">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="64b02-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="64b02-133">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="64b02-133">-Share</span></span>
<span data-ttu-id="64b02-134">Itt adhatja meg azt a **CloudFileShare** -objektumot, amely azt a megosztást jelképezi, amelyhez a parancsmagok kvótát állítanak be.</span><span class="sxs-lookup"><span data-stu-id="64b02-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="64b02-135">**CloudFileShare** objektum beolvasásához használja az Get-AzStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="64b02-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="64b02-136">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="64b02-136">-ShareName</span></span>
<span data-ttu-id="64b02-137">Annak a fájlnak a nevét adja meg, amelyhez kvótát szeretne beállítani.</span><span class="sxs-lookup"><span data-stu-id="64b02-137">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64b02-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b02-138">CommonParameters</span></span>
<span data-ttu-id="64b02-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64b02-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b02-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64b02-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b02-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64b02-141">INPUTS</span></span>

### <span data-ttu-id="64b02-142">System. String</span><span class="sxs-lookup"><span data-stu-id="64b02-142">System.String</span></span>

### <span data-ttu-id="64b02-143">Microsoft. Azure. Storage. file. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="64b02-143">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="64b02-144">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="64b02-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="64b02-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64b02-145">OUTPUTS</span></span>

### <span data-ttu-id="64b02-146">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="64b02-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="64b02-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64b02-147">NOTES</span></span>

## <span data-ttu-id="64b02-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64b02-148">RELATED LINKS</span></span>

[<span data-ttu-id="64b02-149">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="64b02-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="64b02-150">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="64b02-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="64b02-151">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="64b02-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)