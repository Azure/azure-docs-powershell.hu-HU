---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: cff5f387b6729f51634ee0466b099e1df8314589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502819"
---
# <span data-ttu-id="69ee5-101">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="69ee5-101">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="69ee5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="69ee5-103">ImmutabilityPolicy kapja a tároló blob-tárolókban</span><span class="sxs-lookup"><span data-stu-id="69ee5-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69ee5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69ee5-104">SYNTAX</span></span>

### <span data-ttu-id="69ee5-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69ee5-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69ee5-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="69ee5-106">AccountObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69ee5-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="69ee5-107">ContainerObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69ee5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="69ee5-108">DESCRIPTION</span></span>
<span data-ttu-id="69ee5-109">A **Get-AzureRmStorageContainerImmutabilityPolicy** parancsmag ImmutabilityPolicy tároló blob-tárolókat kap</span><span class="sxs-lookup"><span data-stu-id="69ee5-109">The **Get-AzureRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="69ee5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="69ee5-110">EXAMPLES</span></span>

### <span data-ttu-id="69ee5-111">Példa 1: ImmutabilityPolicy-tároló blob-tárolójának beszerzése a tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="69ee5-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="69ee5-112">Ez a parancs a ImmutabilityPolicy-tároló blob-tárolóját a tárolási fióknév és a tároló neve segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="69ee5-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="69ee5-113">2. példa: ImmutabilityPolicy-tároló blob-tárolójának beszerzése a tárolási fiók objektummal és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="69ee5-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="69ee5-114">Ez a parancs a ImmutabilityPolicy és a tároló nevét tároló blob-tárolók esetén válik.</span><span class="sxs-lookup"><span data-stu-id="69ee5-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="69ee5-115">3. példa: ImmutabilityPolicy beszerzése tároló blob-tárolóról a Storage Container objektummal</span><span class="sxs-lookup"><span data-stu-id="69ee5-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject 
```

<span data-ttu-id="69ee5-116">Ez a parancs tárterület-tároló objektummal ImmutabilityPolicy válik.</span><span class="sxs-lookup"><span data-stu-id="69ee5-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="69ee5-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69ee5-117">PARAMETERS</span></span>

### <span data-ttu-id="69ee5-118">-Container</span><span class="sxs-lookup"><span data-stu-id="69ee5-118">-Container</span></span>
<span data-ttu-id="69ee5-119">Tároló tároló objektum</span><span class="sxs-lookup"><span data-stu-id="69ee5-119">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="69ee5-120">-ContainerName</span></span>
<span data-ttu-id="69ee5-121">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="69ee5-121">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ee5-122">-DefaultProfile</span></span>
<span data-ttu-id="69ee5-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69ee5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-124">-ETAG</span><span class="sxs-lookup"><span data-stu-id="69ee5-124">-Etag</span></span>
<span data-ttu-id="69ee5-125">A Immutability házirend ETAG.</span><span class="sxs-lookup"><span data-stu-id="69ee5-125">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ee5-126">-ResourceGroupName</span></span>
<span data-ttu-id="69ee5-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="69ee5-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="69ee5-128">-StorageAccount</span></span>
<span data-ttu-id="69ee5-129">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="69ee5-129">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="69ee5-130">-StorageAccountName</span></span>
<span data-ttu-id="69ee5-131">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="69ee5-131">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ee5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ee5-132">CommonParameters</span></span>
<span data-ttu-id="69ee5-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69ee5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ee5-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69ee5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ee5-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69ee5-135">INPUTS</span></span>

### <span data-ttu-id="69ee5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="69ee5-136">System.String</span></span>

## <span data-ttu-id="69ee5-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69ee5-137">OUTPUTS</span></span>

### <span data-ttu-id="69ee5-138">Microsoft. Azure. Command. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="69ee5-138">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="69ee5-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69ee5-139">NOTES</span></span>

## <span data-ttu-id="69ee5-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69ee5-140">RELATED LINKS</span></span>

