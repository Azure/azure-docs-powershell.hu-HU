---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-azcloudserviceremotedesktopextensionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
ms.openlocfilehash: 022093b8fe1df28a151405a18009b40dd24b0c97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166651"
---
# <span data-ttu-id="f48c5-101">New-AzCloudServiceRemoteDesktopExtensionObject</span><span class="sxs-lookup"><span data-stu-id="f48c5-101">New-AzCloudServiceRemoteDesktopExtensionObject</span></span>

## <span data-ttu-id="f48c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f48c5-102">SYNOPSIS</span></span>
<span data-ttu-id="f48c5-103">Memóriában lévő objektum létrehozása távoli asztali bővítményhez</span><span class="sxs-lookup"><span data-stu-id="f48c5-103">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="f48c5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f48c5-104">SYNTAX</span></span>

```
New-AzCloudServiceRemoteDesktopExtensionObject [-Name] <String> [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-TypeHandlerVersion] <String>] [[-RolesAppliedTo] <String[]>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="f48c5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f48c5-105">DESCRIPTION</span></span>
<span data-ttu-id="f48c5-106">Memóriában lévő objektum létrehozása távoli asztali bővítményhez</span><span class="sxs-lookup"><span data-stu-id="f48c5-106">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="f48c5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f48c5-107">EXAMPLES</span></span>

### <span data-ttu-id="f48c5-108">1. példa: Távoli asztali bővítményobjektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="f48c5-108">Example 1: Create remote desktop extension object</span></span>
```powershell
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
```

<span data-ttu-id="f48c5-109">Ez a parancs távoli asztali bővítményobjektumot hoz létre, amely egy felhőszolgáltatás létrehozására vagy frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="f48c5-109">This command creates remote desktop extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="f48c5-110">További részleteket a New-AzCloudService webhelyen talál.</span><span class="sxs-lookup"><span data-stu-id="f48c5-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="f48c5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f48c5-111">PARAMETERS</span></span>

### <span data-ttu-id="f48c5-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f48c5-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f48c5-113">Alverzió automatikus frissítése.</span><span class="sxs-lookup"><span data-stu-id="f48c5-113">Auto upgrade minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48c5-114">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="f48c5-114">-Credential</span></span>
<span data-ttu-id="f48c5-115">Távoli asztali bővítmény hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="f48c5-115">Credential for Remote Desktop Extension.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48c5-116">-Expiration</span><span class="sxs-lookup"><span data-stu-id="f48c5-116">-Expiration</span></span>
<span data-ttu-id="f48c5-117">Távoli asztali bővítmény lejárata.</span><span class="sxs-lookup"><span data-stu-id="f48c5-117">Expiration for Remote Desktop Extension.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48c5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f48c5-118">-Name</span></span>
<span data-ttu-id="f48c5-119">A távoli asztali bővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="f48c5-119">Name of Remote Desktop Extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48c5-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="f48c5-120">-RolesAppliedTo</span></span>
<span data-ttu-id="f48c5-121">Az alkalmazott szerepkörök.</span><span class="sxs-lookup"><span data-stu-id="f48c5-121">Roles applied to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48c5-122">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f48c5-122">-TypeHandlerVersion</span></span>
<span data-ttu-id="f48c5-123">Távoli asztali bővítmény verziója.</span><span class="sxs-lookup"><span data-stu-id="f48c5-123">Remote Desktop Extension version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48c5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f48c5-124">CommonParameters</span></span>
<span data-ttu-id="f48c5-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f48c5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f48c5-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f48c5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f48c5-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f48c5-127">INPUTS</span></span>

## <span data-ttu-id="f48c5-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f48c5-128">OUTPUTS</span></span>

### <span data-ttu-id="f48c5-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="f48c5-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="f48c5-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f48c5-130">NOTES</span></span>

<span data-ttu-id="f48c5-131">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f48c5-131">ALIASES</span></span>

## <span data-ttu-id="f48c5-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f48c5-132">RELATED LINKS</span></span>

