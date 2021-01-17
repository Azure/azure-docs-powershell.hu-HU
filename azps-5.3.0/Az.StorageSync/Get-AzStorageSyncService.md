---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: ec446a92c96bd92d7a4af5610f00ff76dcd50b50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466866"
---
# <span data-ttu-id="bf5c7-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="bf5c7-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="bf5c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf5c7-102">SYNOPSIS</span></span>
<span data-ttu-id="bf5c7-103">Ez a parancs felsorolja az adott előfizetési/erőforráscsoporton belüli összes tárterület-szinkronizálási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="bf5c7-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="bf5c7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bf5c7-104">SYNTAX</span></span>

### <span data-ttu-id="bf5c7-105">ParentStringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bf5c7-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf5c7-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf5c7-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf5c7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bf5c7-107">DESCRIPTION</span></span>
<span data-ttu-id="bf5c7-108">Ez a parancs felsorolja az adott előfizetési/erőforráscsoporton belüli összes tárterület-szinkronizálási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="bf5c7-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="bf5c7-109">Az egyes tárhelyszinkronizálási szolgáltatások attribútumainak felsorolására is használható.</span><span class="sxs-lookup"><span data-stu-id="bf5c7-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="bf5c7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bf5c7-110">EXAMPLES</span></span>

### <span data-ttu-id="bf5c7-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="bf5c7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="bf5c7-112">Ez a parancs felsorolja az adott erőforráscsoporton belüli összes tárterület-szinkronizálási szolgáltatáserőforrást.</span><span class="sxs-lookup"><span data-stu-id="bf5c7-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="bf5c7-113">Az egyes tárhelyszinkronizálási szolgáltatások attribútumainak felsorolására is használható.</span><span class="sxs-lookup"><span data-stu-id="bf5c7-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="bf5c7-114">A -StorageSyncServiceName paramétert megadásával adott értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="bf5c7-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="bf5c7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf5c7-115">PARAMETERS</span></span>

### <span data-ttu-id="bf5c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf5c7-116">-DefaultProfile</span></span>
<span data-ttu-id="bf5c7-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf5c7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf5c7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bf5c7-118">-Name</span></span>
<span data-ttu-id="bf5c7-119">A tárterület-szinkronizálási szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="bf5c7-119">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="bf5c7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf5c7-120">-ResourceGroupName</span></span>
<span data-ttu-id="bf5c7-121">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bf5c7-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="bf5c7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf5c7-122">CommonParameters</span></span>
<span data-ttu-id="bf5c7-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf5c7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf5c7-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf5c7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf5c7-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf5c7-125">INPUTS</span></span>

### <span data-ttu-id="bf5c7-126">System.String</span><span class="sxs-lookup"><span data-stu-id="bf5c7-126">System.String</span></span>

## <span data-ttu-id="bf5c7-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf5c7-127">OUTPUTS</span></span>

### <span data-ttu-id="bf5c7-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="bf5c7-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="bf5c7-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bf5c7-129">NOTES</span></span>

## <span data-ttu-id="bf5c7-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf5c7-130">RELATED LINKS</span></span>
