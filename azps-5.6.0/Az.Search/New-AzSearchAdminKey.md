---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
ms.openlocfilehash: 4724b24f995b836bbd63420c852d6f0004089a51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938450"
---
# <span data-ttu-id="14de1-101">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="14de1-101">New-AzSearchAdminKey</span></span>

## <span data-ttu-id="14de1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14de1-102">SYNOPSIS</span></span>
<span data-ttu-id="14de1-103">Az Azure Cognitive Search szolgáltatás rendszergazdai kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="14de1-103">Regenerates an admin key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="14de1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="14de1-104">SYNTAX</span></span>

### <span data-ttu-id="14de1-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="14de1-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14de1-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14de1-106">ParentObjectParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14de1-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14de1-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14de1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="14de1-108">DESCRIPTION</span></span>
<span data-ttu-id="14de1-109">A **New-AzSearchAdminKey** parancsmag újragenerálja az Azure Kognitív keresés szolgáltatás rendszergazdai kulcsát.</span><span class="sxs-lookup"><span data-stu-id="14de1-109">The **New-AzSearchAdminKey** cmdlet regenerates an admin key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="14de1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="14de1-110">EXAMPLES</span></span>

### <span data-ttu-id="14de1-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="14de1-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="14de1-112">A példa létrehozza az Azure Kognitív keresési szolgáltatás elsődleges kulcsát.</span><span class="sxs-lookup"><span data-stu-id="14de1-112">The example regenerates Primary key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="14de1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14de1-113">PARAMETERS</span></span>

### <span data-ttu-id="14de1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14de1-114">-DefaultProfile</span></span>
<span data-ttu-id="14de1-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14de1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14de1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="14de1-116">-Force</span></span>
<span data-ttu-id="14de1-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="14de1-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14de1-118">-KeyKind</span><span class="sxs-lookup"><span data-stu-id="14de1-118">-KeyKind</span></span>
<span data-ttu-id="14de1-119">Az Azure Kognitív keresési szolgáltatás rendszergazdai kulcsának fajtája (Elsődleges/Másodlagos).</span><span class="sxs-lookup"><span data-stu-id="14de1-119">Azure Cognitive Search Service admin key kind (Primary/Secondary).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKeyKind
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14de1-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="14de1-120">-ParentObject</span></span>
<span data-ttu-id="14de1-121">Azure Kognitív keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="14de1-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14de1-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="14de1-122">-ParentResourceId</span></span>
<span data-ttu-id="14de1-123">Azure Kognitív keresési szolgáltatás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="14de1-123">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14de1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14de1-124">-ResourceGroupName</span></span>
<span data-ttu-id="14de1-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="14de1-125">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14de1-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="14de1-126">-ServiceName</span></span>
<span data-ttu-id="14de1-127">Azure Kognitív keresési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="14de1-127">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14de1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14de1-128">-Confirm</span></span>
<span data-ttu-id="14de1-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="14de1-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14de1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14de1-130">-WhatIf</span></span>
<span data-ttu-id="14de1-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="14de1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14de1-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="14de1-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14de1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14de1-133">CommonParameters</span></span>
<span data-ttu-id="14de1-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14de1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14de1-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14de1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14de1-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14de1-136">INPUTS</span></span>

### <span data-ttu-id="14de1-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="14de1-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="14de1-138">System.String</span><span class="sxs-lookup"><span data-stu-id="14de1-138">System.String</span></span>

## <span data-ttu-id="14de1-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14de1-139">OUTPUTS</span></span>

### <span data-ttu-id="14de1-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="14de1-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="14de1-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="14de1-141">NOTES</span></span>

## <span data-ttu-id="14de1-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14de1-142">RELATED LINKS</span></span>

[<span data-ttu-id="14de1-143">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="14de1-143">Get-AzSearchAdminKeyPair</span></span>](./Get-AzSearchAdminKeyPair.md)
