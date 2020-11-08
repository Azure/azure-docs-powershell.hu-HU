---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: d53edc73bb1813841403348919758f1c6c13eff4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195792"
---
# <span data-ttu-id="4eebd-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="4eebd-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="4eebd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4eebd-102">SYNOPSIS</span></span>
<span data-ttu-id="4eebd-103">A Media Service-parancsmagok tárterület-konfigurációjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="4eebd-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="4eebd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4eebd-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eebd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4eebd-105">DESCRIPTION</span></span>
<span data-ttu-id="4eebd-106">A **New-AzMediaServiceStorageConfig** parancsmag a Media Service-parancsmagok tárolási fiókjának konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="4eebd-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="4eebd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4eebd-107">EXAMPLES</span></span>

### <span data-ttu-id="4eebd-108">Példa 1: a Media Service-parancsmagok tároló-konfigurációjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="4eebd-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="4eebd-109">Az első parancs **a New-AzStorageAccount** parancsmaggal hozza létre a Storage Account objektum objektumát.</span><span class="sxs-lookup"><span data-stu-id="4eebd-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="4eebd-110">A parancs a tárolási fiók Storage1 és a típus neve Standard_GRS, és az eredményt a $StorageAccount nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4eebd-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="4eebd-111">A második parancs a $StorageAccount változóban tárolt tárterület-azonosító adataival hozza létre a tárterület-konfiguráció objektumát a médiafájlhoz társított elsődleges tárterület-fiókként.</span><span class="sxs-lookup"><span data-stu-id="4eebd-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="4eebd-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4eebd-112">PARAMETERS</span></span>

### <span data-ttu-id="4eebd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eebd-113">-DefaultProfile</span></span>
<span data-ttu-id="4eebd-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4eebd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4eebd-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="4eebd-115">-IsPrimary</span></span>
<span data-ttu-id="4eebd-116">Azt jelzi, hogy a parancsmag a tárolási fiókot hozza létre a médiaszolgáltató elsődleges tárterületének.</span><span class="sxs-lookup"><span data-stu-id="4eebd-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eebd-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4eebd-117">-StorageAccountId</span></span>
<span data-ttu-id="4eebd-118">A tárolási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4eebd-118">Specifies the ID of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eebd-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4eebd-119">-Confirm</span></span>
<span data-ttu-id="4eebd-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4eebd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eebd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eebd-121">-WhatIf</span></span>
<span data-ttu-id="4eebd-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4eebd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eebd-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4eebd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eebd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eebd-124">CommonParameters</span></span>
<span data-ttu-id="4eebd-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4eebd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eebd-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eebd-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eebd-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4eebd-127">INPUTS</span></span>

### <span data-ttu-id="4eebd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4eebd-128">System.String</span></span>

## <span data-ttu-id="4eebd-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4eebd-129">OUTPUTS</span></span>

### <span data-ttu-id="4eebd-130">Microsoft. Azure. commands. Media. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4eebd-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="4eebd-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4eebd-131">NOTES</span></span>

## <span data-ttu-id="4eebd-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4eebd-132">RELATED LINKS</span></span>

[<span data-ttu-id="4eebd-133">Szinkronizálás – AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="4eebd-133">Sync-AzMediaServiceStorageKey</span></span>](./Sync-AzMediaServiceStorageKey.md)

