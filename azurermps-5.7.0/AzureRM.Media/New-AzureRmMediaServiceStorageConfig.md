---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/new-azurermmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
ms.openlocfilehash: 7296d744749dd037c10d0d4d5ee2b0461a55b794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673040"
---
# <span data-ttu-id="fb9df-101">New-AzureRmMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="fb9df-101">New-AzureRmMediaServiceStorageConfig</span></span>

## <span data-ttu-id="fb9df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb9df-102">SYNOPSIS</span></span>
<span data-ttu-id="fb9df-103">A Media Service-parancsmagok tárterület-konfigurációjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="fb9df-103">Create a storage account configuration for the media service cmdlets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb9df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb9df-104">SYNTAX</span></span>

```
New-AzureRmMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb9df-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb9df-105">DESCRIPTION</span></span>
<span data-ttu-id="fb9df-106">A **New-AzureRmMediaServiceStorageConfig** parancsmag a Media Service-parancsmagok tárolási fiókjának konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="fb9df-106">The **New-AzureRmMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="fb9df-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fb9df-107">EXAMPLES</span></span>

### <span data-ttu-id="fb9df-108">Példa 1: a Media Service-parancsmagok tároló-konfigurációjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="fb9df-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="fb9df-109">Az első parancs **a New-AzureRmStorageAccount** parancsmaggal hozza létre a Storage Account objektum objektumát.</span><span class="sxs-lookup"><span data-stu-id="fb9df-109">The first command creates a storage account object by using **the New-AzureRmStorageAccount** cmdlet.</span></span>
<span data-ttu-id="fb9df-110">A parancs a tárolási fiók Storage1 és a típus neve Standard_GRS, és az eredményt a $StorageAccount nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fb9df-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>

<span data-ttu-id="fb9df-111">A második parancs a $StorageAccount változóban tárolt tárterület-azonosító adataival hozza létre a tárterület-konfiguráció objektumát a médiafájlhoz társított elsődleges tárterület-fiókként.</span><span class="sxs-lookup"><span data-stu-id="fb9df-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="fb9df-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb9df-112">PARAMETERS</span></span>

### <span data-ttu-id="fb9df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb9df-113">-DefaultProfile</span></span>
<span data-ttu-id="fb9df-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fb9df-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb9df-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="fb9df-115">-IsPrimary</span></span>
<span data-ttu-id="fb9df-116">Azt jelzi, hogy a parancsmag a tárolási fiókot hozza létre a médiaszolgáltató elsődleges tárterületének.</span><span class="sxs-lookup"><span data-stu-id="fb9df-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9df-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="fb9df-117">-StorageAccountId</span></span>
<span data-ttu-id="fb9df-118">A tárolási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb9df-118">Specifies the ID of the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9df-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb9df-119">-Confirm</span></span>
<span data-ttu-id="fb9df-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb9df-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9df-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb9df-121">-WhatIf</span></span>
<span data-ttu-id="fb9df-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb9df-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb9df-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb9df-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb9df-124">CommonParameters</span></span>
<span data-ttu-id="fb9df-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb9df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb9df-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb9df-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb9df-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb9df-127">INPUTS</span></span>

### <span data-ttu-id="fb9df-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="fb9df-128">None</span></span>
<span data-ttu-id="fb9df-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="fb9df-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb9df-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb9df-130">OUTPUTS</span></span>

### <span data-ttu-id="fb9df-131">Microsoft. Azure. commands. Media. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb9df-131">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="fb9df-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb9df-132">NOTES</span></span>

## <span data-ttu-id="fb9df-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb9df-133">RELATED LINKS</span></span>

[<span data-ttu-id="fb9df-134">Szinkronizálás – AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="fb9df-134">Sync-AzureRmMediaServiceStorageKeys</span></span>](./Sync-AzureRmMediaServiceStorageKeys.md)


