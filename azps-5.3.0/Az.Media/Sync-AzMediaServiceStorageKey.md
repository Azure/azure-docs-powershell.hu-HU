---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/sync-azmediaservicestoragekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
ms.openlocfilehash: 9ac16dec6403eb17f5c0bc352b7419aeb9854fec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481259"
---
# <span data-ttu-id="37d4d-101">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="37d4d-101">Sync-AzMediaServiceStorageKey</span></span>

## <span data-ttu-id="37d4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="37d4d-103">Szinkronizálja a médiaszolgáltatással társított tárfiókok tárfiókkulcsait.</span><span class="sxs-lookup"><span data-stu-id="37d4d-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="37d4d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="37d4d-104">SYNTAX</span></span>

```
Sync-AzMediaServiceStorageKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37d4d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="37d4d-105">DESCRIPTION</span></span>
<span data-ttu-id="37d4d-106">A **Sync-AzMediaServiceStorageKey** parancsmag szinkronizálja a médiaszolgáltatással társított tárfiókok tárfiókkulcsait.</span><span class="sxs-lookup"><span data-stu-id="37d4d-106">The **Sync-AzMediaServiceStorageKey** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="37d4d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="37d4d-107">EXAMPLES</span></span>

### <span data-ttu-id="37d4d-108">1. példa: Az adathordozó-szolgáltatással társított tárfiók kulcsának szinkronizálása</span><span class="sxs-lookup"><span data-stu-id="37d4d-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzMediaServiceStorageKey -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="37d4d-109">Az első parancs a Get-AzStorageAccount parancsmag segítségével lekérte a Storage135 nevű tárfiókot, amely az ResourceGroup001-hez tartozik, és az eredményt a $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="37d4d-109">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="37d4d-110">A második parancs szinkronizálja a MediaService001 nevű médiaszolgáltatás  tárfiókkulcsait a $StorageAccount azonosítótulajdonságával.</span><span class="sxs-lookup"><span data-stu-id="37d4d-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="37d4d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37d4d-111">PARAMETERS</span></span>

### <span data-ttu-id="37d4d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="37d4d-112">-AccountName</span></span>
<span data-ttu-id="37d4d-113">A parancsmag által szinkronizált médiaszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="37d4d-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

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

### <span data-ttu-id="37d4d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d4d-114">-DefaultProfile</span></span>
<span data-ttu-id="37d4d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="37d4d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37d4d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37d4d-116">-ResourceGroupName</span></span>
<span data-ttu-id="37d4d-117">Annak az erőforráscsoportnak a nevét adja meg, amely az médiaszolgáltatást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="37d4d-117">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="37d4d-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="37d4d-118">-StorageAccountId</span></span>
<span data-ttu-id="37d4d-119">A médiaszolgáltatás-fiókhoz társított tárfiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="37d4d-119">Specifies the storage account ID associated with the media service account.</span></span>

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

### <span data-ttu-id="37d4d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37d4d-120">-Confirm</span></span>
<span data-ttu-id="37d4d-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="37d4d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37d4d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37d4d-122">-WhatIf</span></span>
<span data-ttu-id="37d4d-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="37d4d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37d4d-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="37d4d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37d4d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d4d-125">CommonParameters</span></span>
<span data-ttu-id="37d4d-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37d4d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d4d-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37d4d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d4d-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37d4d-128">INPUTS</span></span>

### <span data-ttu-id="37d4d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="37d4d-129">System.String</span></span>

## <span data-ttu-id="37d4d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37d4d-130">OUTPUTS</span></span>

### <span data-ttu-id="37d4d-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37d4d-131">System.Boolean</span></span>

## <span data-ttu-id="37d4d-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="37d4d-132">NOTES</span></span>

## <span data-ttu-id="37d4d-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37d4d-133">RELATED LINKS</span></span>
