---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: d029a00a2ddba5974fb473e58b933820e2e14757
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376094"
---
# <span data-ttu-id="b701c-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="b701c-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="b701c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b701c-102">SYNOPSIS</span></span>
<span data-ttu-id="b701c-103">Beállítja egy megosztás tárterület-kapacitását.</span><span class="sxs-lookup"><span data-stu-id="b701c-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="b701c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b701c-104">SYNTAX</span></span>

### <span data-ttu-id="b701c-105">ShareName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b701c-105">ShareName (Default)</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b701c-106">Megosztás</span><span class="sxs-lookup"><span data-stu-id="b701c-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="b701c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b701c-107">DESCRIPTION</span></span>
<span data-ttu-id="b701c-108">A **Set-AzStorageShareQuota** parancsmag beállítja egy adott megosztás tárterületkapacitását.</span><span class="sxs-lookup"><span data-stu-id="b701c-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="b701c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b701c-109">EXAMPLES</span></span>

### <span data-ttu-id="b701c-110">1. példa: Megosztás tárolási kapacitásának beállítása</span><span class="sxs-lookup"><span data-stu-id="b701c-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="b701c-111">Ez a parancs a ContosoShare01 nevű megosztás tárterületkapacitását 1024 GB-ra állítja.</span><span class="sxs-lookup"><span data-stu-id="b701c-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="b701c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b701c-112">PARAMETERS</span></span>

### <span data-ttu-id="b701c-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b701c-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b701c-114">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="b701c-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b701c-115">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="b701c-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b701c-116">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="b701c-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b701c-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b701c-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b701c-118">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="b701c-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b701c-119">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="b701c-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b701c-120">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="b701c-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b701c-121">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="b701c-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b701c-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="b701c-122">The default value is 10.</span></span>

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

### <span data-ttu-id="b701c-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b701c-123">-Context</span></span>
<span data-ttu-id="b701c-124">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b701c-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b701c-125">Tárterületkörnyezetet a [New-AzStorageContext](./New-AzStorageContext.md) parancsmag használatával szerezhet be.</span><span class="sxs-lookup"><span data-stu-id="b701c-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b701c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b701c-126">-DefaultProfile</span></span>
<span data-ttu-id="b701c-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b701c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b701c-128">-Quota</span><span class="sxs-lookup"><span data-stu-id="b701c-128">-Quota</span></span>
<span data-ttu-id="b701c-129">A gigabájtban (GB) megadott kvótaértéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="b701c-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="b701c-130">Tekintse meg a kvótakorlátot. https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits</span><span class="sxs-lookup"><span data-stu-id="b701c-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

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

### <span data-ttu-id="b701c-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b701c-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b701c-132">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b701c-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b701c-133">-Megosztás</span><span class="sxs-lookup"><span data-stu-id="b701c-133">-Share</span></span>
<span data-ttu-id="b701c-134">Egy **CloudFileShare-objektumot** ad meg, amely azt a megosztást jelzi, amelyhez a parancsmagok kvótát állít be.</span><span class="sxs-lookup"><span data-stu-id="b701c-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="b701c-135">**CloudFileShare-objektum** beszerzéséhez használja a Get-AzStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b701c-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="b701c-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b701c-136">-ShareName</span></span>
<span data-ttu-id="b701c-137">Annak a fájlmegosztásnak a nevét adja meg, amelyhez kvótát kell beállítani.</span><span class="sxs-lookup"><span data-stu-id="b701c-137">Specifies the name of the file share for which to set a quota.</span></span>

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

### <span data-ttu-id="b701c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b701c-138">CommonParameters</span></span>
<span data-ttu-id="b701c-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b701c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b701c-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b701c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b701c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b701c-141">INPUTS</span></span>

### <span data-ttu-id="b701c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b701c-142">System.String</span></span>

### <span data-ttu-id="b701c-143">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="b701c-143">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="b701c-144">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b701c-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b701c-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b701c-145">OUTPUTS</span></span>

### <span data-ttu-id="b701c-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="b701c-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="b701c-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b701c-147">NOTES</span></span>

## <span data-ttu-id="b701c-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b701c-148">RELATED LINKS</span></span>

[<span data-ttu-id="b701c-149">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b701c-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="b701c-150">Get-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="b701c-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="b701c-151">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="b701c-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
