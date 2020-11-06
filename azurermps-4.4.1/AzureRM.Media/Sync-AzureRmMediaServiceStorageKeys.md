---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Sync-AzureRmMediaServiceStorageKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Sync-AzureRmMediaServiceStorageKeys.md
ms.openlocfilehash: 71112bf54f4de8e0c7e4fd1ecfd296eff45ac868
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502688"
---
# <span data-ttu-id="9c5ff-101">Sync-AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="9c5ff-101">Sync-AzureRmMediaServiceStorageKeys</span></span>

## <span data-ttu-id="9c5ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c5ff-102">SYNOPSIS</span></span>
<span data-ttu-id="9c5ff-103">A Media szolgáltatáshoz társított tárolási fiókhoz tartozó tárolási fiók kulcsait szinkronizálja.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c5ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c5ff-104">SYNTAX</span></span>

```
Sync-AzureRmMediaServiceStorageKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c5ff-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c5ff-105">DESCRIPTION</span></span>
<span data-ttu-id="9c5ff-106">A **szinkronizáló-AzureRmMediaServiceStorageKeys** parancsmag a médiaszolgáltató által társított tárterület-fiókhoz szinkronizálja a tárolási fiók kulcsait.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-106">The **Sync-AzureRmMediaServiceStorageKeys** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="9c5ff-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9c5ff-107">EXAMPLES</span></span>

### <span data-ttu-id="9c5ff-108">1. példa: a Media szolgáltatáshoz társított tárterület-fiókhoz tartozó tárterület-kulcsok szinkronizálása</span><span class="sxs-lookup"><span data-stu-id="9c5ff-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzureRmStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzureRmMediaServiceStorageKeys -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="9c5ff-109">Az első parancs az Get-AzureRmStorageAccount parancsmagot használja a Storage135 nevű, a ResourceGroup001 nevű tárterület-fiók beszerzéséhez, és az eredményt az $StorageAccount nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-109">The first command uses the Get-AzureRmStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>

<span data-ttu-id="9c5ff-110">A második parancs a $StorageAccount változóban található **azonosító** tulajdonsággal szinkronizálja a MediaService001 nevű Media-szolgáltatás tárolási kulcsát.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="9c5ff-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c5ff-111">PARAMETERS</span></span>

### <span data-ttu-id="9c5ff-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9c5ff-112">-AccountName</span></span>
<span data-ttu-id="9c5ff-113">Annak a médiafájlnak a nevét adja meg, amelyre a parancsmag szinkronizálja.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

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

### <span data-ttu-id="9c5ff-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c5ff-114">-ResourceGroupName</span></span>
<span data-ttu-id="9c5ff-115">A Media-szolgáltatást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-115">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="9c5ff-116">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9c5ff-116">-StorageAccountId</span></span>
<span data-ttu-id="9c5ff-117">A Media Service-fiókhoz társított tárolási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-117">Specifies the storage account ID associated with the media service account.</span></span>

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

### <span data-ttu-id="9c5ff-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9c5ff-118">-Confirm</span></span>
<span data-ttu-id="9c5ff-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c5ff-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c5ff-120">-WhatIf</span></span>
<span data-ttu-id="9c5ff-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c5ff-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c5ff-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c5ff-123">-DefaultProfile</span></span>
<span data-ttu-id="9c5ff-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c5ff-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c5ff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5ff-125">CommonParameters</span></span>
<span data-ttu-id="9c5ff-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c5ff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5ff-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c5ff-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5ff-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c5ff-128">INPUTS</span></span>

## <span data-ttu-id="9c5ff-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c5ff-129">OUTPUTS</span></span>

### <span data-ttu-id="9c5ff-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c5ff-130">System.Boolean</span></span>

## <span data-ttu-id="9c5ff-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c5ff-131">NOTES</span></span>

## <span data-ttu-id="9c5ff-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c5ff-132">RELATED LINKS</span></span>

