---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/sync-azmediaservicestoragekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
ms.openlocfilehash: e9d413a8f77422b723c2dabc57d7d68c691617d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835165"
---
# <span data-ttu-id="fc1f1-101">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="fc1f1-101">Sync-AzMediaServiceStorageKey</span></span>

## <span data-ttu-id="fc1f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc1f1-102">SYNOPSIS</span></span>
<span data-ttu-id="fc1f1-103">A Media szolgáltatáshoz társított tárolási fiókhoz tartozó tárolási fiók kulcsait szinkronizálja.</span><span class="sxs-lookup"><span data-stu-id="fc1f1-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="fc1f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc1f1-104">SYNTAX</span></span>

```
Sync-AzMediaServiceStorageKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc1f1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc1f1-105">DESCRIPTION</span></span>
<span data-ttu-id="fc1f1-106">A **szinkronizáló-AzMediaServiceStorageKey** parancsmag a médiaszolgáltató által társított tárterület-fiókhoz szinkronizálja a tárolási fiók kulcsait.</span><span class="sxs-lookup"><span data-stu-id="fc1f1-106">The **Sync-AzMediaServiceStorageKey** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="fc1f1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fc1f1-107">EXAMPLES</span></span>

### <span data-ttu-id="fc1f1-108">1. példa: a Media szolgáltatáshoz társított tárterület-fiókhoz tartozó tárterület-kulcsok szinkronizálása</span><span class="sxs-lookup"><span data-stu-id="fc1f1-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzMediaServiceStorageKey -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="fc1f1-109">Az első parancs az Get-AzStorageAccount parancsmagot használja a Storage135 nevű, a ResourceGroup001 nevű tárterület-fiók beszerzéséhez, és az eredményt az $StorageAccount nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fc1f1-109">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="fc1f1-110">A második parancs a $StorageAccount változóban található **azonosító** tulajdonsággal szinkronizálja a MediaService001 nevű Media-szolgáltatás tárolási kulcsát.</span><span class="sxs-lookup"><span data-stu-id="fc1f1-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="fc1f1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc1f1-111">PARAMETERS</span></span>

### <span data-ttu-id="fc1f1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fc1f1-112">-AccountName</span></span>
<span data-ttu-id="fc1f1-113">Annak a médiafájlnak a nevét adja meg, amelyre a parancsmag szinkronizálja.</span><span class="sxs-lookup"><span data-stu-id="fc1f1-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc1f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc1f1-114">-DefaultProfile</span></span>
<span data-ttu-id="fc1f1-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fc1f1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc1f1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc1f1-116">-ResourceGroupName</span></span>
<span data-ttu-id="fc1f1-117">A Media-szolgáltatást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc1f1-117">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="fc1f1-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="fc1f1-118">-StorageAccountId</span></span>
<span data-ttu-id="fc1f1-119">A Media Service-fiókhoz társított tárolási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc1f1-119">Specifies the storage account ID associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc1f1-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fc1f1-120">-Confirm</span></span>
<span data-ttu-id="fc1f1-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fc1f1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc1f1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc1f1-122">-WhatIf</span></span>
<span data-ttu-id="fc1f1-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fc1f1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc1f1-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fc1f1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc1f1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc1f1-125">CommonParameters</span></span>
<span data-ttu-id="fc1f1-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc1f1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc1f1-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc1f1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc1f1-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc1f1-128">INPUTS</span></span>

### <span data-ttu-id="fc1f1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fc1f1-129">System.String</span></span>

## <span data-ttu-id="fc1f1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc1f1-130">OUTPUTS</span></span>

### <span data-ttu-id="fc1f1-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc1f1-131">System.Boolean</span></span>

## <span data-ttu-id="fc1f1-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc1f1-132">NOTES</span></span>

## <span data-ttu-id="fc1f1-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc1f1-133">RELATED LINKS</span></span>
