---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceExtensionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
ms.openlocfilehash: d37a717ba87771310de4f1944e3865712e00554e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935841"
---
# <span data-ttu-id="ee0e6-101">New-AzCloudServiceExtensionObject</span><span class="sxs-lookup"><span data-stu-id="ee0e6-101">New-AzCloudServiceExtensionObject</span></span>

## <span data-ttu-id="ee0e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee0e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ee0e6-103">Memóriában lévő objektum létrehozása bővítményhez</span><span class="sxs-lookup"><span data-stu-id="ee0e6-103">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="ee0e6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ee0e6-104">SYNTAX</span></span>

```
New-AzCloudServiceExtensionObject [-AutoUpgradeMinorVersion <Boolean>] [-Name <String>]
 [-ProtectedSetting <String>] [-Publisher <String>] [-RolesAppliedTo <String[]>] [-Setting <String>]
 [-Type <String>] [-TypeHandlerVersion <String>] [<CommonParameters>]
```

## <span data-ttu-id="ee0e6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ee0e6-105">DESCRIPTION</span></span>
<span data-ttu-id="ee0e6-106">Memóriában lévő objektum létrehozása bővítményhez</span><span class="sxs-lookup"><span data-stu-id="ee0e6-106">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="ee0e6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ee0e6-107">EXAMPLES</span></span>

### <span data-ttu-id="ee0e6-108">1. példa: A Mintával bővítő objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="ee0e6-108">Example 1: Create Geneva extension object</span></span>
```powershell
PS C:\> $extension = New-AzCloudServiceExtensionObject -Name "GenevaExtension" -Publisher "Microsoft.Azure.Geneva" -Type "GenevaMonitoringPaaS" -TypeHandlerVersion "2.14.0.2"
```

<span data-ttu-id="ee0e6-109">Ezzel a paranccsal egy Olyan Extension-objektumot hoz létre, amely egy felhőszolgáltatás létrehozására vagy frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="ee0e6-109">This command creates Geneva extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="ee0e6-110">További részletekért lásd: New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="ee0e6-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="ee0e6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee0e6-111">PARAMETERS</span></span>

### <span data-ttu-id="ee0e6-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ee0e6-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="ee0e6-113">Explicit módon adja meg, hogy a crp képes-e automatikusan frissíteni a TypeHandlerVersiont a nagyobb alverziókra, amikor elérhetővé válnak.</span><span class="sxs-lookup"><span data-stu-id="ee0e6-113">Explicitly specify whether CRP can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee0e6-114">-Name</span><span class="sxs-lookup"><span data-stu-id="ee0e6-114">-Name</span></span>
<span data-ttu-id="ee0e6-115">név.</span><span class="sxs-lookup"><span data-stu-id="ee0e6-115">Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee0e6-116">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="ee0e6-116">-ProtectedSetting</span></span>
<span data-ttu-id="ee0e6-117">A bővítmény védett beállításai, amelyek titkosítottak, mielőtt elküldik a VM-nek.</span><span class="sxs-lookup"><span data-stu-id="ee0e6-117">Protected settings for the extension which are encrypted before sent to the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee0e6-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ee0e6-118">-Publisher</span></span>
<span data-ttu-id="ee0e6-119">Publisher.</span><span class="sxs-lookup"><span data-stu-id="ee0e6-119">Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee0e6-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="ee0e6-120">-RolesAppliedTo</span></span>
<span data-ttu-id="ee0e6-121">RolesAppliedTo.</span><span class="sxs-lookup"><span data-stu-id="ee0e6-121">RolesAppliedTo.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee0e6-122">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="ee0e6-122">-Setting</span></span>
<span data-ttu-id="ee0e6-123">A bővítmény nyilvános beállításai.</span><span class="sxs-lookup"><span data-stu-id="ee0e6-123">Public settings for the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee0e6-124">-Type</span><span class="sxs-lookup"><span data-stu-id="ee0e6-124">-Type</span></span>
<span data-ttu-id="ee0e6-125">Írja be a megfelelő parancsot.</span><span class="sxs-lookup"><span data-stu-id="ee0e6-125">Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee0e6-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ee0e6-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="ee0e6-127">TypeHandlerVersion.</span><span class="sxs-lookup"><span data-stu-id="ee0e6-127">TypeHandlerVersion.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee0e6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee0e6-128">CommonParameters</span></span>
<span data-ttu-id="ee0e6-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee0e6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee0e6-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee0e6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee0e6-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee0e6-131">INPUTS</span></span>

## <span data-ttu-id="ee0e6-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee0e6-132">OUTPUTS</span></span>

### <span data-ttu-id="ee0e6-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="ee0e6-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="ee0e6-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ee0e6-134">NOTES</span></span>

<span data-ttu-id="ee0e6-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ee0e6-135">ALIASES</span></span>

## <span data-ttu-id="ee0e6-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee0e6-136">RELATED LINKS</span></span>

