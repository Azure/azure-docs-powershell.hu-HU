---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: ec446a92c96bd92d7a4af5610f00ff76dcd50b50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302919"
---
# <span data-ttu-id="c4ffc-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c4ffc-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="c4ffc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ffc-103">Ez a parancs felsorolja az összes tárterület-szinkronizálási szolgáltatást az előfizetés/erőforrás csoport adott hatókörén belül.</span><span class="sxs-lookup"><span data-stu-id="c4ffc-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="c4ffc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4ffc-104">SYNTAX</span></span>

### <span data-ttu-id="c4ffc-105">ParentStringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4ffc-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4ffc-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4ffc-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4ffc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4ffc-107">DESCRIPTION</span></span>
<span data-ttu-id="c4ffc-108">Ez a parancs felsorolja az összes tárterület-szinkronizálási szolgáltatást az előfizetés/erőforrás csoport adott hatókörén belül.</span><span class="sxs-lookup"><span data-stu-id="c4ffc-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="c4ffc-109">Használható az egyes tárterület-szinkronizálási szolgáltatások attribútumainak felsorolása is.</span><span class="sxs-lookup"><span data-stu-id="c4ffc-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="c4ffc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c4ffc-110">EXAMPLES</span></span>

### <span data-ttu-id="c4ffc-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c4ffc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="c4ffc-112">Ez a parancs felsorolja az összes tárterület-szinkronizálási szolgáltatás erőforrását egy adott erőforráscsoport között.</span><span class="sxs-lookup"><span data-stu-id="c4ffc-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="c4ffc-113">Használható az egyes tárterület-szinkronizálási szolgáltatások attribútumainak felsorolása is.</span><span class="sxs-lookup"><span data-stu-id="c4ffc-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="c4ffc-114">A-StorageSyncServiceName, ha egy adott értéket szeretne visszaadni.</span><span class="sxs-lookup"><span data-stu-id="c4ffc-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="c4ffc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4ffc-115">PARAMETERS</span></span>

### <span data-ttu-id="c4ffc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ffc-116">-DefaultProfile</span></span>
<span data-ttu-id="c4ffc-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4ffc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4ffc-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c4ffc-118">-Name</span></span>
<span data-ttu-id="c4ffc-119">A tárterület-szinkronizálási szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="c4ffc-119">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ffc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4ffc-120">-ResourceGroupName</span></span>
<span data-ttu-id="c4ffc-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c4ffc-121">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ffc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ffc-122">CommonParameters</span></span>
<span data-ttu-id="c4ffc-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4ffc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ffc-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4ffc-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ffc-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4ffc-125">INPUTS</span></span>

### <span data-ttu-id="c4ffc-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c4ffc-126">System.String</span></span>

## <span data-ttu-id="c4ffc-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4ffc-127">OUTPUTS</span></span>

### <span data-ttu-id="c4ffc-128">Microsoft. Azure. Command. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c4ffc-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="c4ffc-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4ffc-129">NOTES</span></span>

## <span data-ttu-id="c4ffc-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4ffc-130">RELATED LINKS</span></span>
