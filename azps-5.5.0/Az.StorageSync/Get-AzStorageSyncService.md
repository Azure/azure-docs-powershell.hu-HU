---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: ec446a92c96bd92d7a4af5610f00ff76dcd50b50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157907"
---
# <span data-ttu-id="764af-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="764af-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="764af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="764af-102">SYNOPSIS</span></span>
<span data-ttu-id="764af-103">Ez a parancs felsorolja az adott előfizetési/erőforráscsoporton belüli összes tárterület-szinkronizálási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="764af-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="764af-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="764af-104">SYNTAX</span></span>

### <span data-ttu-id="764af-105">ParentStringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="764af-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="764af-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="764af-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="764af-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="764af-107">DESCRIPTION</span></span>
<span data-ttu-id="764af-108">Ez a parancs felsorolja az adott előfizetési/erőforráscsoporton belüli összes tárterület-szinkronizálási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="764af-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="764af-109">Az egyes tárhelyszinkronizálási szolgáltatások attribútumainak felsorolására is használható.</span><span class="sxs-lookup"><span data-stu-id="764af-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="764af-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="764af-110">EXAMPLES</span></span>

### <span data-ttu-id="764af-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="764af-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="764af-112">Ez a parancs felsorolja az adott erőforráscsoporton belüli összes tárterület-szinkronizálási szolgáltatáserőforrást.</span><span class="sxs-lookup"><span data-stu-id="764af-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="764af-113">Az egyes tárhelyszinkronizálási szolgáltatások attribútumainak felsorolására is használható.</span><span class="sxs-lookup"><span data-stu-id="764af-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="764af-114">A -StorageSyncServiceName paramétert megadásával adott értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="764af-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="764af-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="764af-115">PARAMETERS</span></span>

### <span data-ttu-id="764af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="764af-116">-DefaultProfile</span></span>
<span data-ttu-id="764af-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="764af-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="764af-118">-Name</span><span class="sxs-lookup"><span data-stu-id="764af-118">-Name</span></span>
<span data-ttu-id="764af-119">A tárterület-szinkronizálási szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="764af-119">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="764af-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="764af-120">-ResourceGroupName</span></span>
<span data-ttu-id="764af-121">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="764af-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="764af-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="764af-122">CommonParameters</span></span>
<span data-ttu-id="764af-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="764af-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="764af-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="764af-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="764af-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="764af-125">INPUTS</span></span>

### <span data-ttu-id="764af-126">System.String</span><span class="sxs-lookup"><span data-stu-id="764af-126">System.String</span></span>

## <span data-ttu-id="764af-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="764af-127">OUTPUTS</span></span>

### <span data-ttu-id="764af-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="764af-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="764af-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="764af-129">NOTES</span></span>

## <span data-ttu-id="764af-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="764af-130">RELATED LINKS</span></span>
