---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012301"
---
# <span data-ttu-id="32eae-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="32eae-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="32eae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32eae-102">SYNOPSIS</span></span>
<span data-ttu-id="32eae-103">ImmutabilityPolicy kapja a tároló blob-tárolókban</span><span class="sxs-lookup"><span data-stu-id="32eae-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="32eae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32eae-104">SYNTAX</span></span>

### <span data-ttu-id="32eae-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="32eae-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32eae-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="32eae-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32eae-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="32eae-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32eae-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="32eae-108">DESCRIPTION</span></span>
<span data-ttu-id="32eae-109">A **Get-AzRmStorageContainerImmutabilityPolicy** parancsmag ImmutabilityPolicy tároló blob-tárolókat kap</span><span class="sxs-lookup"><span data-stu-id="32eae-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="32eae-110">Példák</span><span class="sxs-lookup"><span data-stu-id="32eae-110">EXAMPLES</span></span>

### <span data-ttu-id="32eae-111">Példa 1: ImmutabilityPolicy-tároló blob-tárolójának beszerzése a tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="32eae-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="32eae-112">Ez a parancs a ImmutabilityPolicy-tároló blob-tárolóját a tárolási fióknév és a tároló neve segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="32eae-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="32eae-113">2. példa: ImmutabilityPolicy-tároló blob-tárolójának beszerzése a tárolási fiók objektummal és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="32eae-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="32eae-114">Ez a parancs a ImmutabilityPolicy és a tároló nevét tároló blob-tárolók esetén válik.</span><span class="sxs-lookup"><span data-stu-id="32eae-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="32eae-115">3. példa: ImmutabilityPolicy beszerzése tároló blob-tárolóról a Storage Container objektummal</span><span class="sxs-lookup"><span data-stu-id="32eae-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="32eae-116">Ez a parancs tárterület-tároló objektummal ImmutabilityPolicy válik.</span><span class="sxs-lookup"><span data-stu-id="32eae-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="32eae-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32eae-117">PARAMETERS</span></span>

### <span data-ttu-id="32eae-118">-Container</span><span class="sxs-lookup"><span data-stu-id="32eae-118">-Container</span></span>
<span data-ttu-id="32eae-119">Tároló tároló objektum</span><span class="sxs-lookup"><span data-stu-id="32eae-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32eae-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="32eae-120">-ContainerName</span></span>
<span data-ttu-id="32eae-121">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="32eae-121">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32eae-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32eae-122">-DefaultProfile</span></span>
<span data-ttu-id="32eae-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32eae-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32eae-124">-ETAG</span><span class="sxs-lookup"><span data-stu-id="32eae-124">-Etag</span></span>
<span data-ttu-id="32eae-125">A Immutability házirend ETAG.</span><span class="sxs-lookup"><span data-stu-id="32eae-125">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32eae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32eae-126">-ResourceGroupName</span></span>
<span data-ttu-id="32eae-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="32eae-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32eae-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="32eae-128">-StorageAccount</span></span>
<span data-ttu-id="32eae-129">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="32eae-129">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32eae-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="32eae-130">-StorageAccountName</span></span>
<span data-ttu-id="32eae-131">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="32eae-131">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32eae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32eae-132">CommonParameters</span></span>
<span data-ttu-id="32eae-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32eae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32eae-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32eae-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32eae-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32eae-135">INPUTS</span></span>

### <span data-ttu-id="32eae-136">System. String</span><span class="sxs-lookup"><span data-stu-id="32eae-136">System.String</span></span>

### <span data-ttu-id="32eae-137">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="32eae-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="32eae-138">Microsoft. Azure. Command. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="32eae-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="32eae-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32eae-139">OUTPUTS</span></span>

### <span data-ttu-id="32eae-140">Microsoft. Azure. Command. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="32eae-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="32eae-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32eae-141">NOTES</span></span>

## <span data-ttu-id="32eae-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32eae-142">RELATED LINKS</span></span>
