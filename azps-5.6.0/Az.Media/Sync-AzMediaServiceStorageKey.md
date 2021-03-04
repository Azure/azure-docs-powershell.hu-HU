---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/powershell/module/az.media/sync-azmediaservicestoragekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
ms.openlocfilehash: 75e83c3d861bfbe579634da0ee136f564be43ba8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934105"
---
# <span data-ttu-id="34c14-101">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="34c14-101">Sync-AzMediaServiceStorageKey</span></span>

## <span data-ttu-id="34c14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34c14-102">SYNOPSIS</span></span>
<span data-ttu-id="34c14-103">Szinkronizálja a médiaszolgáltatással társított tárfiókok tárfiókkulcsait.</span><span class="sxs-lookup"><span data-stu-id="34c14-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="34c14-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="34c14-104">SYNTAX</span></span>

```
Sync-AzMediaServiceStorageKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34c14-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="34c14-105">DESCRIPTION</span></span>
<span data-ttu-id="34c14-106">A **Sync-AzMediaServiceStorageKey** parancsmag szinkronizálja a médiaszolgáltatással társított tárfiókok tárfiókkulcsait.</span><span class="sxs-lookup"><span data-stu-id="34c14-106">The **Sync-AzMediaServiceStorageKey** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="34c14-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="34c14-107">EXAMPLES</span></span>

### <span data-ttu-id="34c14-108">1. példa: A médiaszolgáltatással társított tárfiók kulcsának szinkronizálása</span><span class="sxs-lookup"><span data-stu-id="34c14-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzMediaServiceStorageKey -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="34c14-109">Az első parancs a Get-AzStorageAccount parancsmagot használva szerezze be a Storage135 nevű tárfiókot, amely az ResourceGroup001-hez tartozik, és az eredményt a $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="34c14-109">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="34c14-110">A második parancs szinkronizálja a MediaService001 nevű médiaszolgáltatás  tárfiókkulcsait a $StorageAccount azonosítótulajdonságával.</span><span class="sxs-lookup"><span data-stu-id="34c14-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="34c14-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34c14-111">PARAMETERS</span></span>

### <span data-ttu-id="34c14-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="34c14-112">-AccountName</span></span>
<span data-ttu-id="34c14-113">A parancsmag által szinkronizált médiaszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="34c14-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

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

### <span data-ttu-id="34c14-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c14-114">-DefaultProfile</span></span>
<span data-ttu-id="34c14-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="34c14-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34c14-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34c14-116">-ResourceGroupName</span></span>
<span data-ttu-id="34c14-117">Annak az erőforráscsoportnak a nevét adja meg, amely az médiaszolgáltatást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="34c14-117">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="34c14-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="34c14-118">-StorageAccountId</span></span>
<span data-ttu-id="34c14-119">A médiaszolgáltatás-fiókhoz társított tárfiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="34c14-119">Specifies the storage account ID associated with the media service account.</span></span>

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

### <span data-ttu-id="34c14-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34c14-120">-Confirm</span></span>
<span data-ttu-id="34c14-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="34c14-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34c14-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34c14-122">-WhatIf</span></span>
<span data-ttu-id="34c14-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="34c14-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34c14-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="34c14-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34c14-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c14-125">CommonParameters</span></span>
<span data-ttu-id="34c14-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34c14-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c14-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34c14-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c14-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34c14-128">INPUTS</span></span>

### <span data-ttu-id="34c14-129">System.String</span><span class="sxs-lookup"><span data-stu-id="34c14-129">System.String</span></span>

## <span data-ttu-id="34c14-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34c14-130">OUTPUTS</span></span>

### <span data-ttu-id="34c14-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="34c14-131">System.Boolean</span></span>

## <span data-ttu-id="34c14-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="34c14-132">NOTES</span></span>

## <span data-ttu-id="34c14-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34c14-133">RELATED LINKS</span></span>
