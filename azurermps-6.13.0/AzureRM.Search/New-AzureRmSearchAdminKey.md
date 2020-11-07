---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchAdminKey.md
ms.openlocfilehash: fa7ea6f1e53b94a349d51856432f1c01b2e89ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673131"
---
# <span data-ttu-id="b6269-101">New-AzureRmSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="b6269-101">New-AzureRmSearchAdminKey</span></span>

## <span data-ttu-id="b6269-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6269-102">SYNOPSIS</span></span>
<span data-ttu-id="b6269-103">Újragenerálja az Azure Search szolgáltatás rendszergazdai kulcsát.</span><span class="sxs-lookup"><span data-stu-id="b6269-103">Regenerates an admin key of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6269-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6269-104">SYNTAX</span></span>

### <span data-ttu-id="b6269-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b6269-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6269-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6269-106">ParentObjectParameterSet</span></span>
```
New-AzureRmSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6269-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6269-107">ParentResourceIdParameterSet</span></span>
```
New-AzureRmSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6269-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6269-108">DESCRIPTION</span></span>
<span data-ttu-id="b6269-109">A **New-AzureRmSearchAdminKey** parancsmag regenerálta az Azure keresési szolgáltatás rendszergazdai kulcsát.</span><span class="sxs-lookup"><span data-stu-id="b6269-109">The **New-AzureRmSearchAdminKey** cmdlet regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="b6269-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b6269-110">EXAMPLES</span></span>

### <span data-ttu-id="b6269-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b6269-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="b6269-112">A példa regenerálta az Azure keresési szolgáltatás elsődleges kulcsát.</span><span class="sxs-lookup"><span data-stu-id="b6269-112">The example regenerates Primary key of the Azure Search Service.</span></span>

## <span data-ttu-id="b6269-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6269-113">PARAMETERS</span></span>

### <span data-ttu-id="b6269-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6269-114">-DefaultProfile</span></span>
<span data-ttu-id="b6269-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6269-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6269-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b6269-116">-Force</span></span>
<span data-ttu-id="b6269-117">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6269-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b6269-118">-Kind</span><span class="sxs-lookup"><span data-stu-id="b6269-118">-KeyKind</span></span>
<span data-ttu-id="b6269-119">Keresési szolgáltatás-rendszergazdai kulcs típusa (elsődleges/másodlagos)</span><span class="sxs-lookup"><span data-stu-id="b6269-119">Search Service admin key kind (Primary/Secondary).</span></span>

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

### <span data-ttu-id="b6269-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b6269-120">-ParentObject</span></span>
<span data-ttu-id="b6269-121">Keresési szolgáltatás bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="b6269-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="b6269-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b6269-122">-ParentResourceId</span></span>
<span data-ttu-id="b6269-123">Keresési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b6269-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="b6269-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6269-124">-ResourceGroupName</span></span>
<span data-ttu-id="b6269-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b6269-125">Resource Group name.</span></span>

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

### <span data-ttu-id="b6269-126">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="b6269-126">-ServiceName</span></span>
<span data-ttu-id="b6269-127">Keresési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="b6269-127">Search Service name.</span></span>

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

### <span data-ttu-id="b6269-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6269-128">-Confirm</span></span>
<span data-ttu-id="b6269-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6269-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6269-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6269-130">-WhatIf</span></span>
<span data-ttu-id="b6269-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6269-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6269-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6269-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6269-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6269-133">CommonParameters</span></span>
<span data-ttu-id="b6269-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6269-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6269-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6269-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6269-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6269-136">INPUTS</span></span>

### <span data-ttu-id="b6269-137">Microsoft. Azure. commands. Management. Search. models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="b6269-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="b6269-138">Paraméterek: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b6269-138">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="b6269-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b6269-139">System.String</span></span>

## <span data-ttu-id="b6269-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6269-140">OUTPUTS</span></span>

### <span data-ttu-id="b6269-141">Microsoft. Azure. commands. Management. Search. models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="b6269-141">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="b6269-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6269-142">NOTES</span></span>

## <span data-ttu-id="b6269-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6269-143">RELATED LINKS</span></span>

[<span data-ttu-id="b6269-144">Get-AzureRmSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="b6269-144">Get-AzureRmSearchAdminKeyPair</span></span>](./Get-AzureRmSearchAdminKeyPair.md)
